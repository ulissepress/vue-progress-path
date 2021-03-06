# vue-progress-path

[![npm](https://img.shields.io/npm/v/vue-progress-path.svg) ![npm](https://img.shields.io/npm/dm/vue-progress-path.svg)](https://www.npmjs.com/package/vue-progress-path)
[![vue2](https://img.shields.io/badge/vue-2.x-brightgreen.svg)](https://vuejs.org/)

Progress bars and loading indicators that can take any form!

> This library is Work In Progress.

[Live Demo](https://akryum.github.io/vue-progress-path/)

<p>
  <a href="https://www.patreon.com/akryum" target="_blank">
    <img src="https://c5.patreon.com/external/logo/become_a_patron_button.png" alt="Become a Patreon">
  </a>
</p>

## Sponsors

### Silver

<p align="center">
  <a href="https://vueschool.io/" target="_blank">
    <img src="https://vueschool.io/img/logo/vueschool_logo_multicolor.svg" alt="VueSchool logo" width="200px">
  </a>
</p>

## Installation

```
npm i -S vue-progress-path
```

```
yarn add vue-progress-path
```

## Usage

```js
import 'vue-progress-path/dist/vue-progress-path.css'
import VueProgress from 'vue-progress-path'

Vue.use(VueProgress, {
  // defaultShape: 'circle',
})
```

You can now use the `<loading-progress>` component.

## CSS customization example

You can customize the progress components with CSS:

```css
.vue-progress-path path {
  stroke-width: 12;
}

.vue-progress-path .progress {
  stroke: red;
}

.vue-progress-path .background {
  stroke: #edd;
}
```

## Examples

Google Material Design-like spinner:

```html
<loading-progress
  :progress="progress"
  :indeterminate="indeterminate"
  :counter-clockwise="counterClockwise"
  :hide-background="hideBackground"
  size="64"
  rotate
  fillDuration="2"
  rotationDuration="1"
/>
```

Semi-circle:

```html
<loading-progress
  :progress="progress"
  :indeterminate="indeterminate"
  :counter-clockwise="counterClockwise"
  :hide-background="hideBackground"
  shape="semicircle"
  size="64"
/>
```

Custom SVG path:

```html
<loading-progress
  :progress="progress"
  :indeterminate="indeterminate"
  :counter-clockwise="counterClockwise"
  :hide-background="hideBackground"
  shape="M10 80 C 40 10, 65 10, 95 80 S 150 150, 180 80"
  size="180"
  fill-duration="2"
/>
```
