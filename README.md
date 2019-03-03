

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

 By doing that, we are telling the image to not to wider than the container or any element it contains. This case is very much valid when a Desktop Image is being shown on mobile devices. In other words, by doing that, the image will never be wider than the width of the view port.

 **Position**
Difference between absolute and relative is that relative will leave the space; however, absolute does not. Also Absolute does not have default width. Also, it would be absolute to the Body of the page not any container.

**Float**
It places an element along the left or right side of its container, allowing other elements to wrap around it.

**clear**
To clear the floating on the element. 



### Responsive Design ###
Designing a webpage that looks good on devices of various sizes and is usable on as many devices as possible.

**Media Query**
Used to modify the CSS of a site depending on qualities such as viewport size or device type.

```
@media(min-width:600px){
    body {
        background-color:blue;
    }
}
```

**Flexbox**
A one-dimensional layout system in CSS

**CSS Grid Layout**
A two-dimensional layout system in CSS. 

We can mix both of these layout technics while creating webpages. For example, using Flexbox in navigation, and for the rest of the mutilcolumn body by CSS Grid system.

**Feature Queries**
Queries which are going to be used if browser does not support any Feature. This is especially the case when 
the end user has older or traditional browser.



### GRID LAYOUT###

```
.container {
    display:grid;
    grid-template-columns: 200px, 300px;
    grid-template-rows : 200px, 50px, 100px;
    grid-gap : 20px;
    grid-row-gap:10px;
    grid-column-gap:10px;
}
```
We can also add sizing of each column we can use "auto"

```
.container {
    grid-template-columns: auto, 100px, auto;
}

```

here auto would split the extra space evenly to first and third column, but it can also make columns of 
uneven size. To fix that, we can use "fr".

FR - Fraction Unit.


```
.container {
    grid-template-columns: 1fr, 100px, 1fr;
}
```
OR

```
.container {
    grid-template-columns: 1fr, 3fr, 9fr;
}
```
Same FR can be set for ROWS as well
  -  grid-template-rows: 1fr, 3fr, 9fr;
