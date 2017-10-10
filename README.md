# pilot-bootstrap
Pilot is modern HTML and CSS framework for prototyping responsive, mobile first projects on the web  

## Base  
* For consistency we are using 8pt grid system  
* Root font size is browser default of 16px (you can scale the site by modifying root font size)  
* Base font size is 1x (16px) based on root size and it's line height is 1.5x (24px) based on base font size  
* Base SVG width and height must equal to base font line height (24px)  
* For vertical spacing we only use top margin that is based on it's font size (1em)
* For horisontal spacing we are using root font size (1rem) or it's content components specific font size (1em)  

## Adding/Creating new icons (SVG)  
1) Text and stroke elements must be outlined  
2) Use rect over line element  
3) Keep icons consistent  
4) Artboard (viewbox) must be 24x24px.  
5) Clean up generated SVG code (remove unneeded styles, classes, id's etc.). [svgo](https://www.npmjs.com/package/svgo)  
6) Add prefixed classes for CSS.  
7) Sprite SVG's with unique ID's  

## Images  
* Image sizes based on 8pt grid system (only sizes you will need based on width: 512px, 1024px, 2048px)  
* Image ratios based on 8pt grid system (only ratios you will need: 1:1, 2:1, 9:6)  
* File types: inlcude webp, optimize png/jpg files  
* Use picture element to include image with correct sizes  
* picture with picture class has modifiers that can be used to add image placeholder to avoid unnecessary content shiftment.  

### Example  
```
<picture class="picture">  
    <source srcset="assets/cover_2048.webp" media="(min-width: 1024px)" type="image/webp">  
    <source srcset="assets/cover_2048.jpg" media="(min-width: 1024px)" type="image/jpeg">  
    <source srcset="assets/cover_1024.webp 1x, assets/cover_2048.webp 2x" media="(min-width: 512px)" type="image/webp">  
    <source srcset="assets/cover_1024.jpg 1x, assets/cover_2048.jpg 2x" media="(min-width: 512px)" type="image/jpeg">  
    <source srcset="assets/cover_512.webp 2x, assets/cover_1024.webp 2x" type="image/webp">  
    <source srcset="assets/cover_512.jpg 2x, assets/cover_1024.jpg 2x" type="image/jpeg">  
    <img src="assets/cover_1024.jpg" alt="cover">  
</picture>  
```


## UI   
There are few rules that gets applied across the whole UI.  
* [Material: Metrics & keylines](https://material.io/guidelines/layout/metrics-keylines.html#metrics-keylines-ratio-keylines)
* [8pt Material Design GUI Templates](https://medium.com/@_bklmn/8pt-gui-templates-ed8798badab3)  
* [Intro to The 8-Point Grid System](https://builttoadapt.io/intro-to-the-8-point-grid-system-d2573cde8632)  
* [8-Point Grid: Borders And Layouts](https://builttoadapt.io/8-point-grid-borders-and-layouts-e91eb97f5091)  


## General  
2) Nothing is allowed to overflow outside it's component (components have overflow: hidden applied).  
3) The quality of images should not be compromised by stretching them beyond 100%.  
4) Images have certain ratio's dictated by the parent components (avoiding extra rendering and content shift while images are being loaded).  

## Images  
### Ratios  
Allowed image ratios: 1:1, 2:1, 9:6  

### Resolutions  
Required image width's: 512, 1024, 2048  

### Picture
Small component that can be found also in some of the components. By default it displays images on 9:6 ratio but can be changed by using modifier classes.  

## Components  
Only way you should modify components are:  
1) CSS variables made available by the component  
2) Helper classes  
3) Component specific modifier classes  

