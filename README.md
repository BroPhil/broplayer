# BroPlayer
Polymer WebComponent, extending HTML5 Video

BroPlayer is based on the HTML5 video element. 
You can disable some parts of the controls, while HTML5-video only lets you disable the controls as once.

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
    <script type="text/javascript" src="bower_components/webcomponentsjs/webcomponents-lite.min.js"></script>
    <script type="text/javascript" src="bower_components/jquery/dist/jquery.min.js"></script>
    <script type="text/javascript" src="bower_components/velocity/velocity.min.js"></script>
    <link rel="import" href="bower_components/broplayer/bro-player.min.html">
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
The HTML5 video element is only able to display controls or not. But you can't enable/disable only parts of the controls (eg. volumebar, seekbar, playbutton). This is what makes BroPlayer special. By Default, controls are enabled. But you are able to disable every single control easily via an attribute:
```html
  <bro-player width="1280" height="720" src="video.mp4" hide-progressbar></bro-player>
```
Here is a list of possible hiding properties:


Attribute | Description
------------ | -------------
hide-progressbar | Hide the progressbar
hide-time | Hiding the time
hide-playpause | Hiding the play/pause-button
hide-volume | Hiding the volumebar
hide-mute | Hiding the mute button
hide-fullscreen | Hiding the fullscreen button

#### Allowing Contextmenu
By Befault, the right-click on the player is prevented. But you are able to enable the context menu:
```html
  <bro-player width="1280" height="720" src="video.mp4" allow-contextmenu></bro-player>
```

Attribute | Description
------------ | -------------
allow-contextmenu | Allowing right-click contextMenu on the video

## Styling
You are also able to style BroPlayer.
```html
  <bro-player width="1280" height="720" src="video.mp4" background-color="#FF0000"></bro-player>
```

Here is a list of styling-attributes:

Attribute | Default | Description
------------ | ------------- | -------------
background-color | #000000 | The background color of the controls
background-opacity | 0.7 | The opacity of the controls background
foreground-color | #FFFFFF | The foreground color of the controls
progress-color | #3367D6 | The color of the video progress
buffer-color | #7BAAF7 | The color of the loaded buffer progress

## Errors
The default HTML5 video tag does not show an error if the video source can't be played. It only shows an error message, if the browser doesn't support the video tag. BroPlayer displays an error if none of the sources can be played. You can set this error message on your own in your own language if you want:

```html
  <bro-player width="1280" height="720" src="video.mp4" no-video="Video konnte nicht geladen werden"></bro-player>
```

Attribute | Default | Description
------------ | ------------- | -------------
no-video | "Cannot open source" | The error message which will be displayed when the player can't play any source.
