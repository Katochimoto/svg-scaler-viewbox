# SVG Scaler

Scale svg size

## Install

```bash
yarn add style-loader --dev
```
or using npm
```bash
npm install style-loader --save-dev
```

## Usage

```
import SVGTranslator from 'svg-scaler-viewbox';

new SVGTranslator({ width: 24 }).process(`
  <svg xmlns="http://www.w3.org/2000/svg" width="48" height="48">
    <circle cx="24" cy="24" r="24" fill="#D8D8D8"/>
  </svg>
`).then((result) => {
  console.log(result)
});

```

## Options

### `width`

`type:number`, will make the svg scale to the size by the number, will fix to square, unity all svg files to same size.

### scale

`type:number`, just normal `scale`, but if have the width or the height option, the `scale` will not work.

## Warning

* not support image in svg.

## Thanks

* https://github.com/fontello/svgpath
* https://github.com/isaacs/sax-js
