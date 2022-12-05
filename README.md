# prettier-plugin-nativewind

A fork of 
[`prettier-plugin-tailwindcss`](https://github.com/tailwindlabs/prettier-plugin-tailwindcss)
with support for [NativeWind](https://www.nativewind.dev/).

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

## Usage

Please refer to the 
[original package documentation](https://github.com/tailwindlabs/prettier-plugin-tailwindcss/#readme)
for usage instructions.

## Changelog

### v0.1.1

* Add support for NativeWind `variants()` calls.

### v0.1.0

* Initial release (forked from `prettier-plugin-tailwindcss@0.2.0`)
