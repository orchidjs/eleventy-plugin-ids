# eleventy-plugin-ids

@11ty plugin for adding ids to html headings and other elements

```html
<h1>Foo Bar</h1>
```
will become

```html
<h1 id="foo-bar">Foo Bar</h1>
```

## Installation

```
npm install @orchidjs/eleventy-plugin-ids
```

## Basic Usage

Add eleventy-plugin-ids to your .eleventy.js file
```js
module.exports = function(eleventyConfig) {
	//...
	
	const anchors_plugin = require('@orchidjs/eleventy-plugin-ids');
	eleventyConfig.addPlugin(anchors_plugin);
	
	//...
}
```


## Settings

```js
module.exports = function(eleventyConfig) {
	//...
	
	const anchors_plugin = require('@orchidjs/eleventy-plugin-ids');
	eleventyConfig.addPlugin(anchors_plugin,{
		selectors: ['h1','h2','h3','h4','h5','h6'],
		prefix: 'custom-id-prefix-',
		formatter: function(element,existing_ids_array){
			return '--generate-a-custom-id-here-',
		}
	});
	
	//...
}
```
