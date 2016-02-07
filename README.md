# Tooltip plugin for Chartist.js

This plugin provides quick and easy tooltips for your chartist charts. Touch support is planned soon.

Please visit http://gionkunz.github.io/chartist-js/plugins.html for more information.

## Available options and their defaults

```javascript
var defaultOptions = {
  currency: undefined, //accepts '£', '$', '€', etc.
  //e.g. 4000 => €4,000
  tooltipFnc: undefined, //accepts function
  //build custom tooltip
  class: undefined, // accecpts 'class1', 'class1 class2', etc.
  //adds class(es) to tooltip wrapper
  appendToBody: false //accepts true or false
  //appends tooltips to body instead of chart container
};
```

## Sample usage in Chartist.js

`bower install chartist-plugin-tooltip --save`

With descriptive text:
```js
var chart = new Chartist.Line('.ct-chart', {
  labels: [1, 2, 3],
  series: [
    [
      {meta: 'description', value: 1},
      {meta: 'description', value: 5},
      {meta: 'description', value: 3}
    ],
    [
      {meta: 'other description', value: 2},
      {meta: 'other description', value: 4},
      {meta: 'other description', value: 2}
    ]
  ]
}, {
  plugins: [
    Chartist.plugins.tooltip()
  ]
});
```

Without descriptive text:
```js
var chart = new Chartist.Line('.ct-chart', {
  labels: [1, 2, 3, 4, 5, 6, 7],
  series: [
    [1, 5, 3, 4, 6, 2, 3],
    [2, 4, 2, 5, 4, 3, 6]
  ]
}, {
  plugins: [
    Chartist.plugins.tooltip()
  ]
});
```

With options text:
```js
var chart = new Chartist.Line('.ct-chart', {
  labels: [1, 2, 3],
  series: [
    [
      {meta: 'description', value: 1},
      {meta: 'description', value: 5},
      {meta: 'description', value: 3}
    ],
    [
      {meta: 'other description', value: 2},
      {meta: 'other description', value: 4},
      {meta: 'other description', value: 2}
    ]
  ]
}, {
  plugins: [
    Chartist.plugins.tooltip({
      currency: '$',
      class: 'class1 class2',
      appendToBody: true
    })
  ]
});
