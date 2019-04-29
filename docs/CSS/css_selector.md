# CSS Selector

### CSS Selector Priority

<hr>

-   \* {} Universal Selector: 0 points

-   body {} Type Selector: 1 point

-   .class {} class selector: 10 points

-   \#id {} ID Selector: 100 points

-   `<p style = "color: red"> Inline Style </hr p>` Inline style: 1000 points

How to apply top level

When the Selector Priority is the same, the style you applied later appears, but if you type !Important, you can create a style that applies to the top level.

### Example

<hr>

```
<style>
            #contentsId {
                background: skyblue;
            }
            .contentsClass {
                background: yellow;
            }
            p {
                background: black;
            }
        </style>
    </head>
    <body>
        <h1>CSS Selectors</h1>

        <p id="contentsId" class="contentsClass">
            Lorem, ipsum dolor sit amet consectetur adipisicing elit. Quaerat
            laudantium iste fugiat tempore, ab autem sequi saepe consequuntur
            quis vel labore blanditiis officia ea eaque similique totam iusto
            quasi architecto?
        </p>
    </body>
```

ID Selector \> class selector \> Type Selector

<img src="https://i.postimg.cc/HLj60GfC/CSS-Selectors.png">

```
<style>
            #contentsId {
                background: skyblue;
            }
            .contentsClass {
                background: yellow !important;    <-------
            }
            p {
                background: black;
            }
        </style>
    </head>
    <body>
        <h1>CSS Selectors</h1>

        <p id="contentsId" class="contentsClass">
            Lorem, ipsum dolor sit amet consectetur adipisicing elit. Quaerat
            laudantium iste fugiat tempore, ab autem sequi saepe consequuntur
            quis vel labore blanditiis officia ea eaque similique totam iusto
            quasi architecto?
        </p>
    </body>
```

\!important \> ID Selector \> class selector \> Type Selector

<img src="https://i.postimg.cc/bYR1vCB0/CSS-Selectors-important.png">

### 1. .class

<hr>

Selects all elements with class="yellow"

```
<style>
    .yellow {
        background-color: yellow;
    }
</style>
</head>
<body>
    <h1>CSS Selectors</h1>

    <div class="yellow">
        <p>highlight1 highlight1 highlight1</p>
        <p>highlight2 highlight2 highlight2</p>
    </div>

    <p>nothing nothing nothing</p>
</body>
```

<img src="https://i.postimg.cc/PxsFd3Rs/CSS-Selectors-class-and-id.png">

### 2. .id

<hr>

Selects the element with id="yellow"

```
<style>
    #yellow {
        background-color: yellow;
    }
</style>
</head>

<body>
    <h1>CSS Selectors</h1>

    <div id="yellow">
        <p>highlight1 highlight1 highlight1</p>
        <p>highlight2 highlight2 highlight2</p>
    </div>

    <p>nothing nothing nothing</p>
</body>
```

<img src="https://i.postimg.cc/PxsFd3Rs/CSS-Selectors-class-and-id.png">

### 3. \*

<hr>

Selects all elements

```
* {
    background-color: yellow;
    }
</style>
</head>

<body>
    <h1>CSS Selectors</h1>
    <div id="yellow">
        <p>highlight1 highlight1 highlight1</p>
        <p>highlight2 highlight2 highlight2</p>
    </div>
    <p>nothing nothing nothing</p>
</body>
```

<img src="https://i.postimg.cc/R0h58DnM/CSS-Selectors.png">

### 4. element (ex. html, body, div, p, a…)

<hr>

Selects all `<html, body, div, p, a...>` elements

```
<style>
    p {
        background-color: yellow;
    }
</style>
</head>

<body>
    <h1>CSS Selectors</h1>

    <div id="yellow">
        <p>highlight1 highlight1 highlight1</p>
        <p>highlight2 highlight2 highlight2</p>
    </div>

    <p>highlight3 highlight3 highlight3</p>
</body>
```

<img src="https://i.postimg.cc/L5TxmmrG/CSS-Selectors-element.png">

### 5. element, element

<hr>

Selects all <h1> elements and all <p> elements

