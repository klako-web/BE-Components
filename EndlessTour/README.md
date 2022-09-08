# EndlessTour

This is the documentation for ``EndlessTour`` and ``EndlessTourPro``.

![Icon](./assets/iconTour.jpg) &nbsp; &nbsp; &nbsp; &nbsp;
![IconPro](./assets/iconTourPro.jpg)

>**Disclaimer**: This component is not released for productive use yet. No warranties!

<br>

## Use Cases
Onboard your user to your app. Provide guidance for UI elements on your page in a step-by-step, interactive tour showing tooltips for each relevant screen area. Start the below video to see a demo:


https://user-images.githubusercontent.com/69795385/188916715-0b5e0aa4-6fe7-405e-a578-618a7fd7f86a.mp4

<br>

## General usage
- Place the component somewhere on a page. There will be no visible reflection in the preview. Don't worry.
- Fill the ``Id`` property of the component in the side panel. Otherwise, you will not be able to work with actions
- To trigger a tour you have to use the Action ``Start Tour``, for instance within an On-Click-Handler of a button:

![On Click Handler](./assets/onClickHandler.png)

The Action ``Start`` receives the parameter ``Step List`` which must be a list of objects. Each object represents one step of the tour. Each object in the list can contain the following properties:
- ``title`` (optional): The title of the tooltip for a step. Can contain HTML-tags.
- ``anchor`` (optional): The ``Id`` of the HTML-element to which the tooltip shall relate to. Currently, in Backendless UI-Builder, anchors can be assigned to Block-UI-Elements only.Therefore, if you want to show a tooltip for a single UI-element or a group of UI-elements, you have to wrap them by a Block and assign an anchor to this block. If you don't pass the ``anchor``-parameter to  the ``Start``-action, the tooltip will be centered on the page without any relation to a UI-element.
- ``message``: The information you want to convey by the tooltip. Can contain HTML-syntax, for instance, image and link-tags.

<br>

## Actions
For each nocode-block of an action, you have to select the ``Id`` of the custom component instance, which you placed on the page.

### Start
This action is exposed via a Backendless Codeless Block. See section [General usage](#general-usage) for an example. The block parameter has to be set to the ``Id`` of a component instance on the page.

<br>

## Properties

### Classes
Can be used to style the tooltips by entering a CSS-class defined in the Theme-editor of UI-Builder. Only one class is considered for styling. See section [Styling](#styling) for an example.

### Next Step Label
**(Pro-version only)** The text label on the button which triggers the next step of a tour. Can contain HTML-tags. This label can be set by a logic handler or by data binding.

### Previous Step Label
**(Pro-version only)** The text label on the button which returns to the previous step of a tour. Can contain HTML-tags. This label can be set by a logic handler or by data binding.

### Done Label
**(Pro-version only)** The text label on the "Done"-button which is shown for the last step of a tour. Can contain HTML-tags. This label can be set by a logic handler or by data binding.

### Show Step Numbers
The number of the current step is shown in tooltip together with the total number of steps (e.g. "2 of 5").

### Step Number Separator
The word "of" seperating step numbers by default can be changed to support any language. This word can be set by a logic handler or by data binding.

### Show Progress Bullets
The tour progress is shown by a set of clickable bullets.

### Show Progress Bar
The tour progress is shown by a progress bar.

### Keyboard Navigation
**(Pro-version only)** The tour can be stepped through with a keyboard. The arrow-keys and the enter-key can be used.

### Exit On Exc
**(Pro-version only)** The Escape-key (Esc) can be used to exit from the tour at any time.

### Exit on Background Click
**(Pro-version only)** The tour can be exited by clicking outside of the tooltip.

### Don't Show Again
**(Pro-version only)** If this checkbox is set, each tooltip offers the option to not start the tour the next time, even if the ``Start``-action is called. The ``EndlessTour`` stores a cookie on the user's browser, by which it recognizes that the next ``Start``-action shall be ignored. To re-activate the tour, the cookie must be deleted, or its lifetime must be expired.

### Don't Show Again Label
**(Pro-version only)** The label used in the tooltip when offering the option "Don't Show Again". This label can be set by a logic handler or by data binding.

### Don't Show Again Cookie
**(Pro-version only)** The name of the cookie which is created when a user select the "Don't Show Again"-option. The default value is ``tour-dontShowAgain``.

### Cookie Lifetime
**(Pro-version only)** The cookie lifetime in days. The default is ``365``.

<br>

## Styling
(**Pro-version only**)
Create a class in the theme editor of UI-Builder. Enter the name of this class into the ``Classes`-property field of your component instance. The following example shows how to style the tooltip elements:

```css
.tourTooltip {
  .introjs-tooltip-header {
    .introjs-tooltip-title {
      color: blue;
    }
    .introjs-skipbutton {
      color: red;
    }
  }
  .introjs-tooltiptext {
    font-weight: bold;
    font-style: italic;
  }
  .introjs-dontShowAgain label {
    font-size: 12px ;
    color: purple ;
    font-weight: bold ;
  }
  .introjs-bullets ul li a.active {
    width: 20px;
    background: blue;
  }
  .introjs-progress {
    background-color: aquamarine;
    .introjs-progressbar {
      background-color: navy;
    }
  }
  .introjs-helperNumberLayer {
    font-size: 11px;
    color: RebeccaPurple;
  }
  .introjs-button {
    font: 11px/normal sans-serif !important;
    background-color: AntiqueWhite !important;
  }
  .introjs-disabled {
    text-shadow: none !important;
    font: 11px/normal sans-serif !important;
    color: Grey !important;
    background-color: GhostWhite !important;
  }
}
```

<br>

## Restrictions
- The ``Display`` property of a component instance is not evaluated.

## Reused libraries and components
This product includes the following external code libraries/components, which are not owned by the author of ``EndlessPopup`` and ``EndlessPopupPro``:

- [Sweetalert2](https://sweetalert2.github.io/). Licensed under the [MIT License](https://github.com/sweetalert2/sweetalert2/blob/main/LICENSE).
