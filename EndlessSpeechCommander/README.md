# Endless Speech Commander

This is the documentation for the UI component ***Endless Speech Commander*** for the [Backendless Full Stack Visual App Development Platform](https://backendless.com).

<center>

![Icon](./assets/icon.jpg)

</center>

## Use Case
Developers can create apps where users can issue commands verbally via the device microphone.

## Technical Setup and Restrictions
>>**Please read this carefully!**

+ ***Speech Commander*** is connecting to a remote service provider which is providing the actual service of speech-to-text recognition. Therefore, ***Speech Commander*** requires an active internet connection. It will not work offline. Due to the remote communication, voice speed depends on the available communication bandwidth and server provider processing capacities. Don't try to build apps with ***Speech Commander*** which require real-time speech processing.
+ Multiple service providers are supported. If a user triggers voice regognition, voice data is sent over the internet to servers of the selected service provider. These servers can be located in a different country than the actual user. To comply with your local data protection regulations, you might need to take some measures, like informing your users about this data transfer. Please check, whether you can comply to your local data protection laws before buying ***Speech Commander***. 
+ Currently, the following service providers are supported:
   + Native
   + [speechly.com](https://speechly.com)

### **Native** service provider
This setting leverages the [Web Speech API](https://developer.mozilla.org/en-US/docs/Web/API/Web_Speech_API) of the browser. This means, it depends on the current browser which capabilities are available and to which servers speech data is sent. [Web Speech API](https://developer.mozilla.org/en-US/docs/Web/API/Web_Speech_API) is not (fully) supported by all browsers. There are three levels of support:
- fully supported (e.g. Chrome on Desktop)
- no support for continuous listening (e.g. Chrome on Android)
- no support at all (e.g. Firefox)

You should test the current browser coverage, as this evolves over time. To get the supported feature of a browser, use the action ``getStatus``.

Although the browser support range for the native service provider is limited, there is a broad range of languages which are supported.

### **speechly.com** service provider
Visit [speechly.com](https:speechly.com) to learn about the free and paid offerings. With speechly.com, ***Speech Commander** works on almost all browser. However, language support is currently limited to English and Finnish. You need to create a speechly account to get an AppId. You need to enter this AppId as a UI Component Setting for your Backendless App.

<br>

## General usage
Place the component on a page. There will be no visible reflection in the preview or in the published app. This component only exposes actions and events.

<br>

## Properties

### Commands
..

### Show Transcript
.

### Fuzzy Match
.

### Fuzzy Threshold
.

### Provider
.

<br>

## Actions

### Start
The speech recognition process is started.

### Stop
.

### Get Transcript
.

### Reset Transcript
.

### Get Status
.

<br>


## Events

### On Result
.

### On Listening Change
.

### On Error

<br>

## Support
No support guarantee is provided for this free version! You can [open an issue](https://github.com/klako-web/Endless-Components/issues/new) though and assign the label ``speechCommander``.

## Reused libraries and components
.
