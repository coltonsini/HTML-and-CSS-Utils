# Animate CSS Library 

## This script will do the job when you need to get the animations of animate.css library to repeat each time a scroll is made vertically and appears on the viewport.

To import the library for your animations, you should use in the `<header>` tag of your html file. 
```html
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/animate.css/4.1.1/animate.min.css"/>
```

This script will get your animations to work on scroll and repeatedly.

```javascript
const animatedElements = document.querySelectorAll(".animate__animated");
	const observer = new IntersectionObserver((entries) => {
		entries.forEach((entry) => {
			const animationName = entry.target.dataset.animation;
			if (entry.isIntersecting) {
				entry.target.classList.add(animationName, "animated");
			} else {
				entry.target.classList.remove(animationName, "animated");
			}
		});
	});
	animatedElements.forEach((element) => {
		observer.observe(element);
	});
```
    
Another way to do it 

```javascript
const animatedElements = document.querySelectorAll('.animate__animated');

animatedElements.forEach(element => {
  const animationName = element.dataset.animation;
  const elementPosition = element.getBoundingClientRect().top;
  const windowHeight = window.innerHeight;

  if (elementPosition < windowHeight) {
    element.classList.add(animationName, 'animated');
  }
});

window.addEventListener('scroll', () => {
  animatedElements.forEach(element => {
    const animationName = element.dataset.animation;
    const elementPosition = element.getBoundingClientRect().top;
    const windowHeight = window.innerHeight;

    if (elementPosition < windowHeight) {
      element.classList.add(animationName, 'animated');
    } else {
      element.classList.remove(animationName, 'animated');
    }
  });
});
```
    
then you put on your tag a class with the name `animate__animated` and use the following to add your desired animation `data-animation="animate__rotateInDownLeft"`
    
link to the library (https://animate.style)
