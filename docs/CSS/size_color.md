# Size and Color

### Size

<hr>

There are size units such as cm, mm, and inch, but typical size units used in CSS are px, em, rem, %.

px is the absolute value, em, rem and \% is the relative value.

The default font size for most browsers is 16px, 1em, 1rem, 100%.

### px

<hr>

px is the pixel unit. 1px means the size of one pixel.

Pixels have relative sizes depending on the device resolution.

```html
<style>
    .fontSize15 {
        font-size: 15px;
    }
    .fontSize30 {
        font-size: 30px;
    }
</style>
</head>

<body>
    <p class="fontSize15">font-size: 15px</p>
    <p class="fontSize30">font-size: 30px</p>
</body>
```

<img src="https://i.postimg.cc/0yjjQNJx/size-px.png">

### em

<hr>

em is the relative unit. Sets the size relative to the inherited or default size.

```html
<style>
    .fontSize1em {
        font-size: 1em;
    }
    .fontSize2em {
        font-size: 2em;
    }
</style>
</head>

<body>
    <p class="fontSize1em">font-size: 1em</p>
    <p class="fontSize2em">font-size: 2em</p>
</body>
```

<img src="https://i.postimg.cc/tCySHT44/size-em1.png">

```html
<style>
    div {
        font-size: 2em;
    }
    .div1 {
        background: skyblue;
        padding: 30px;
    }
    .div2 {
        background: pink;
        width: 500px;
    }
</style>
</head>

<body>
    <div class="fontSize2em div1">
        font-size: 2em
        <div class="fontSize2em div2">font-size: 2em</div>
    </div>
</body>
```

<img src="https://i.postimg.cc/zXXQgvZP/size-em2.png">

### rem

<hr>

rem is based on the size of the top-level element(html). The r in rem means root.

```html
<style>
    div {
        font-size: 2rem;
    }
    .div1 {
        background: skyblue;
        padding: 30px;
    }
    .div2 {
        background: pink;
        width: 500px;
    }
</style>
</head>

<body>
    <div class="fontSize2rem div1">
        font-size: 2em
        <div class="fontSize2rem div2">font-size: 2rem</div>
    </div>
</body>
```

<img src="https://i.postimg.cc/WbvkWqbX/size-rem.png">

### %

<hr>

% is the relative unit. Sets the size relative to the inherited or default size.

```html
<style>
    div {
        width: 50%;
    }
    p {
        width: 50%;
        background-color: yellow;
    }
</style>
</head>
<body>
    <div>
        <p>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Nisi,
            quas quam! In perferendis reiciendis blanditiis aliquid debitis
            ducimus quod sapiente eligendi pariatur! Sunt commodi ratione
            aspernatur tenetur! Impedit, omnis ratione?
        </p>
    </div>
    <p>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Nisi, quas
        quam! In perferendis reiciendis blanditiis aliquid debitis ducimus
        quod sapiente eligendi pariatur! Sunt commodi ratione aspernatur
        tenetur! Impedit, omnis ratione?
    </p>
</body>
```

<img src="https://i.postimg.cc/Rh3Xg6SM/size.png">

### Viewport(vh, vw, vmin, vmax)

<hr>

-   vh, vw

The vh is in hundredths of a height value. For example, if the browser height size is 900px, 1vh means 9px. Similarly, if the width of the viewport is 750px, 1vw is 7.5px.

```html
<style>
    div {
        border: 1px solid #000;
        padding: 0;
    }
    p {
        font-size: 2rem;
        background: skyblue;
        margin: 0;
    }
    .div1 {
        height: 33vh;
        width: 50vw;
    }
</style>
</head>
<body>
    <div class="outer">
        <p class="div1">vh, vw</p>
    </div>
</body>
```

<img src="https://i.postimg.cc/9Qr1VgsL/size-vh-vw.png">

-   vmin, vmax

If vh and vw are always affected by the width and height values of the viewport, vmin and vmax can specify the maximum and minimum values according to the width and height values.

For example, if your browser is 1100px wide and 700px high, 1vmin will be 7px and 1vmax will be 11px. When the width value becomes 800px and the height value becomes 1080px, vmin becomes 8px and vmax becomes 10.8px.

```html
<style>
    div {
        border: 1px solid #000;
        padding: 0;
    }
    p {
        font-size: 2rem;
        background: skyblue;
        margin: 0;
    }
    .div1 {
        height: 50vmax;
        width: 30vmin;
    }
</style>
</head>
<body>
    <div class="outer">
        <p class="div1">vmin, vmax</p>
    </div>
</body>
```

<img src="https://i.postimg.cc/ZRb062Pm/size-vmin-vmax.png">

### Color
