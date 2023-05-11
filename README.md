# Deprecation notice

## ⚠️ This package is no longer actively maintained ⚠️

[`prettier-plugin-tailwindcss`](https://www.npmjs.com/package/prettier-plugin-tailwindcss)
now supports sorting Tailwind classes in custom locations, making this fork obsolete.

---

---

# prettier-plugin-nativewind

A fork of 
[`prettier-plugin-tailwindcss`](https://www.npmjs.com/package/prettier-plugin-tailwindcss)
with support for [NativeWind](https://www.nativewind.dev) and other use custom use cases.

```bash
npm install -D prettier-plugin-nativewind
# or
pnpm add -D prettier-plugin-nativewind
# or
yarn add -D prettier-plugin-nativewind
```

## Fork features

Support for automatically sorting tailwind classes found in strings inside of:

* JSX props: `className` and `tw`

* Styled components defined using `styled()`

* Class variants defined using `variants()`

* Or, customize which props and function calls to look for tailwind classes in

## Usage

Please refer to the 
[original package documentation](https://github.com/tailwindlabs/prettier-plugin-tailwindcss/#readme)
for basic usage instructions.

### Customizing props

This fork adds two additional prettier configuration options, which allow you
to customize which props and function calls to search for tailwind classes in.

* `tailwindCustomProps`
* `tailwindCustomFunctions`
* `tailwindCustomTaggedTemplates`

**Customize props:**

Sort custom props which get passed as classnames to child elements:

```js
// prettier.config.js
module.exports = {
    tailwindCustomProps: ['className', 'containerClassName'] 
};
```

**Customize functions:**

Sort inside calls to
[`cva()`](https://www.npmjs.com/package/class-variance-authority) 
instead of `styled()`:

```js
// prettier.config.js
module.exports = {
    tailwindCustomFunctions: ['cva'] 
};
```

**Tagged template literals:**

```js
// prettier.config.js
module.exports = {
  // Sort template strings found in tagged template literal calls named tw``
  tailwindCustomTaggedTemplates: ['tw']
};
```

**Regular expressions:**

You can also use regular expressions by starting a string with `^`.

Sort any prop which ends in `ClassName`:

```js
// prettier.config.js
module.exports = {
    tailwindCustomProps: ['className', '^[a-z]+ClassName$'] 
};
```

## Changelog

### v0.2.3

* Add deprecation to readme
* Add postinstall warning message

### v0.2.2

* Synchronize with upstream `prettier-plugin-tailwindcss@0.2.6`

### v0.2.1

* Synchronize with upstream `prettier-plugin-tailwindcss@0.2.5`
* Add support for tagged template literals

### v0.2.0

* Synchronize with upstream `prettier-plugin-tailwindcss@0.2.1`
* Add support for customizing which props and functions to search

### v0.1.1

* Add support for NativeWind `variants()` calls.

### v0.1.0

* Initial release (forked from `prettier-plugin-tailwindcss@0.2.0`)
