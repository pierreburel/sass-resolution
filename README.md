# Resolution

Sass mixin to target high density screens.  

Demo: [Sassmeister](http://sassmeister.com/gist/fd61ca5e9ebde7996d84)

Compatibility: Sass 3.2+ and LibSass

---

## Install

Download [`_resolution.scss`](https://raw.githubusercontent.com/pierreburel/sass-resolution/master/_resolution.scss) or install with [Bower](http://bower.io/) or [npm](https://www.npmjs.com/):

### Bower

```
bower install sass-resolution
```

### npm

```
npm install sass-resolution
```

---

## Usage

Import `_resolution.scss` and use the `resolution` mixin.

You can set the resolution by using different notations and units : pixel-ratio (`2`, `2x` or `@2x`), dppx (`2dppx`), dpi (`192dpi`), percentage (`200%`) or presets like `retina` (Apple) and `xhdpi` (Android).

You can set the default resolution by changing `$resolution-default`.

### SCSS

```scss
@import "resolution";

.example {
  @include resolution {
    content: "default";
  }
  @include resolution(2dppx) {
    content: "2dppx";
  }
  @include resolution(192dpi) {
    content: "192dpi";
  }
  @include resolution(1.5) {
    content: "1.5";
  }
  @include resolution(3dppx) {
    content: "3dppx";
  }
  @include resolution(2.5) {
    content: "2.5";
  }
  @include resolution(240dpi) {
    content: "240dpi";
  }
  @include resolution(retina) {
    content: "retina";
  }
  @include resolution(hdpi) {
    content: "hdpi";
  }
  @include resolution(xhdpi) {
    content: "xhdpi";
  }
  @include resolution(xxhdpi) {
    content: "xxhdpi";
  }
  @include resolution(3x) {
    content: "3x";
  }
  @include resolution("@3x") {
    content: "@3x";
  }
  @include resolution(150%) {
    content: "150%";
  }
}
```

### CSS

```css
@media (-webkit-min-device-pixel-ratio: 2), (min-resolution: 192dpi) {
  .example {
    content: "default";
  }
}

@media (-webkit-min-device-pixel-ratio: 2), (min-resolution: 192dpi) {
  .example {
    content: "2dppx";
  }
}

@media (-webkit-min-device-pixel-ratio: 2), (min-resolution: 192dpi) {
  .example {
    content: "192dpi";
  }
}

@media (-webkit-min-device-pixel-ratio: 1.5), (min-resolution: 144dpi) {
  .example {
    content: "1.5";
  }
}

@media (-webkit-min-device-pixel-ratio: 3), (min-resolution: 288dpi) {
  .example {
    content: "3dppx";
  }
}

@media (-webkit-min-device-pixel-ratio: 2.5), (min-resolution: 240dpi) {
  .example {
    content: "2.5";
  }
}

@media (-webkit-min-device-pixel-ratio: 2.5), (min-resolution: 240dpi) {
  .example {
    content: "240dpi";
  }
}

@media (-webkit-min-device-pixel-ratio: 2), (min-resolution: 192dpi) {
  .example {
    content: "retina";
  }
}

@media (-webkit-min-device-pixel-ratio: 1.5), (min-resolution: 144dpi) {
  .example {
    content: "hdpi";
  }
}

@media (-webkit-min-device-pixel-ratio: 2), (min-resolution: 192dpi) {
  .example {
    content: "xhdpi";
  }
}

@media (-webkit-min-device-pixel-ratio: 3), (min-resolution: 288dpi) {
  .example {
    content: "xxhdpi";
  }
}

@media (-webkit-min-device-pixel-ratio: 3), (min-resolution: 288dpi) {
  .example {
    content: "3x";
  }
}

@media (-webkit-min-device-pixel-ratio: 3), (min-resolution: 288dpi) {
  .example {
    content: "@3x";
  }
}

@media (-webkit-min-device-pixel-ratio: 1.5), (min-resolution: 144dpi) {
  .example {
    content: "150%";
  }
}
```
