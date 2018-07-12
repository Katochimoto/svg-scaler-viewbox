<div align="center">
  <a href="https://github.com/webpack/webpack">
    <img width="200" height="200"
      src="https://webpack.js.org/assets/icon-square-big.svg">
  </a>
  <h1>SVG Scaler Loader</h1>
  <p>Scale your svg files</p>
</div>

<h2 align="center">Install</h2>

## Install

```bash
yarn add style-loader --dev
```
or using npm
```bash
npm install style-loader --save-dev
```

<h2 align="center"><a href="https://webpack.js.org/concepts/loaders">Usage</a></h2>

It's recommended to combine `svg-scaler-loader` with the [`@svgr/webpack`](https://github.com/smooth-code/svgr/tree/master/packages/webpack)

**component.js**
```js
import Icon from './icon.svg'
```

**webpack.config.js**
```js
{
  module: {
    rules: [
      {
        test: /\.svg$/,
        use: [
          { loader: '@svgr/webpack' },
          {
            loader: 'svg-scaler-loader',
            options: {
              width: 24,
            }
          }
        ]
      }
    ]
  }
}
```

## Options

### `svgo`

`type:boolean`, default is `false`, if you want optimize with [svgo](https://github.com/svg/svgo), please set it `true`;

### `width`

`type:number`, will make the svg scale to the size by the number, will fix to square, unity all svg files to same size.

### scale

`type:number`, just normal `scale`, but if have the width or the height option, the `scale` will not work.
