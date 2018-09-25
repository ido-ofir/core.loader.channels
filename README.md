# core.loader.channels

loads channels from plugin definitions.

definition of channels in <a href="https://github.com/ido-ofir/core.constructor">core.constructor</a>

```js
let core = new require('core.constructor')();
 
core.plugin(
    require('core.loader.channels')
);

// plugins can now declare actions on the plugin definition object:
core.plugin({
    name: 'test',
    channels: {
        a(data, done){ ... },
        b(data, done){ ... },
    }
});

// fire the newly created channels
core.fire('a', { some: 'data' })
core.fire('b', { some: 'data' })
```
