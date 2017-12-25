# 熟悉 CSS

首先我們要先知道如何把CSS套用到網頁上。

1. Inline
```
<div style="color: white; font-size: 20;">...</div>
```
2. Embed
```
<style type="text/css">
  div {
    color: white;
  }
</style>
<div>...</div>
```
3. External Link
```
<link href="style.css" rel="stylesheet">
```
> p.s.假如有多個外部連結，則越後面套入的CSS優先權越高。

---

在前面已經提到，CSS語法必須由一選擇器，來指定屬性樣式。

而選擇器主要有三種：
- 類型 (Type) 選擇器：HTML 標籤
```
h1 {
  color: red;
}
```
- Class 選擇器：使用者自訂
```
.my-button {
  color: white;
}
```
- ID 選擇器：使用者自訂
```
#container {
  background-color: blue;
}
```

### 後代選擇器
但有時候css設定並沒有想像中這麼簡單。
例如今天html如下這樣呈現時
```
<ul>
  <li>
    first
  </li>
  <li>
    second
  </li>
  <li>
    third
  </li>
</ul>
```
當想改變ul中li的字型顏色，難道要為每個li都加上class嗎？這樣豈不是太麻煩了？
這時候CSS就可以這樣設定：
```
ul li {
  color: red;
}
```
### 子代選擇器
```
<div>
    <span>Blue</span>
    <p>
        <span>Black</span>
    </p>
</div>  
```
CSS若使用子代選擇器，如下表示：
```
div > span { 
  color: blue; 
} 
```
![](/assets/css-child-selector.png)
只有div **下一層** 的span會套用樣式。

若使用後代選擇器，如下表示：
```
div span { 
  color: blue; 
} 
```
則所有div下的span都會套用樣式。

### CSS Class 與 CSS ID
假若html如下這樣呈現：
```
<button id="first-btn">First</button>
<button id="second-btn">Second</button>
```
如果要分別更改兩個不同的button，則CSS可以這樣設定：

```
button#first-btn {
  color: red;
}
button.second-btn {
  color: blue;
}
```



### 分組選擇器：多個元素同個CSS
承上例，如果要一次設定多個元素為同一個CSS樣式，可以這樣設定：
```
button#first-btn ,button.second-btn {
  color: red;
}
```

### 同一元素多重Class
我們也可以在一個元素同時套用數個 class。

舉例來說，若我們有以下的 HTML，
```
<button class="large-btn red-btn">這是多重 Class 的例子。</button>
```
那麼CSS可以如下：
```
.large-btn { 
  width: 150px;
  height; 50px;
  font-size:20px; 
}

.red-btn { 
  color: white; 
  background: red;
}
```

### 屬性選擇器
今天有一html如下：
```
<input type="text">
<input type="button" value="送出">
```

若只想更改input type是button的樣式，則CSS可以這樣設定：

```
input[type="button"] {
  color: red;
}
```

### 偽類選擇器
偽類 (pseudo class) 就是在選已經存在的東西。
#### 錨偽類
在支援 CSS 的瀏覽器中，連結的不同狀態都可以不同的方式顯示。
- :link  /* 還沒訪問 */
- :visited  /* 已訪問 */
- :hover  /* 滑鼠移到上面 */
- :active  /* 已選定 */
```
a:link {color: #FF0000}		
a:visited {color: #00FF00}	
a:hover {color: #FF00FF}	
a:active {color: #0000FF}	
```
#### 第一個與最後一個
- :first-child
- :last-child
```
p:first-child {font-weight: bold;}
p:last-child {font-weight: 300;}
```

#### 第幾個：nth-child(n)
```
p:nth-child(2) {color: red;}
p:nth-child(odd/even) {background: grey;}
```

#### 允許鍵盤輸入的元素焦點：focus
```
input:focus {border-color: blue;}
```