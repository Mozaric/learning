# Note of Html

## 目錄

[網頁技術](#網頁技術)

[小知識](#小知識)

[Html 檔架架構](#html-檔架架構)

[常用標籤](#常用標籤)

[連結](#連結)

[圖片](#圖片)

[影片](#影片)

[Youtube 影片](#youtube-影片)

[列表](#列表)

[表格](#表格)

[容器 (div)](#容器-div)

[容器 (span)](#容器-span)

[容器 (div) vs 容器 (span)](#容器-div-vs-容器-span)

[輸入控制項 (input)](#輸入控制項-input)

[輸入控制項 (textarea)](#輸入控制項-textarea)

[meta](#meta)

[參考資料](#參考資料)

## 網頁技術

| Technique  | Usage                     |
| ---------- | ------------------------- |
| Html       | Structure                 |
| CSS        | Presentation & Appearance |
| Javascript | Dynamism and Action       |

![](https://www.affde.com/uploads/article/50492/78Ilde35SFSD5y1v.gif)

## 小知識

+ 若欲關閉瀏覽器的 Javascript 功能，瀏覽靜態網頁
    - 網頁 → F12 → 設定 → 勾選`停用 Javacript`
+ 若欲關閉當前網頁的 CSS ，來瀏覽網頁骨架
    - 網頁 → F12 → 主控台 → 輸入 `document.head.parentNode.removeChild(document.head)` → 執行
+ 通常網頁首頁的檔案會命名為 `index.html`
+ 在檔案中不論換行、縮排與否，實際輸出的網頁是一樣的。此動作僅是為了提高程式碼的可讀性，讓人類更容易閱讀

## Html 檔架架構

+ 通常會於第一行輸入 `<!DOCTYPE html>` ，用來告知瀏覽器此檔案是 html 檔
+ 整體會由 `html` 標籤所包含
+ 其中 `head` 標籤內主要用來存放網頁資訊，而 `body` 標籤內用來存放網頁內容

```html
<!DOCTYPE html> <!-- 用來告知瀏覽器此檔案為 html 檔 -->
<html>
    <head>
        <!-- 存放網頁資訊 -->
        <meta charset="UTF-8"/> <!-- 設定網頁的編碼 -->
        <title>Frank 的網頁</title> <!-- 設定網頁的標題 -->
    </head>
    <body>
        <!-- 存放網頁內容 -->
        <h1>Hello World!</h1>
    </body>
</html>
```

## 常用標籤

| Tag      | Usage                          |
| -------- | ------------------------------ |
| head     | 網頁資訊                       |
| title    | 網頁標題                       |
| body     | 網頁內容                       |
| h1       | 標題(大)(通常一個網頁只有一個) |
| h6       | 標題(小)                       |
| p        | 一般的文字/段落                |
| b        | 粗體字                         |
| i        | 斜體字                         |
| br       | 換行                           |
| hr       | 水平線                         |
| a        | 超連結                         |
| img      | 圖片                           |
| video    | 影片                           |
| ul       | 列表(無順序)                   |
| ol       | 列表(有順序)                   |
| li       | 清單                           |
| table    | 表格                           |
| tr       | 表格行                         |
| td       | 表個資料                       |
| div      | 容器                           |
| span     | 容器                           |
| input    | 輸入                           |
| textarea | 輸入                           |

## 連結

使用 `a` 標籤，於 `href` 屬性設定欲連結的網頁/檔案，於`值`的部分設定欲顯示的文字

```html
<body>
    <h2>連結</h2>
    <a href="https://google.com">Google</a> <!-- 連結到網頁， 其中 href 是 a 的"屬性" -->
    <a href="page2.html">page2</a> <!-- 連結到同個資料夾下的 page2.html -->
    <a href="dir/page3.html">page3</a> <!-- 連結到 dir 資料夾下的 page3.html -->
    <a href="sample.PNG">簡介</a><!-- 連結到檔案 -->
</body>
```

![](image/example-link.png)

## 圖片

使用 `img` 標籤，於 `src` 屬性設定欲顯示的圖片位址，於 `width`, `height` 屬性設定圖片的寬度、高度(若寬、高僅設定其中一個數值，另一邊會使用等比例縮放)

```html
<body>
    <h2>圖片</h2>
    <img src="https://www.udacity.com/blog/wp-content/uploads/2020/06/HTML_Blog-scaled.jpeg" width="200"/> <!-- 顯示網路上的圖片 -->
    <img src="sample.PNG"/> <!-- 顯示同個資料夾下的圖片 -->
</body>
```

![](image/example-img.png)

## 影片

使用 `video` 標籤，於 `src` 屬性設定欲顯示的影片位址，加入 `controls` 屬性以顯示影片控制項，於 `width`, `height` 屬性設定影片寬度、高度，於`值`設定無法載入影片時的顯示文字

```html
<body>
    <h2>影片</h2>
    <video src="sample.mp4" controls width="500">無法載入影片</video>
</body>
```

![](image/example-video.png)

## Youtube 影片

於欲嵌入的 Youtube 影片選擇`分享→嵌入`即會產生程式碼

```html
<body>
    <h2>Youtube 影片</h2>
    <iframe width="560" height="315" src="https://www.youtube.com/embed/CLUPkcLQm64" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</body>
```

![](image/example-youtube-video.png)

## 列表

使用 `ul` (無序)或 `ol` (有序)標籤，於 `li` 標籤內輸入內容

```html
<body>
    <h2>列表</h2>
    <ul> <!-- 無序列表 -->
        <li>Google</li>
        <li>Facebook</li>
        <li>Instgram</li>
        <li>Twitter</li>
    </ul>
    <ol type="I"> <!-- 有序列表，使用 type 屬性調整項目符號 -->
        <li>Google</li>
        <li>Facebook</li>
        <li>Instgram</li>
        <li>Twitter</li>
    </ol>
</body>
```

![](image/example-list.png)

## 表格

使用 `table` 標籤，於 `width` 屬性內設定寬度，於 `tr` (table row)標籤內包含一行的資料，於 `td` (table data)標籤內輸入內容

```html
<body>
    <h2>表格</h2>
    <table width="300">
        <tr>
            <td>日期</td>
            <td>數學</td>
            <td>英文</td>
        </tr>
        <tr>
            <td>2022/02/08</td>
            <td>80</td>
            <td>90</td>
        </tr>
        <tr>
            <td>2022/02/09</td>
            <td>85</td>
            <td>95</td>
        </tr>
    </table>
</body>
```

![](image/example-table.png)

## 容器 (div)

有無使用容器其輸出的網頁是相同的，但未來在使用 CSS 做網頁美化時可提高方便性

```html
<body>
    <h2>容器 (div)</h2>
    <div>div1</div> <!-- 無論字多大，皆會佔用整行的空間-->
    <div>div2</div>
    <div style="background-color:red;"> <!-- 善用 div 可於 CSS 做美化網頁時方便許多-->
        <ul>
            <li>Google</li>
            <li>Facebook</li>
            <li>Instgram</li>
            <li>Twitter</li>
        </ul>
    </div>
</body>
```

![](image/example-div.png)

## 容器 (span)

```html
<body>
    <h2>容器 (span)</h2>
    <span>span1</span> <!-- 字多大，佔用的空間就多大-->
    <span>span2</span>
    <p>My mother has <span style="background-color:blue;">blue</span> eyes.</p> 
</body>
```

![](image/example-span.png)

## 容器 (div) vs 容器 (span)

The `span` tag is much like the `div` element, both are easily styled with CSS or manipulated with JavaScript using the class or id attribute, but `div` is a block-level element and `span` is an inline element.

## 輸入控制項 (input)

使用 `input` 標籤，於 `type` 屬性內設定控制項的種類

```html
<body>
    <h2>輸入控制項 (input)</h2>
    <input type="text" placeholder="請輸入帳號"/> <!-- type 屬性決定 input 類型， placeholder 屬性可設提示文字-->
    <br/><br/>
    <input type="password" placeholder="請輸入密碼"/>
    <br/><br/>
    <input type="date"/>
    <br/><br/>
    <input type="color"/>
    <br/><br/>
    <input type="file"/>
    <br/><br/>
    <input type="checkbox"/>
    <br/><br/>
    <input type="range"/>
</body>
```

![](image/example-input.png)

## 輸入控制項 (textarea)

使用 `textarea` 標籤，於 `placeholder` 屬性內設定提示文字

```html
<body>
    <h2>輸入控制項 (textarea)</h2>
    <textarea placeholder="請輸入文章"></textarea>
</body>
```

![](image/example-textarea.png)

## meta

使用 `meta` 標籤，用來設定網頁的資訊，以提供給瀏覽器、搜尋引擎

```html
<head> <!-- 存放網頁資訊 -->
    <meta charset="UTF-8"/> <!-- 設定網頁的編碼 -->
    <meta name="description" content="裡面有很多 html 範例"/> <!-- 提供給搜尋引擎的資訊 -->
    <meta name="author" content="Frank"/> <!-- 提供給搜尋引擎的資訊 -->
    <meta name="keywords" content="html, example"/> <!-- 提供給搜尋引擎的資訊 -->
    <meta name="viewport" content="width=device-width, initial-scale=1.0"/> <!-- 根據瀏覽裝置的寬度來對畫面做堤整/縮放，初始的縮放比為 100% -->
    <title>小白的網頁</title>
</head>
```

## 參考資料

[【html】1小時初學者教學](https://www.youtube.com/watch?v=CLUPkcLQm64)

[HTML Full Course - Build a Website Tutorial](https://www.youtube.com/watch?v=pQN-pnXPaVg)

[HTML Tutorial](https://www.w3schools.com/html/default.asp)

[HTML Reference](https://www.w3schools.com/tags/default.asp)
