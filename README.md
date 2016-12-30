# Switch

[![Build Status](https://travis-ci.org/zhiyul/Switch.svg?branch=master)](https://travis-ci.org/zhiyul/Switch)
[![Coverage Status](https://coveralls.io/repos/github/zhiyul/Switch/badge.svg?branch=master)](https://coveralls.io/github/zhiyul/Switch?branch=master)

:rabbit: A simple and powerful iOS style switch for checkbox.

[Live Preview](http://weatherstar.me/Switch/)

## Installation

##### Standalone:

```html
<link rel="stylesheet" href="dist/switch.css" />
<script src="dist/switch.js"></script>
```

##### npm:

```javascript
$ npm install weatherstar-switch --save-dev
```

## Usage

````html
<input type="checkbox" class="checkbox-switch" />
````

standalone version

````javascript
var el = document.querySelector('.checkbox-switch');
var mySwitch = new Switch(el, options);
````

work with module bundle

```javascript
require('weatherstar-switch/dist/switch.css');
var Switch = require('weatherstar-switch');

var el = document.querySelector('.checkbox-swtich');
var mySwitch = new Switch(el, options);
```

## Settings and Defaults

```js
defaults = {
    size             : 'default'
  , checked          : undefined
  , onText           : 'Y'
  , offText          : 'N'
  , onSwitchColor    : '#64BD63'
  , offSwitchColor   : '#fff'
  , onJackColor      : '#fff'
  , offJackColor     : '#fff'
  , showText         : false
  , disabled         : false
  , onInit           : function(){}
  , onChange         : function(){}
  , onRemove         : function(){}
  , onDestroy        : function(){}
};
```

- `size` : size of switch element, can be `default` | `small` | `large`
- `checked` : state of switch and checbox, if `undefined` the switch state according to the checkbox 
- `onText` :  text in the jack when switch ON
- `offText` : text in the jack when switch OFF
- `onSwitchColor` : color of checked switch element
- `offSwitchColor` : color of unchecked switch element
- `onJackColor` : color of checked jack element
- `offJackColor` : color of unchecked jack element
- `showText` : show or hide text in the jack of switch 
- `disabled` : enable or disable click events and changing the state of the switch
- `onInit` : called when switch init finish
- `onChange` : called when original checkbox's `checked` change
- `onRemove` : called when `mySwitch.remove()`
- `onDestroy` : called when  `mySwitch.destroy()`

## API

##### .on()

Set switch ON.

##### .off()

Set switch OFF.

##### .toggle()

Toggle switch.

##### .disable()

Disable events bind to switch.

##### .enable()

Enable events bind to switch.

##### .destroy()

Remove all events bind to switch.

##### .remove()

Remove switch form DOM and show the checkbox.

## License

MIT © [zhiyul](http://github.com/zhiyul)

