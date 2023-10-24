
- [ ] :has()选择器如何与+（相邻兄弟选择器）及~（通用兄弟选择器）相结合 (@2023-10-25) 

html:
```html
<div class="box"></div>
<div class="box"></div>
<div class="box"></div>
<div class="circle"></div>
<div class="rect"></div>
<div class="circle"></div>
<div class="circle"></div>
```
css:
```css
.box:has(~ .box + .circle){
	width:100px;
	border:2px solid #09f;
}
```

这段css最终的效果是除了和`.circle`相连接的兄弟之外，`.circle`之前的所有`.box`元素都被选中