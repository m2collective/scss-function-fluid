# SCSS Function Fluid

A package for integrating function to create responsive typography and design.

![npm](https://img.shields.io/npm/v/@m2collective/scss-function-fluid?style=for-the-badge)

___

## Installation

You can install the package automatically using NPM:

```
npm i @m2collective/scss-function-fluid
```

## Usage

To use the package, import it into your project:

```scss
@use "@m2collective/scss-function-fluid" as *;

.demo {
    font-size: fluid(16px, 24px);
}

// Return

.demo {
    font-size: 1rem;
}
```

## Changing the namespace

You can change the namespace during function import and use the function with a different namespace:

```scss
@use "@m2collective/scss-function-fluid" as function;

.demo {
    font-size: function.fluid(16px, 24px);
}

// Return

.demo {
    font-size: 1rem;
}
```

## Changing the variables

You can redefine the default values for the specified variables when importing the function:

```scss
@use "@m2collective/scss-function-fluid" as * with (
    $min-breakpoint: 480px,
    $max-breakpoint: 1536px,
    $unit: vw,
    $baseline: 16,
    $round: 2,
);

.demo {
    font-size: fluid(16px, 24px);
}

// Return

.demo {
    font-size: 1rem;
}
```

## License

The MIT License (MIT). Please see the [License file](LICENSE.txt) for more information.
