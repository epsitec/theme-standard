## Standard for Theming

Incompatibility of global CSS Selectors and Components results in various ways we style our Components. It devides our community into 3 categories:

1. Traditional CSS class names.
1. Generated CSS class names.
1. Inline Styles.

As a result - we have no consistency across UI libraries in terms of theming. This standard aims to fix it. It is framework agnostic and supports all approaches.

### Theme Example

```json
{
  "someOption": "someValue",
  "style": {
    "color": "red"
  },
  "styles": {
    "myButton": {
      "color": "green"
    }
  },
  "classes": {
    "myButton": ".my-button-dk3j4"
  }
}
```

### Definition of Theme

Theme is a [JSON](http://www.json.org/) that defines the look and related functionality of a component. A component is allowed to implement a __subset__ of this standard.

### Reserved Properties

Reserved properties are `style`, `styles` and `classes`.

### Options

Any property name other than reserved one, can be used as an option.
Option values are any legal JSON values.

### Style

A `style` property is reserved for style objects. Style object may have any property names and values which can be rendered inline, defined by the [css-style-attr](https://www.w3.org/TR/css-style-attr/) specification.

### Styles

A `styles` object is a map of named `style` objects, where `name` is any valid JSON property name and `value` is of `style` format.

### Classes

A `classes` object is a map of names and class names. Name is any valid property name. Value is a string which is specified by the [html class attribute](https://www.w3.org/TR/2011/WD-html5-20110525/elements.html#classes).

### Development

This is an early stage proposal. Feel free to create issues and discribe use cases. Also feel free to make the documentation better.


