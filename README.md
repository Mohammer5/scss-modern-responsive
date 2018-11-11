# Modern responsive

This library contains 5 mixins to simplify working with breakpoints.

## Install

You can use either yarn or npm:

```
npm install modern-responsive
```

## Why use this library

I created these mixins to increase the readability of SCSS code.
The mixins work well with well named variables.

## Usage

There are two ways how to import the mixins.

```scss
// import all mixins
@import "~modern-responsive/lib/from";

// or import the mixin that you need
@import "~modern-responsive";
```

Let's say you've set the following breakpoints:

```scss
$phone: 480px;
$tablet: 720px;
$desktop: 1024px;
```

You can use the mixins like this:

```scss
@import "~modern-responsive/lib/from";
@import "../path/to/breakpoints";

.headline {
  font-size: 12px;

	@include from($tablet) {
	  font-size: 16px;
	}

	@include from($desktop) {
	  font-size: 20px;
	}
}
```