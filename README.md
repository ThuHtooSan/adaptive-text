# adaptive-text
This is a SCSS function that returns a text color (black or white) based on the provided background color by using [W3C's algorithm](https://www.w3.org/TR/AERT/#color-contrast). Simply speaking, this function changes text color based on color contrast.

![Screenshot](screenshot.png?raw=true)

## How to use
1. Copy the function to your `functions.scss` 

	```bash
	$ sed -n '/@function/,$p' adaptive-text.scss >> functions.scss
	```
2. Load required modules to your `functions.scss`

	```bash
	$ sed -n '/@use/,/@use/p' adaptive-text.scss | cat - functions.scss > /tmp/out && mv /tmp/out functions.scss
	```
3. Import your `functions.scss` 

	```scss
	@use 'functions' as *;
	// or
	@import 'functions';
	```
4. You are ready to use it!

	Example:

	```scss
	@each $key, $val in $some-color-map {
		.bg-#{$key} {
			background: $val;
			color: adaptive-text($val);
		}
	}
	```