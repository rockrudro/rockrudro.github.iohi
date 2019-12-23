
##  CopyPasteJS

This a small JS library to execute clipboard functions in a fast and easy way.

See the demo here: [https://assisfery.github.io/CopyPasteJS/index.html](https://assisfery.github.io/CopyPasteJS/index.html)

CND repository: https://www.jsdelivr.com/package/gh/assisfery/CopyPasteJS

[![](https://data.jsdelivr.com/v1/package/gh/assisfery/CopyPasteJS/badge)](https://www.jsdelivr.com/package/gh/assisfery/CopyPasteJS)


### Get Start
Just import the  **src/CopyPasteJS.js**  file in your document.
```html
<script src="src/CopyPasteJS.js"></script>
```

Those file are hosted in CDN JSDelivr.
```html
<script src="https://cdn.jsdelivr.net/gh/assisfery/CopyPasteJS@master/src/CopyPasteJS.min.js"></script>
```

### Copy Text - From Input Element
To copy data from a input element just add  **data-copy-origin="#element"**  attribute to the button.
```html
<button class="btn btn-success" data-copy-origin="#txtCopy">Copy</button>
```

### Copy Text - From Nowhere
To copy text to clipboard  **data-copy-text="text"**  attribute to the button.
```html
<button class="btn btn-success" data-copy-text="Some text">Copy</button>
```

### Paste Text
To paste data to a input element just add  **data-paste-target="#element"**  attribute to the button.
```html
<button class="btn btn-success" data-paste-target="#txtPaste">Paste</button>
```

### Cut Text
To cut data from a input element just add  **data-cut-origin="#element"**  attribute to the button.
```html
<button class="btn btn-success" data-cut-origin="#txtCut">Cut</button>
```

### Copy and Paste Text
To copy and paste data from a input element to another just add  **data-copy-origin="#element"**  and  **data-paste-target="#element"**  attributes to the button.
```html
<button class="btn btn-success"
data-copy-origin="#txtCopy2"
data-paste-target="#txtPaste2">Copy and Paste</button>
```

### Copy Callback function
After data is been copied if you want to execute a function just add  **data-copy-callback="jscode()"**  attribute to the button.
```html
<button class="btn btn-success" data-copy-origin="#txtCopy3" data-copy-callback="alert('copied')">Copy and Callback</button>
```

### Paste Callback function
After data is been pasted if you want to execute a function just add  **data-paste-callback="jscode()"**  attribute to the button.
```html
<button class="btn btn-success" data-paste-target="#txtPaste3" data-paste-callback="alert('pasted')">Paste and Callback</button>
```

### JavaScript Utils
You can do all those actions in JavaScript code.

#### Copy Text in JavaScript
```js
CopyPasteJS.copyText("Text copied in JS");
```

#### Copy Text in JavaScript and Callback Function
```js
CopyPasteJS.copyText("Text copied in JS and Callback triggered", function(){
	alert("Yes its done");
});
```

#### Copy Value From Element in JavaScript
```js
CopyPasteJS.copyFrom("#txtCopy4");

// OR USE CALLBACK
CopyPasteJS.copyFrom("#txtCopy4", function(){
	alert(123);
});
```

#### Paste To Element in JavaScript
```js
CopyPasteJS.pasteTo("#txtPaste4");

// OR CALL A FUNCTION
CopyPasteJS.pasteTo("#txtPaste4", function(){
	alert("I fell amazing");
});
```