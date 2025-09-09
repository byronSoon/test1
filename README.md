# test1

**基礎資料**

| **Endpoint** | <https://qcest-1.com> |
|----|----|
| **Token** | [8378d556-9d28-48dd-af0c-cefc7c8902f3_262800](8378d556-9d28-48dd-af0c-cefc7c8902f3_262800) |

| API功能 | Type | 網址 |
|----|----|----|
| 取得Bearer Token | GET | [{Endpoint}/GuruOutbound/GetBearer?gettoken=Token](%7bEndpoint%7d/GuruOutbound/GetBearer?gettoken=Token) |
| 對資料做動作，包含對資料做動作，包含查詢、更新、刪除… | POST | [{Endpoint}/GuruOutbound/TransBearer](%7bEndpoint%7d/GuruOubound/TransBearer) |

1.  **API獲取Token**

<!-- -->

1.  使用Postman在 URL輸入

[{Endpoint}/GuruOutbound/GetBearer?gettoken={Token}](%7bEndpoint%7d/GuruOutbound/GetBearer?gettoken=%7bToken%7d)，

並使用GET模式然後按下 **Send**。

<img src="C:\Users\kevin.lai\Downloads\教育訓練課程API_20250902_media/media/image2.png" style="width:5.76806in;height:0.62847in" />

2.  <img src="C:\Users\kevin.lai\Downloads\教育訓練課程API_20250902_media/media/image3.png" style="width:3.46546in;height:1.44452in" alt="一張含有 文字, 螢幕擷取畫面, 字型, 數字 的圖片 AI 產生的內容可能不正確。" />使用Postman在頁面下半部會顯示 JSON 格式的資料，其中的 **access token** 複製下來。

**二.使用Postman 設定Token**  
  
1.使用Postman並使用**GET模式**，在 URL 輸入欄輸入  
[{Endpoint}/GuruOutbound/TransBearer](https://qcest-1.com/GuruOubound/TransBearer)

<img src="C:\Users\kevin.lai\Downloads\教育訓練課程API_20250902_media/media/image4.png" style="width:5.76806in;height:1.59306in" />

2.點擊 URL 下方的 **Authorization**，選擇 **Bearer Token** 作為授權類型，並將剛剛複製的 **access token** 貼入 **Token** 欄位。<img src="C:\Users\kevin.lai\Downloads\教育訓練課程API_20250902_media/media/image5.png" style="width:5.76806in;height:1.57917in" />

**三.顯示API回傳資料:**  
1.點擊 **Body**，在 Body 區域輸入所需欄位（Token 欄位可留空）。  
<img src="C:\Users\kevin.lai\Downloads\教育訓練課程API_20250902_media/media/image6.png" style="width:5.76806in;height:1.625in" />  
{

    "ctrler": "DEVFORMT02",

    "method" : "xsp",

    "jsonParam" :

        "{ \\webQuery\\: \\0:1_100\\, \\uspName\\: \\personalCourseRecord_List\\, \\formNo\\: \\0\\ }",

    "token" : "your-token-here"

}

**四. API修改(新增)資料  **
1.使用Postman並使用**POST模式**，在 URL 輸入欄輸入  
[{Endpoint}/GuruOutbound/TransBearer](https://qcest-1.com/GuruOubound/TransBearer)**  **

2.Body 選擇raw 並貼上以下json  
**範例一: (對照第3點圖一)** <img src="C:\Users\kevin.lai\Downloads\教育訓練課程API_20250902_media/media/image7.png" style="width:5.76806in;height:1.66458in" alt="一張含有 文字, 螢幕擷取畫面, 行, 字型 的圖片 AI 產生的內容可能不正確。" />  
{

    "ctrler": "DEVFORMT02",

    "method": "xmit",

    "jsonParam": "{\\jsonData\\:\\{\\\\data\\\\:\[{\\\\course\\\\:\\\\測試video影片\\\\,

\\\\learning_method\\\\:\\\\線上課程\\\\,\\\\account\\\\:\\\\test@example.com\\\\,

\\\\name\\\\:\\\\王小明\\\\,\\\\first_learning_access_time\\\\:\\\\2025-08-01 09:00:00\\\\,

\\\\last_learning_access_time\\\\:\\\\2025-08-21 10:00:00\\\\,\\\\total_learning_time\\\\:\\\\01:30:00\\\\,

\\\\certification_hours\\\\:10,\\\\pass_status\\\\:\\\\通過\\\\},{\\\\course\\\\:\\\\測試vimeo影片2\\\\,

\\\\learning_method\\\\:\\\\線上課程\\\\,\\\\account\\\\:\\\\test@example.com\\\\,\\\\name\\\\:\\\\王小明\\\\,\\\\first_learning_access_time\\\\:\\\\2025-08-01 09:00:00\\\\,\\\\last_learning_access_time\\\\:\\\\2025-08-21 10:00:00\\\\,\\\\total_learning_time\\\\:\\\\01:30:00\\\\,\\\\certification_hours\\\\:10,

\\\\pass_status\\\\:\\\\通過\\\\}\]}\\,\\uspName\\:\\personalCourseRecord_Modify\\}",

    "token": "your-token-here"

}

**範例二: (對照第3點圖一)  **
<img src="C:\Users\kevin.lai\Downloads\教育訓練課程API_20250902_media/media/image8.png" style="width:5.76806in;height:1.80972in" />**  
{**

**"ctrler": "DEVFORMT02",**

**"method": "xmit",**

**"jsonParam": "{\\jsonData\\:\\{\\\\data\\\\:\[{\\\\totalcounta\\\\:1,\\\\rownum\\\\:\\\\21\\\\,\\\\course\\\\:\\\\0227限時課程問卷01\\\\,\\\\learning_method\\\\:\\\\線上課程\\\\,\\\\account\\\\:\\\\se01@se.com\\\\,\\\\name\\\\:\\\\維運01\\\\,\\\\first_learning_access_time\\\\:\\\\2025-02-27 14:15:12\\\\,\\\\last_learning_access_time\\\\:\\\\2025-02-27 14:15:12\\\\,\\\\total_learning_time\\\\:\\\\01:20:58\\\\,\\\\certification_hours\\\\:\\\\0.0\\\\,\\\\pass_status\\\\:\\\\通過\\\\}\]}\\ , \\uspName\\:\\personalCourseRecord_Modify\\}",**

**"token": ""**

**}**

3.按下 **Send**，修改的資料會在下方 Body 區域顯示。  
**圖一:**

<img src="C:\Users\kevin.lai\Downloads\教育訓練課程API_20250902_media/media/image9.png" style="width:5.60836in;height:1.37407in" />

**圖二:  **
<img src="C:\Users\kevin.lai\Downloads\教育訓練課程API_20250902_media/media/image10.png" style="width:5.76806in;height:1.67708in" />
