# tailwindcss-textShadow
A Utility Plugins for Text Shadow like Tailwindcss default boxshadow with theme and variants option.


## Installation

#### Yarn
```
yarn add tailwindcss-textshadow --dev
```
#### npm
```
npm i --save-dev tailwindcss-textshadow
```
## Add following changes in tailwind.config.js

#### import the plugin

Add the plugin to the `plugins` array in your Tailwind configuration file `(tailwind.config.js)`.

```javascript
plugins: [
  require('tailwindcss-textshadow')
]
```

#### Set your own text shadow

You can change, add, or remove `textShadow` property by editing the `theme.textShadow section` of your Tailwind config.

If a default shadow is provided, it will be used for the non-suffixed `.text-shadow` utility. Any other keys will be used as suffixes, for example the key '2' will create a corresponding `.text-shadow-2` utility.

```javascript
// tailwind.config.js
module.exports = {
  theme: {
    textShadow: {
      default: '0 2px 0 #000',
      md: '0 2px 2px #000',
      h1: '0 0 3px #FF0000, 0 0 5px #0000FF',
      xl: '0 0 3px rgba(0, 0, 0, .8), 0 0 5px rgba(0, 0, 0, .9)',
      none: 'none',
    }
  }
}

```


#### Set Variants in Tailwind Config file

Can use [Tailwind's own variants](https://tailwindcss.com/docs/state-variants/) under the variant name `textShadow`.

```javascript
// tailwind.config.js
variants: {
//...
textShadow: ['responsive', 'hover'],
//...
},
```

## How to use

#### Responsive
To control the textshadow of an text element at a specific breakpoint, add a {screen}: prefix to any existing textShadow utility. For example, use md:text-shadow-h1 to apply the text-shadow-h1 utility at only medium screen sizes and above.

```html
<div class="text-shadow sm:text-shadow-md md:text-shadow-h1 lg:text-shadow-xl xl:text-shadow-2xl ...">
  <!-- ... -->
</div>
```

## Credits

- [Adam Wathan](https://github.com/adamwathan)
- [plugin-examples](https://github.com/tailwindcss/plugin-examples)


## License

The MIT License (MIT). Please see [License File](LICENSE) for more information.
