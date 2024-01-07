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

https://codebeautify.org/percent-to-rem-converter
