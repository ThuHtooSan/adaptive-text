# adaptive-text
This is a SCSS function that returns a text color (black or white) based on the provided background color by using [W3C's algorithm](https://www.w3.org/TR/AERT/#color-contrast). Simply speaking, this function changes text color based on color contrast.

![Screenshot](screenshot.png?raw=true)

## How to use
1. Copy this function to your `functions.scss` 
	```bash
	$ cat adaptive-text.scss >> functions.scss
	```
2. Import your `functions.scss` 
	```scss
	@use 'functions' as *;
	// or
	@import 'functions';
	```
3. You are ready to use it! 
	Example:
	```scss
	color: adaptive-text(oceanblue);
	```
	Replace `oceanblue` with your element's background color.