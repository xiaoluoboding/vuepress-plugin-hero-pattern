# Vuepress Plugin HeroPattern

Register a global `<HeroPattern />` component for VuePress.

This component generate a seemless SVG background pattern.

> This plugin is a adaptor of [hero-pattern](http://www.heropatterns.com/) for VuePress

## See Demo on CodeSandbox

[![Edit vuepress-plugin-hero-pattern](https://codesandbox.io/static/img/play-codesandbox.svg)](https://codesandbox.io/s/musing-surf-twidv?fontsize=14&hidenavigation=1&theme=dark)

## Installation

```bash
yarn add vuepress-plugin-hero-pattern -S
or
npm i vuepress-plugin-hero-pattern -S
```

## Register the plugin

```js
...
module.exports = {
  ...,
  plugins: {
    ['hero-pattern']
  },
  ...
}
...
```

## Usage

> Only background image, you must give the width & height of the element

```vue
<HeroPattern style="width: 240px; height: 80px;" />
```

> With the custom slot, in the case, you can let the slot element control the pattern's height
 ÷
```vue
<hero-pattern>
  <div style="padding: 64px; font-size: 2rem; color: white;">
    All Posts
  </div>
</hero-pattern>
```

## API

| Props | Description | Type | Default |
| :---: | :---------: | :--: | :-----: |
| pattern | 87 kinds of patterns that Hero Patterns supported, check [pattern list]() | String | `line-to-motion` |
| fillColor | Controls the foreground color of the generated image. | String | `#9c92ac` |
| fillOpacity | Controls the foreground opacity of the generated image. | String | `0.4` |
| backgroundColor | Controls the background color of the generated image. | String | `#dfdbe5` |
| repeat | Controls how the background repeated of the generated image. | String | `repeat` |

## Slot

`<HeroPattern />` component provide a custom slot, you can write some element on the generated pattern.

## License

MIT @ [xiaoluoboding](https://github.com/xiaoluoboding)
