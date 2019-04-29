# a

### a

<hr>

`<a>` is an inline element, and may enclose paragraph, table, or even whole section. But, there should be no interactive content (buttons or other links) inside the `<a>`.

### Attributes

<hr>

-   download = Specify that the target will be downloaded

    -   `<a href="/images/imagefile.jpg" download> download </a>`

    -   `<a href="http://abc.com/files/myfile.pdf" download="filename"> download </a>`

<br>

-   href = "URI": URI of the link goes to

    -   `<a href="https://www.google.com">google</a>`

<br>

-   hreflang = "language code": Specify the language of the linked

    -   `<a href="https://www.google.com" hreflang="en">google</a>`

<br>

-   rel = "link type": Specify the relationship between current page and linked page

    -   `<a rel="" href="http://www.google.com/">google</a>`

        -   rel = alternate | author | bookmark | external | help | license | next | nofollow | noreferrer | noopener | prev | search | tag

<br>

-   tabindex = "Tab Move Order": Tabindex attribute specifies the tab order (between 0 ~ 32767.) of an element.

    -   `<a href="http://google.com" tabindex="1">google</a>`

<br>

-   target = "Frame name": Specify where to open the linked document

    -   `<a href="https://www.google.com" target="_blank">google</a>`

        -   target = \_blank | \_self | \_parent | \_top | framename

<br>

-   href = "mailto: "

    -   `<a href="mailto:abc@gmail.com">abc@gmail.com</a>`

<br>

-   href = "tel: "

    -   `<a href="tel:123-456-7890">123-456-7890</a>`

<br>

-   href = "#"

    -   `<a href = "#">` move to the top

    -   `<a href = "#header">` move to #footer, #contents (ID only available)
