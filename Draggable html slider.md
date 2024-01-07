# Horizontal Click and Drag Scrolling with JS

This is an example to get a container with several horizontal items to work with a mouse drag action

## Explanation

I found this useful to create a draggable component in HTML for several uses, like a custom shop scrolling list.

*HTML example:*

```html
<div class="objects-container">
    <!-- Your content goes here -->
    <div class="object"></div>
</div>
```

*CSS example:*

```css
.objects-container{
  display: flex;
  flex-direction: row;
  overflow-x: scroll;
  -ms-overflow-style: none;
  scrollbar-width: none;
  cursor: pointer;
  transition: all .3s ease;
}

.objects-container.active {
  cursor: grabbing;
  cursor: -webkit-grabbing;
  transform: scale(1.01);
}

.object{
  width: 247px;
  min-width: 247px;
}
```

> [!TIP]
> There's two important things about this horizontal scrollbar.
> - The first one is that the container of each object needs to have a `width` and `min-width` property settled down.
> - The second one is that you can take away the property `transform` away since that is going to increase the size of the container once you grab the element.

*Javascript example:*

```javascript
function slideProduct() {

  const slider = document.querySelector(".objects-container");
  let isDown = false;
  let startX;
  let scrollLeft;

  slider.addEventListener("mousedown", (e) => {
    isDown = true;
    slider.classList.add("active");
    startX = e.pageX - slider.offsetLeft;
    scrollLeft = slider.scrollLeft;
  });
  slider.addEventListener("mouseleave", () => {
    isDown = false;
    slider.classList.remove("active");
  });
  slider.addEventListener("mouseup", () => {
    isDown = false;
    slider.classList.remove("active");
  });
  slider.addEventListener("mousemove", (e) => {
    if (!isDown) return;
    e.preventDefault();
    const x = e.pageX - slider.offsetLeft;
    const walk = (x - startX) * 3;
    slider.scrollLeft = scrollLeft - walk;
  });
}

document.addEventListener("DOMContentLoaded", slideProduct);
```

> [!IMPORTANT]
> Code taken from: https://codepen.io/thenutz/pen/VwYeYEE
