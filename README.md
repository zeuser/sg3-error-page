# sg3-error-page
HTML coded responsive error page template used in Songator3 (eg. 403, 404, 500 and 503 error view)

## How to install

Clone this repository or download it as ZIP

```sh
git clone https://github.com/EllenFawkes/sg3-error-page.git
```
Copy all html template files (exclude `index.html`) and `/css/error` and `/img/error` onto your public html directory or your project.
Now you can setup your server error pages defintions.

## Customizing

### Edit PSD

In `/psd` directory you can found source PSD files.

* `sg3_erropage` - PSD source of page template
* `area.psd` - PSD source of background image in main area (with it you can create own themes)

### Customize theme

In file `/css/error/theme.css` you can customize your own templates.

Example of template definition:

```css
.main-place.purple { /* main-place.<theme-name> */
	background-color: #330433; /* area main color */
	background-image: url('../../img/error/area-purple.jpg'); /* area image */
	text-shadow: 0px 1px 5px #1f021f; /* last parameter is color of shadow in text in area */
	border-bottom-color: #1f021f; /* delimiter color (should be same color as main */
}
```

Apply your theme inside html template:

```html
		<div class="main-place <your-theme-name>">
			<h1>401</h1> <!-- HTTP status code -->
			<h2>
			    <!-- The error message -->
				<span>Unauthorized</span>
				<small>You don't have permissions to view this page.</small>
			</h2>
		</div>
```

### Change logo

```html
<div class="subtext">
			<a href="#"><img src="<your-logo-path>" alt="<alternate-description>"></a> <!-- Put link and logo here -->
			...
```

### Customize error messages

```html
<div class="main-place orange">
			<h1>error code</h1> <!-- HTTP status code -->
			<h2>
			    <!-- The error message -->
				<span>Your error title</span>
				<small>Your error message</small>
			</h2>
		</div>
```

### Customize navigation

You can find navigation inside tag `div class="subtext"`

```html
<div class="navigation">
	<a href="page1.html">Your link 1</a>
	<a href="page2.html">Your link 2</a>
	...
</div>
```

## Credits

SG3 Error Pages created by PurrplingCat

There was no project such as Bootstrap used in this project 
