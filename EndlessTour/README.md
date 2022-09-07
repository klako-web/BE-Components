# EndlessTour

This is the documentation for ``EndlessTour`` and ``EndlessTourPro``.

![Icon](./assets/iconTour.jpg) &nbsp; &nbsp; &nbsp; &nbsp;
![IconPro](./assets/iconTourPro.jpg)

## Use Cases
Onboard your user to your app. Provide guidance for UI elements on your page in a step-by-step, interactive tour.

>**Disclaimer**: This component is not released for productive use yet. No warranties!

## General usage
- Place the component somewhere on a page. There will be no visible reflection in the preview. Don't worry.
- Fill the ``Id`` property in the side panel. Otherwise, you will not be able to work with actions
- To trigger 

<br>

## Actions
For each nocode-block of an action, you have to select the ``Id`` of the custom component instance, which you placed on the page.

### Show
This action is exposed via a Backendless Codeless Block. See **General usage** for an example. The block parameter has to be set to the ``Id`` of a component instance on a specific page.

<br>

## Properties

### Title
The text to be shown as popup title. The **Pro-version** supports HTML.



![Class configuration](./assets/classes.png)



## Animations
(**Pro-version only**)


<br>

## Reused libraries and components
This product includes the following external code libraries/components, which are not owned by the author of ``EndlessPopup`` and ``EndlessPopupPro``:

- [Sweetalert2](https://sweetalert2.github.io/). Licensed under the [MIT License](https://github.com/sweetalert2/sweetalert2/blob/main/LICENSE).