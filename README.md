# pilot-bootstrap
Pilot is modern HTML and CSS framework for prototyping responsive, mobile first projects on the web

## UI  
### Design as a whole is greater than sum of it's parts  
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

## Icons (SVG)  
1) Text elements must be outlined  
2) Use rect over line element  
3) Keep icons consistent    
4) Artboard (viewbox) height must follow power of 8 rule and should match with the rest of icons (ala ...x24px).
5) Clean up generated SVG code (remove styles, classes, id's etc. that isn't needed otherwise it might affect the rest of the site or quality).  
6) Add prefixed classes for CSS.  
7) Sprite SVG's with unique ID's  