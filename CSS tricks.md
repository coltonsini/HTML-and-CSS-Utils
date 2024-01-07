# CSS Tricks 

This is a list of several tricks found while making new websites for some specific requirements.

## Text decoration animation on Hover

I found this useful to create an animation over the color of the underline line of your text element, the `transition` Property is set to `.3s` but you can use any timing that works for your project. 

*HTML example:*

```html
<p class="object">
    Lorem Ipsum
</p>
```
*CSS example:*

```css
.object{
    text-decoration: underline;
    text-decoration-color: transparent;
    -webkit-text-decoration-color: transparent;
    -moz-text-decoration-color: transparent;
    transition: all .3s ease;
}

.object:hover{
    text-decoration-color: #FFFFFF; /* put your color here */
    -webkit-text-decoration-color: #FFFFFF;
    -moz-text-decoration-color: #FFFFFF;
}
```

## Embed maps Iframe code

This is an inline style to get the embed maps or embed content to mantain a 16/9 aspect ratio across all devices 

*HTML example:*

```html
<div style="padding-bottom:56.25%; position:relative; display:block; width: 100%">
  <iframe width="100%" height="100%"
    src="https://play.viostream.com/iframe/s0m3m3d14?playerKey=s0m3p14y3r"
    frameborder="0" allowfullscreen="" style="position:absolute; top:0; left: 0">
  </iframe>
</div>
```

> 💡 **Feature Note: Important Information**
>
> This is an inline block style you can use a `class` to get the same result.

> [!IMPORTANT]
> Code taken from: https://help.viostream.com/frequently-asked-questions/how-do-i-make-an-iframe-embed-responsive/

## Percent convertion for REM TO PX TO %

This website will allow you to convert your font between several measures used in website development.

> [!NOTE]
> Link to the website content: https://codebeautify.org/percent-to-rem-converter

## Filter for SVG elements to change the main fill color.

This trick works to get an SVG element to covert them into another color once your using a `<img>` tag instead of the regular `<svg>` tag.

*HTML example:*

```html
<img alt="" src="link to your SVG" class="svg-image">
```

*CSS example:*

```css
/* This example get the element to change to the HEX color #00a4d6 */
.svg-image{
    filter: invert(38%) sepia(96%) saturate(1580%) hue-rotate(165deg) brightness(100%) contrast(101%);
}
```

> 💡 **Feature Note: Important Information**
>
> This is a trick that works but is recommended to avoid using `<svg>` elements with the `<img>` tag since you can style an `<svg>` tag easily with the `fill` or `stroke` properties.

> [!NOTE]
> If the SVG isn't black, use the `brightness(0)` and `saturate(100%)` properties at the beginning of the filter CSS to make it work.
> - Link: https://stackoverflow.com/questions/22252472/how-can-i-change-the-color-of-an-svg-element

> [!IMPORTANT]
> Code taken from: https://codepen.io/sosuke/pen/Pjoqqp
> - Remember that you have to visit the website and put your desired color.

## Input range selector styling

This script works to get to show the value of the script on an specific span using the `#value` for the `id` of the span or any label and `#slider` for the `slider id` here's an example bellow 

*HTML example:*

```html
<span> Grade, over: <strong><output id="value"></output> g/t</strong></span>
<input id="slider" type="range" min="0" max="100" value="31" />
```

*Javascript example:*

```javascript
<script>
document.addEventListener("DOMContentLoaded", function() {
    const value = document.querySelector("#value");
    const input = document.querySelector("#slider");
    value.textContent = input.value;
    input.addEventListener("input", (event) => {
        value.textContent = event.target.value;
    });
});
</script>
```

> 💡 **Feature Note: Important Information**
>
> The recommended styling is inside the links found below to get to the different websites used, this works mainly to get the span to show the value of the range selector input.

> [!IMPORTANT]
> Code taken from:
> - https://www.cssportal.com/style-input-range/
> - https://range-input-css.netlify.app
> - https://nikitahl.com/style-range-input-css



