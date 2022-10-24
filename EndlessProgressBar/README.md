# Endless Progress Bar

This is the documentation for the UI component ***Endless Progress Bar*** and ***Endless Progress Bar*** for the [Backendless Full Stack Visual App Development Platform](https://backendless.com).

<center>

![Icon](./assets/IconProgressBar.jpg) &nbsp; &nbsp; &nbsp; &nbsp;
![Icon](./assets/IconProgressBarPro.jpg)

</center>

## Use Cases
Use an animated progress bar to show the progress of a process. The displayed progress is fully under control by you through simple data binding.



https://user-images.githubusercontent.com/69795385/197525821-06ecafb1-4342-4028-9381-196d24fb56c2.mp4



https://user-images.githubusercontent.com/69795385/197525838-64f0a2b7-5da4-4290-b55a-775a5925ea94.mp4



>**Disclaimer**: No support will be provided for the free (non-PRO) version of this component!

## General usage
Place the component on a page where it should appear. It always renderes with 100% width. It is recommended to wrap it by a Block-component to adjust width, heigth, margin, padding, etc.

<br>

## Properties

### Progress
A numerical value which indicates the degree of completion (extent of the progress bar). Use data binding to set and change this value from within your application.

### Percentage
(**Pro-version only**)
If the checkbox is selected (default), the ``Progress``- property is interpreted as a percentage and the %-sign is shown. For the free version, the ``Progress`` is always interpreted as a percentage.

### Max Progress
(**Pro-version only**)
The maximal progress value which can be achieved. Defaults to ``100``.

### Height
(**Pro-version only**)
The height of the progress bar. Can be in any applicable CSS-units (e.g., ``px``, ``em``, ``%``).

### Border Radius
(**Pro-version only**)
The curvature of the progress bar. Can be in any applicable CSS-units (e.g., ``px``, ``em``, ``%``).

### Color
Progress bar color.

### Background
The color of the background not covered by the progress bar.

### Label
(**Pro-version only**)
Instead of the numerical value ``Progress``, any text label can be shown.

### Label Size
The font size of the progress value or of the label.

### Label Color
The font color of the progress value or of the label.

### Label Alignment
(**Pro-version only**)
The label or progress value can be shown within the progress bar at positions ``Left``, ``Right``, ``Center``, or it can be shown ``Outside`` of the entire bar. 

### Duration
(**Pro-version only**)
Numerical value for setting the bar transition duration in seconds.

### Timing Function
(**Pro-version only**)
Affects how the progress bar transitions towards the target progress value.

<br>

## Actions
None.

<br>

## Events
None.

<br>

## Reused libraries and components
This product includes the following external code libraries/components, which are not owned by the authors of ***Endless Progress Bar*** and ***Endless Progress Bar Pro***:

- [react-progress-bar](https://github.com/KaterinaLupacheva/react-progress-bar). Licensed under the [MIT License](https://github.com/KaterinaLupacheva/react-progress-bar/blob/master/LICENSE).
