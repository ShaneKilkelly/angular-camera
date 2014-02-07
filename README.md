# Angular Camera Directive

An Angular directive for easily taking pictures from your webcam.

This fork of the [original Angular Camera Directive](https://github.com/onemightyroar/angular-camera) will adapt to the resolution and aspect ratio of the devices camera.

## Getting started

1. Install via Bower using `bower install angular-camera`
2. Load the `omr.directives` module in your application: `angular.module('app', ['omr.directives']);`

## Using ngCamera

```html
<ng-camera
  type="photo"
  enabled="true"
  countdown="3"
  ng-model="media"
  overlay-src="http://example.com/photo-frame.png"
  capture="callback(media)"
  capture-message="Go!"></ng-camera>
```

### Options
* `type` _string_ Type of media the capture (photo, video, gif). Photo is currently the only one supported
* `enabled` _boolean_ Enables or disables the stream by turning on/off webcam access
* `countdown` _integer_ Countdown time in seconds. Zero is replaced with `capture-message` text.
* `ng-model` _object_ Scope variable to data-bind resulting Base64-encoded image
* `overlay-src` _string_ Optional. Reference to image frame to overlay onto media. Automatically resizes to fit canvas.
* `capture` _function_ Callback for "Take Picture" button for use in parent scope. Passes Base64-encoded output as parameter
* `capture-message` _string_ Optional. Text to show during countdown instead of "0" 

_Built by [Zach Dunn](https://github.com/zachdunn) from work on the [Robin Platform](http://getrobin.com)_ (altered slightly by [Shane Kilkelly](https://shanekilkelly.net))
