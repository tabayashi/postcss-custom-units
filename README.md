# postcss-custom-units

A PostCSS plugin allowing for on-the-fly custom units for uniform spacing, vertical-rhythm, and baseline grids.

## Examples

Create a value, then utilize that value. Let's say you wanted to build you line-heights off a baseline grid:

```css
h1 {
  --unit-bf: 16px;
  --unit-bl: 24px;
  font-size: 2bf;
  line-height: 2.75bl;
  margin-top: .25bl;
}
```

Yields:

```css
h1 {
  --unit-bf: 16px;
  --unit-bl: 24px;
  font-size: calc(16px * 2);
  line-height: calc(24px * 2.75);
  margin-top: calc(24px * .25);
}
```

## Options

Default:

```javascript
{
  prefix: 'unit',
}
```

- `unit` (String) Allows you to change the prefix customUnits uses to watch for your inline units.

## Usage

Include the plugin:

```javascript
postcss([
  require('postcss-custom-units')(options)
]).process
```

See [PostCSS](https://github.com/postcss/postcss) docs for examples for your environment.

## Licence
Released under the MIT license.
