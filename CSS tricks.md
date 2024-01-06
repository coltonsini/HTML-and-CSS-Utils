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