```
<style>
    h1,
    p {
        background-color: yellow;
    }
</style>
</head>

<body>
    <h1>CSS Selectors (highlight0 highlight0 highlight0)</h1>

    <div id="yellow">
        <p>highlight1 highlight1 highlight1</p>
        <p>highlight2 highlight2 highlight2</p>
    </div>

    <p>highlight3 highlight3 highlight3</p>
</body>
```

<img src="https://i.postimg.cc/Kvp5fpF7/CSS-Selectors-element-element.png">

### 6. element element

<hr>

Selects all <p> elements inside <div> elements

```
<style>
    div p {
        background-color: yellow;
    }
</style>
</head>

<body>
    <h1>CSS Selectors</h1>

    <div id="yellow">
        <span>nothing nothing nothing</span>
        <p>highlight1 highlight1 highlight1</p>
        <p>highlight1 highlight1 highlight1</p>
    </div>

    <p>nothing nothing nothing</p>
</body>
```

<img src="https://i.postimg.cc/MKfck9Vm/CSS-Selectors-element-element-1.png">

```
<style>
    div p {
        background-color: yellow;
    }
</style>
</head>

<body>
    <h1>CSS Selectors</h1>

    <div id="yellow">
        <span>nothing nothing nothing</span>
        <p>highlight1 highlight1 highlight1</p>
        <p>highlight2 highlight2 highlight2</p>
        <div>
            <p>highlight3 highlight3 highlight3</p>
        </div>
        <span>
            <p>highlight4 highlight4 highlight4</p>
        </span>
    </div>

    <p>nothing nothing nothing</p>
</body>
```

<img src="https://i.postimg.cc/Zq5BQ4cC/CSS-Selectors-element-element-2.png">

Compare with element > element

### 7. element > element

<hr>

Selects all <p> elements where the parent is a <div> element

```
<style>
    div > p {
        background-color: yellow;
    }
</style>
</head>

<body>
    <h1>CSS Selectors</h1>

    <div id="yellow">
        <span>nothing nothing nothing</span>
        <p>highlight1 highlight1 highlight1</p>
    </div>

    <p>nothing nothing nothing</p>
</body>
```

<img src="https://i.postimg.cc/3xVkcbK2/CSS-Selectors-element-element-1.png">

```
<style>
    div > p {
        background-color: yellow;
    }
</style>
</head>

<body>
    <h1>CSS Selectors</h1>

    <div id="yellow">
        <span>nothing nothing nothing</span>
        <p>highlight1 highlight1 highlight1</p>
        <p>highlight2 highlight2 highlight2</p>
        <div>
            <p>highlight3 highlight3 highlight3</p>
        </div>
        <span>
            <p>nothing nothing nothing</p>
        </span>
    </div>

    <p>nothing nothing nothing</p>
</body>

```

<img src="https://i.postimg.cc/xTdqTS8K/CSS-Selectors-element-element-2.png">

Compare with element element

### 8. element + element

<hr>

Selects all <p> elements that are placed immediately after <div> elements

```
<style>
    div + p {
        background-color: yellow;
    }
</style>
</head>

<body>
    <h1>CSS Selectors</h1>

    <div id="yellow">
        <span>nothing nothing nothing</span>
        <p>nothing nothing nothing</p>
    </div>

    <p>highlight1 highlight1 highlight1</p>
</body>
```

<img src="https://i.postimg.cc/PJJhhTyJ/CSS-Selectors-element-element-1.png">

```
<style>
    span + p {
        background-color: yellow;
    }
</style>
</head>

<body>
    <h1>CSS Selectors</h1>

    <div id="yellow">
        <span>nothing nothing nothing</span>
        <p>highlight1 highlight1 highlight1</p>
        <p>nothing nothing nothing</p>
    </div>

    <p>nothing nothing nothing</p>
</body>
```

<img src="https://i.postimg.cc/C5RyXJMf/CSS-Selectors-element-element-2.png">

### 9. element1 ~ element2

Selects every <p> element that are preceded by a <span> element

```
<style>
    span ~ p {
        background-color: yellow;
    }
</style>
</head>

<body>
    <h1>CSS Selectors</h1>

    <div id="yellow">
        <span>nothing nothing nothing</span>
        <p>highlight1 highlight1 highlight1</p>
        <p>highlight2 highlight2 highlight2</p>
        <div>
            <p>nothing nothing nothing</p>
        </div>
        <span>
            <p>nothing nothing nothing</p>
        </span>
    </div>

    <p>nothing nothing nothing</p>
</body>
```

