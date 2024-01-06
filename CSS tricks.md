# CSS Tricks 

This is a list of several tricks found while making new websites for some specific requirements.

## Text decoration animation on Hover

I found this useful to create an animation over the color of the underline line of your text element, the `transition` Property is set to `.3s` but you can use any timing that works for your project. 

![HTML5](https://img.shields.io/badge/html5-%23E34F26.svg?style=for-the-badge&logo=html5&logoColor=white)

```html
<p class="object">
    Lorem Ipsum
</p>
```
![CSS3](https://img.shields.io/badge/css3-%231572B6.svg?style=for-the-badge&logo=css3&logoColor=white)

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
