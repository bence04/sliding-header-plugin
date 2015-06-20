# A vanilla JavaScript plugin to slide headers when a page is scrolled

This plugin uses no libraries, like jQuery, and relies on pure JavaScript and a CSS class to work.
Use it to hide an element on your page, for example a header, when scrolling your page down, but show it up again when scrolling up.
It's called 'sliding-header-plugin' but you can customize it to perform a different animation.

Inspired in [this fiddle](http://jsfiddle.net/edwardomni/D58vx/4/)



## How to use
Load the slidingHeader.js file into your page, and create a new instance of SlidingHeader on the bottom of your body.
Then pass an object with the following properties:
* element: this is your target element (required)
* class: custom class name used to hide the element (optional. Defaults to 'to_scroll')

```javascript
<script src="js/slidingHeader.js"></script>	
<script>
	var slidingHeader = new SlidingHeader({
		element: 'header',
		class: 'scrolled'
	});
</script>
```

You also need to define a class in your css file that hides the element. This will be used by the plugin to add/remove it from the target element (default name is 'to_scroll'). 
```css
.scrolled {
	transform: translateY(-100%);
}
```