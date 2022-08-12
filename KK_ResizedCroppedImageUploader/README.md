# KK_ResizedCroppedImageUploader

## Purpose
- selects an image from local file system, camera, or clipboard
- optionally rotates the image
- optionally crops an area of interest
- optionally saves the image to Backendless file system with reduced size (width, height) and reduced quality (for lossy image formats) and desired image type.

>**Disclaimer**: This component is not released for productive use yet. No warranties!

## General usage
1. Place a Block-UI-component on a page where you want to display the preview of image to be uploaded. Adjust the dimensions and other properties of this Block-component to your needs.
2. Place the custom component KK_ResizedCroppedImageUploader into the Block-component. 
3. Fill the ``Id`` property in the side panel. Otherwise, you will not be able to work with actions.
4. Place buttons on your page and in the respective "On Click Event"-handlers call one of the custom component actions. An example how this can look like is shown here:
![sample](./assets/sample.png)

<br>
<br>

## Actions
For each nocode-block of an action, you have to select the ``Id`` of the custom component instance, which you placed on the page.

### Select Image
*Input parameters:* None

An image selection dialog is shown, which depends on the device. On mobiles, you can typically capture a live camera image in addition to selection an existing image from the device.

*Example*:
![On Click Handler](./assets/select.png)

### Rotate Image
*Input parameters:* 
- ``Degree``: The amount of rotation degrees. Can be a positive or negative number.

*Example*:
![On Click Handler](./assets/rotate.png)


### Zoom In/Out
*Input parameters:* 
- ``Ratio``: The ratio of (de-)magnification . Can be a positive or negative number.

> Note: Zooming-in/out is  just a visual effect. The actual image file size and content is not changed.

*Example*:
![On Click Handler](./assets/zoom.png)


### Save Cropped Image

### Get Cropped Image

### Reset

<br>
<br>

## Properties

### Title
The text to be shown as popup title. Can be HTML.

### Content
The text to be shown as popup content. Can be HTML.


## Styling

<br>
<br>

## Reused libraries and components
This product includes the following external code libraries/components, which are not owned by the author of ``KK_UploadResizedCroppedImage``:

- [Cropper.js](https://fengyuanchen.github.io/cropperjs/). Licensed under the [MIT License](https://github.com/fengyuanchen/cropperjs/blob/main/LICENSE).