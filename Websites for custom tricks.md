# Websites for custom tricks

This is a compilation with different websites to get some different type of interactions or styled components that are uncommon.

## Generator for custom CSS borders

I found this useful to create custom CSS borders for your custom HTML elements.

*CSS example for the first example:*

```css
.element{
	--mask: radial-gradient(40px at 40px 40px,#0000 98%,#000) -40px -40px;
	-webkit-mask: var(--mask);
	mask: var(--mask);
}
```

*CSS example for the second example:*

```css
.element{
	clip-path: polygon(52% 0, 0% 100%, 100% 100%);
}
```

> [!NOTE]
> There's two different websites to get edit the borders of your element.
> - First one: https://css-generators.com/custom-corners/
> - Second one: https://bennettfeely.com/clippy/

## Website with different custom tricks

> [!NOTE]
> Link to the website: https://dev.to/lissy93/super-useful-css-resources-1ba3

## Get NavIcon image

This script will help you to get the NavIcon image of any website that you are looking for, you just need to add your link and use it over the website console.

```javascript
if (!empty($comment->comment_author_url)) {
  $url = preg_replace('/^https?:\\/\\//', '', $comment->comment_author_url);
  if ($url != "") {
    $imgurl = "https://www.google.com/s2/favicons?domain=" . $url;
    echo '![](' . $imgurl . ')';
  }
}
```

> [!IMPORTANT]
> Remember to put your desired URL right next to the `domain=` code line.

> [!NOTE]
> Link to the website: https://www.labnol.org/internet/get-favicon-image-of-websites-with-google/4404/
