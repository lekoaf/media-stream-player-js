# Media Stream Player JS

[![CI][ci-image]][ci-url]
[![NPM][npm-image]][npm-url]

[ci-image]: https://github.com/AxisCommunications/media-stream-player-js/workflows/CI/badge.svg
[ci-url]: https://github.com/AxisCommunications/media-stream-player-js/actions

[npm-image]: https://img.shields.io/npm/v/media-stream-player.svg
[npm-url]: https://www.npmjs.com/package/media-stream-player

Media-stream-player is a video player built around [media-stream-library-js](https://github.com/AxisCommunications/media-stream-library-js) based
on React. The main idea is to define the video state entirely within specialized
React components for each format (currently RTP H.264 and JPEG, and still images
). The main video player will only handle the intended video state (attached to
handlers) and format.

You can either import the `Player` and use it directly (see the example
application). If you want to build your own customized player, you can look at
the latter component and build your own player, using the `Container`, `Layer`,
and `PlaybackArea` components.

## Structure

## Installation

### As a stand-alone element

If you don't use the player as part of you React app, the easiest way to use it
is to download the `media-stream-player.min.js` file from the [releases](https://github.com/AxisCommunications/media-stream-player-js/releases)
page and include it in your html file as a script:

```html
<script src="media-stream-player.min.js"></script>
```

Then, you can use the `<media-stream-player/>` tag, similar to how you would use
`<video/>` to include a video element, and provide the camera IP as hostname:

```html
<media-stream-player hostname="192.168.0.90" />
```

You can find an example of this under `examples/web-component`.

### As part of your React application

If you want to import the player as a React component into your own code, or use
parts of the player, you'll need to install the package as a dependency. Make
sure you have Node installed on your machine.

Then, to install the package:

```shell
npm install media-stream-player
```

or if you are using yarn:

```shell
yarn add media-stream-player
```

You can find an example of this under `examples/react-app`

## Icons

The icons used are from https://github.com/google/material-design-icons/, which
are available under the Apache 2.0 license, more information can be found on:
http://google.github.io/material-design-icons

The spinner is from https://github.com/SamHerbert/SVG-Loaders, available under
the MIT license.
