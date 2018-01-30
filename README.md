ngEsc
=======

Trigger an expression when the esc key is pressed.

<br/>

DEMO
-------
https://kimsunwook.github.io/ngEsc

INSTALL
-------

```
bower install ng-esc --save
```

<br/>

USAGE
-----

Make sure you include the module 'ngEsc' in your application config

```
angular.module('myApp', [
  'ngEsc',
  ...
]);
```

```
<input
  ng-esc="message = 'esc pressed'" // Invoked when you press the Esc key
  ng-esc-model="model" // If you do not put object, $esc and $esced values ​​are stored in scope.
  ng-esc-duration="1000" // The value of $ esc lasts true and the default value is 100 (ms).
  ng-class="[
    {'esc_classes':model.$esc}, // The value of $esc becomes true on click and turns false after duration (ms).
    {'esc_classes':model.$esced} // The value of $esced is true when clicked and does not change.
  ]">
```

Once esc is pressed

```
$scope.message === 'esc pressed' // true
$scope.model.$esc === true // true
$scope.model.$esced === true // true
```

<br/>

Easy!