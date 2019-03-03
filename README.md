

## Responsive Layout 
This project is intent to brief you about the responsive layout and css page structuring using CSS FLEXBox and GRID layout. 





### Basic Page Structure

**Viewport**

The visible area of a browser window where a webpage can be displayed.

```
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

"width=device-width"  - Width would be the device width
"initial-scale=1.0"   - One pixel on the screen equal to one device independent pixel. That means the page is not zoomed in or out when the page is loaded.

If you want to stop/restrict user from zooming then you could use following values 
    -   user-scalable
    -   minimum-scale
    -   maximum-scale



**Required CSS**
 - Box sizing : By default padding, margina and border added outside the div. To solve this problem
 we can set the "box-sizing" property to "border-box". 
 *The default box-sizing is "content-box"

 The box-sizing property allows us to include the padding and border in an element's total width and height. If you set box-sizing: border-box; on an element padding and border are included in the width and height.

 To ensure, all the inherited element have the same box-sizing we can add a CSS property.

 ```
 *, *:before, *:after {
     box-sizing : inherit;
 }
 ```  


 **Max-width**
 To make your images responsive, we need to ensure max-width set for the image

 ```
 max-width : 100%;
 ```

 By doing that, we are telling the image to not to wider than the container or any element it contains. This case is very much valid when a Desktop Image is being shown on mobile devices.
