# Ch4. 第一次接觸JavaScript就上手

在前幾章課程中，我們學習了很多如何利用Html & CSS做出精美的網頁，但這樣的網頁，只能稱作靜態網頁，若需要有更多動態效果的互動網頁，我們需要使用客戶端的網頁技術，像是JavaScript這樣的腳本語言。

![HTML&#x3001;CSS&#x8207;JavaScript&#x4E4B;&#x9593;&#x95DC;&#x4FC2;](../.gitbook/assets/group-4.png)

## 規格版本

ECMAScript是目前Javascript統一的規格標準。

* ECMA-262的第一個版本於1997年6月被 ECMA 組織採納。
* ECMAScript 3 \(ES3\) 發行於1999年底。
* ECMAScript 4 \(ES4\) 棄用\(原因是貿然大幅度更新對用戶不太好所以改成每年逐一釋出\)。
* ECMAScript 5 \(ES5\) 發行於2009年底。
* ECMAScript 6 \(ES6\)  ****/ ECMAScript 2015 \(ES2015\) 發行於2015年中**。**
* ES2016 （ES7）2016年6月發布，為ECMAScript的第7個版本。
* ES2017 （ES8）2017年6月發布，為ECMAScript的第8個版本。

{% hint style="info" %}
**問：**ES 是什麼？  
**答：**ES 是 ECMAScript 的縮寫。 ES 後面跟著數字，則是ECMAScript的不同版本號。
{% endhint %}

## 開發環境

現在，我們要開始進入JS的殿堂～

![](../.gitbook/assets/image%20%287%29.png)



首先請在VSCode新增ㄧHTML檔案。  


HTML引入JavaScript程式同樣有幾種方式：

1. External Link

```markup
<head>
    <script type="text/javascript" src="test.js"></script>
</head>
```

    2. Embed  
瀏覽器只要讀到&lt;script&gt;標籤，就會知道內含JavaScript程式碼。

```markup
<script type="text/javascript">
    .....
</script>
```