<img src="https://i.postimg.cc/QMMrcXLb/CSS-Selectors-element-element.png">

### 10. [attribute]

<hr>

Selects all elements with a target attribute

```
<style>
    a[target] {
        background-color: yellow;
    }
</style>
</head>

<body>
    <h1>CSS Selectors</h1>
    <a href="https://www.naver.com">naver</a> <br />
    <br />
    <a href="http://www.daum.net" target="_blank">daum</a> <br />
    <br />
    <a href="http://www.google.com" target="_top">google</a>
</body>
```

<img src="https://i.postimg.cc/9Q79CjgL/CSS-Selectors-attribute.png">

### 11. [attribute=value]

<hr>

Selects all elements with target="\_blank"

```
<style>
    a[target="_blank"] {
        background-color: yellow;
    }
</style>
</head>

<body>
    <h1>CSS Selectors</h1>

    <a href="https://www.naver.com">naver</a> <br />
    <br />
    <a href="http://www.daum.net" target="_blank">daum</a> <br />
    <br />
    <a href="http://www.google.com" target="_top">google</a>
</body>
```

<img src="https://i.postimg.cc/KznQzM9s/CSS-Selectors-attribute-value.png">

### 12. [attribute~=value]

<hr>

Selects all elements with a title attribute containing the word "highlight"

```
<style>
    div[class~="highlight"] {
        background-color: yellow;
    }
</style>
</head>

<body>
    <h1>CSS Selectors</h1>

    <div class="nothing highlight">highlight highlight highlight</div>

    <div class="nothing">nothing nothing nothing</div>

    <div class="highlight">highlight highlight highlight</div>

    <div class="nothing_highlight">nothing nothing nothing</div>

    <p class="highlight">nothing nothing nothing</p>
</body>
```

<img src="https://i.postimg.cc/sgmMVD99/CSS-Selectors-attribute-value.png">

### 13. [attribute|=value]

<hr>

Selects all elements with a lang attribute value starting with "en"

```
<style>
    [lang|="en"] {
        background-color: yellow;
    }
</style>
</head>

<body>
    <h1>CSS Selectors</h1>

    <div lang="en" class="nothing highlight">
        highlight highlight highlight
    </div>

    <div class="nothing">nothing nothing nothing</div>

    <div lang="ko" class="highlight">nothing nothing nothing</div>

    <div class="nothing_highlight">nothing nothing nothing</div>

    <p class="highlight">nothing nothing nothing</p>
</body>
```

<img src="https://i.postimg.cc/MpvCG91P/CSS-Selectors-attribute-or-value.png">

### 14. [attribute^=value]

<hr>

Selects every <div> element whose href attribute value begins with "highlight"

Must start at the same value. (`div[class^="high"]`) also possible.

```
<style>
    div[class^="highlight"] {
        background-color: yellow;
    }
</style>
</head>

<body>
    <h1>CSS Selectors</h1>

    <div class="nothing highlight">
        nothing nothing nothing
    </div>

    <div class="highlight_nothing">highlight highlight highlight</div>

    <div class="highlight">highlight highlight highlight</div>

    <div class="nothing_highlight">nothing nothing nothing</div>

    <p class="highlight">nothing nothing nothing</p>
</body>
```

<img src="https://i.postimg.cc/7hRNtnbh/CSS-Selectors-attribute-value.png">

### 15. [attribute$=value]

Selects every <div> element whose href attribute value ends with "highlight"

Ending value must be the same. (`div[class^="light"]`) also possible.

```
<style>
    div[class$="highlight"] {
        background-color: yellow;
    }
</style>
</head>

<body>
    <h1>CSS Selectors</h1>

    <div class="nothing highlight">
        highlight highlight highlight
    </div>

    <div class="highlight_nothing">nothing nothing nothing</div>

    <div class="highlight">highlight highlight highlight</div>

    <div class="nothing_highlight">highlight highlight highlight</div>

    <p class="highlight">nothing nothing nothing</p>
</body>
```

<img src="https://i.postimg.cc/jSc4GTDB/CSS-Selectors-attribute-value.png">
