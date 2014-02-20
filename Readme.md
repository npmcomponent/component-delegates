*This repository is a mirror of the [component](http://component.io) module [component/delegates](http://github.com/component/delegates). It has been modified to work with NPM+Browserify. You can install it using the command `npm install npmcomponent/component-delegates`. Please do not open issues or send pull requests against this repo. If you have issues with this repo, report it to [npmcomponent](https://github.com/airportyh/npmcomponent).*

# delegates

  Higher level dom event delegation management based on [EventManager](https://github.com/component/event-manager).

## Installation

    $ component install component/delegates

## Example

```js
var delegates = require('delegates');
var el = document.querySelector('ul');

var view = new ListView(el);

function ListView(el) {
  this.events = delegates(el, this);
  this.events.bind('click li', 'remove');
}

ListView.prototype.remove = function(e){
  var el = e.target;
  console.log('remove %s', el.textContent);
  el.parentNode.removeChild(el);
};
```

## API

  See [component/event-manager](https://github.com/component/event-manager).

## License

  MIT
