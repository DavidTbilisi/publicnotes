---
tags:
  - "#it/ProgrammingLanguages/frameworks"
---

[Example Of Vanila Javascript Plugin](https://github.com/woody180/vanilla-javascript-emoji-picker)

## Questions
- Reset button
- Drag & Zoom reset (როდესაც შემდეგ სურათზე გადადიხარ)


Example For Image Viewer[Jquery Plugin Tutorial](https://learn.jquery.com/plugins/basic-plugin-creation/)

```HTML

<div id="viewer"> 

</div>

```


```javascript

Viewer({
	selector:"#viewer",
	buttons:{
		next:true,
		prev:true,
		rotate_left:true,
		rotate_right:true,
		zoom_in:true,
		zoom_out:true,
		zoom_reset:true,
		fullscreen:true,
		info:true,
	},
	per_page:10,
	api_url:"https://example.com/api", // or folder /home/user/images/
})


```