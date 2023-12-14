[TOC]
# Rehabnet WordPress theme
## Getting started
Follow these steps to set up and run project locally for development.
### 1) Requirements
- [Node.js 18.7.0](https://nodejs.org/en/)
### 2) Install
Run the `npm install` or `npm i` command to install the dependencies.
### 3) Run the project locally
Run the `npm run dev` command in the terminal.
## Deployment
### Production assets build
Run the `npm run build` command in the terminal.
## Development process
All functional code is located inside root theme folder.
### [GULP](https://gulpjs.com/)
The JavaScript Task Runner.
### [STYLUS](https://stylus-lang.com/)
CSS preprocessor.
#### Variables
Lots of predefined things can be found in the variables file (01_variables.styl):
Font families, typo related definitions like font-sizes, font weights, colors, shadows, spacings, radiuses, breakpoints. 
An example of how to use a color variable:  `color $grayscale60`
##### Utility classes
We used some utility class names like:
`.grid`, `.flex`, `.table`, `.cell`, `.toCenter`
The grid and flex can be use alongside with your custom class names, like: `<div class="grid outerGrid">`
toCenter class name represents the centered contents of the site.
#### Typography
The base definition of the typography can be found inside the 05_1_typography file.
Use the non regular paragraphs with a wrapper div with the following class names: mediumRegular, smallRegular, tinyRegular.
Example:
```html
<div class="smallRegular">
	<p>Lorem Ipsum</p>
</div>
```
For links, use the `link` class name.
#### Icons and buttons
For buttons, use the `button` class name and add the button type to it like `primary`, you can change the size of the button with `large` or `medium` names.
Example:
```html
<a class="button primary large">
	Lorem Ipsum
</a>
```
We can use icons inside the buttons, in this case we have to use a `span` tag inside the button class, first we have to define the icon place with `iconLeft` or `iconRight` class name, then add the icon class name to the `span` tag.
(you can find the icon list inside the 05_2_fonticon file)
##### Adding new icons
For the icons, [Icomoon](https://icomoon.io/) service is used. For login use [this account](https://passmgr.argo22.com/index.php/pwd/view/1097). If only free plan is available (Icomoon does not allow you to save projects in the cloud with the free plan), use the `assets/fonts/Rehabnet.json` file for importing the project.
After you add the desired icons, download all available fonts with the actual project JSON file and update them in git. 
##### Using the icons
Example:
```html
<a class="button primary large iconRight">
	<span class=".icon-arrow-down">Lorem Ipsum</span>
</a>
```
#### Gutenberg blocks on the admin side
Automatically generated from the STYL files, it uses the same css as the front-end.
### Documentation
- keep [`README.md`](./README.md) updated!
- try to document every decision that isn't clear at first glance
### Plugins
You can check the full list of plugins in `plugins-readme.md`.
### Translations
No translations are presented. Website is in english only.
### Happy coding
