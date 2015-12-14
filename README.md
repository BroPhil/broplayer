# BroPlayer
Polymer WebComponent, Extension of HTML5 Video

BroPlayer is an extension of the HTML5 <video> element. 
You are able to disable some parts of the controls, while <video> only lets you disable the controls as once.

You can easily get BroPlayer with bower:
```sh
$ bower install BroPhil/broplayer
```

## Document Markup
Markup for the document in which you are using BroPlayer:
```html
<!doctype html>
<html>
<head>
    <script src="bower_components/webcomponentsjs/webcomponents-lite.min.js"></script>
    <script type="text/javascript" src="bower_components/jquery/dist/jquery.min.js"></script>
    <link rel="import" href="bower_components/paper-slider/paper-slider.html">
    <link rel="import" href="bro-player.html">
</head>
<body>
    ...
</body>
</html>
```

## Getting Started

#### Basic Usage
The most basic way to implement a BroPlayer Element:
```html
  <bro-player src="video.mp4"></bro-player>
```

#### Width and Height
This creates a Video Element with Controls, with a width of 1280px and a height of 720px. The src Attribute is the link to the video file:
```html
  <bro-player width="1280" height="720" src="video.mp4"></bro-player>
```

#### Nested Sources
```html
  <bro-player width="1280" height="720">
      <source src="video.mp4" type="video/mp4">
      <source src="video.mov" type="video/mov">
  </bro-player>
```

## Hiding Controls
The HTML5 video element is only able to display controls or not. But you can't enable/disable only parts of the controls (eg. volumebar, seekbar, playbutton). This is what makes BroPlayer special. In Default, controls are enabled. But you are able to disable every single control easily via an attribute:
```html
  <bro-player width="1280" height="720" src="video.mp4" hide-progressbar></bro-player>
```
Here is a list of possible hiding properties:


Attribute | Description
------------ | -------------
hide-progressbar | Hide the Progressbar
hide-time | Hiding the Time
hide-playpause | Hiding the Play/Pause-Button
hide-volume | Hiding the Volumebar
hide-mute | Hiding the Mute-Button
hide-fullscreen | Hiding the Fullscreen-Button

#### Allowing Contextmenu
By Befault, the right-click on the player is prevented. But you are able to enable the context menu:
```html
  <bro-player width="1280" height="720" src="video.mp4" allow-contextmenu></bro-player>
```

## Styling
You are also able to style BroPlayer.
```html
  <bro-player width="1280" height="720" src="video.mp4" background-color="#FF0000"></bro-player>
```

Here is a list of styling-attributes:

Attribute | Default | Description
------------ | ------------- | -------------
background-color | #000000 | The Background-Color of the Controls
background-opacity | 0.7 | The Opacity of the Controls-Background
foreground-color | #FFFFFF | The ForegroundColor of the Controls
progress-color | #3367D6 | The color of the video progress.
buffer-color | #7BAAF7 | The color of the loaded buffer progress.
