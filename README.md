# broplayer
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

## Usage

#### Basic
```html
  <bro-player src="video.mp4"></bro-player>
```

#### Width and Height
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
