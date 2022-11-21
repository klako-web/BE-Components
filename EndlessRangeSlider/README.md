# Endless Range Slider

This is the documentation for the UI component ***Endless Range Slider*** for the [Backendless Full Stack Visual App Development Platform](https://backendless.com).

<center>

![Icon](./assets/Icon.jpg)

</center>

## Use Cases
Select one value or a range of values with a slider.

![sample](./assets/sample2.png)

![sample](./assets/sample3.png)

![sample](./assets/sample1.png)

<br>

>**Disclaimer**: No support will be provided for this free version!

<br>

## General usage
Place the component on a page. It is recommended to wrap it by a block component to be able to adjust width, padding and margins.

<br>

## Properties

### Range Selector

### Show Tooltip(s)

### Show Tick Marks

### Tick Values

### Show Labels

### Initial Selection

<br>

## Actions

### Set Enabled Status

### Get Selected Values

### Set Selection Values

<br>

## Events

### On Change

<br>

## Styles
Create a theme extension and change any of the following less-variables (default setting as indicated):

```less
@el-range-slider-fontFamily: Roboto, sans-serif;
@el-range-slider-fontSize: 0.8em;
@el-range-slider-fontColor: @appTextColor;
@el-range-slider-fontWeight: normal;

@el-range-slider-bar-color: #eee;
@el-range-slider-bar-selected-color: @buttonContainedBackground;
@el-range-slider-bar-disabled-color: @disabledColor;
@el-range-slider-bar-height: 10px;  

@el-range-slider-pointer-color: #fff;
@el-range-slider-pointer-width: 1.9em;   
@el-range-slider-pointer-height: 1.3em;  
@el-range-slider-pointer-borderRadius: 4px; 
@el-range-slider-pointer-marginTop: 0;

@el-range-slider-scale-marginTop: 10px;  

@el-range-slider-tooltip-fontSize: 0.9em;
@el-range-slider-tooltip-fontColor: @appTextColor;
@el-range-slider-tooltip-fontWeight: bold;
@el-range-slider-tooltip-fontStyle: normal;
@el-range-slider-tooltip-background: @appBackgroundColor;
@el-range-slider-tooltip-border: 1px solid @el-range-slider-bar-selected-color; 
@el-range-slider-tooltip-minWidth: 3.5em;
@el-range-slider-tooltip-width: max-content;
@el-range-slider-tooltip-height: auto;
```

<br>

## Reused libraries and components
This product includes the following external code libraries/components, which are not owned by the authors of ***Endless Range Slider Pro***:

- [range-slider](https://github.com/slawomir-zaziablo/range-slider). Licensed under the [MIT License](https://github.com/slawomir-zaziablo/range-slider/blob/master/LICENSE).
