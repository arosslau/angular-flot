angular-flot
============

An Angular directive which wraps [Flotcharts](http://www.flotcharts.org/).


# Installation

This library is provided as a Bower component and NPM module:

- Bower: `bower install angular-flot`
- NPM: `npm install angular-flot`


# How to Use

First, make sure to add Flotchart to your project, as explained in [Flotchart's
ReadMe](https://github.com/flot/flot/blob/master/README.md) since we don't bundle Flotcharts for
you.

Add `angular-flot` to the list of dependencies in your Angular.JS application:

```javascript
angular.module('myapp', [
    'ngRoute',
    // ...
    'angular-flot'
]);
```

In your controller, create two variables to hold the dataset and Flot chart options:

```javascript
angular.module('myapp').controller('MyController', function ($scope) {
    $scope.myData = [];
    $scope.myChartOptions = {};
});
```

In your view or template, add the `flot` directive, making sure to specify both the `dataset` and
`options` attributes, pointing to the scope variables defined above:

```html
<flot dataset="myData" options="myChartOptions"></flot>
```


# Reference

Directive attributes:

* `dataset`: Name of a variable defined in the current $scope to be used as input dataset. See
  <https://github.com/flot/flot/blob/master/API.md#data-format> for more information.
* `options`: Name of an object defined in the current scope used to configure the chart. See
  <https://github.com/flot/flot/blob/master/API.md#plot-options> for more information.
* `width`: Chart width, e.g.: "100%" or "350px".
* `height`: Chart height, e.g.: "100%" or "100px".
