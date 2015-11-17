Component for the [Crafty](http://craftyjs.com/) HTML5/JavaScript game engine for
handling input events of gamepad devices. Also contains a *GamepadMultiway*
component for moving an entity with a gamepad.

```javascript
Crafty.e('2D, DOM, Gamepad')
    .gamepad(0)
    .bind('GamepadKeyChange', function (e) {
        console.log('Button ' + e.button + ', Value ' + e.value);
    })
    .bind('GamepadAxisChange', function (e) {
        console.log('Axis ' + e.axis + ', Value ' + e.value);
    });

Crafty.e('2D, DOM, GamepadMultiway') // Entity can be controlled with gamepad
    .gamepadMultiway({
        speed: 100, // Speed is in px/sec
        gamepadIndex: 0
    });
```

The [HTML5 Gamepad API](http://www.html5rocks.com/en/tutorials/doodles/gamepad/)
is yet experimental and subject to change. Expect this code to break until the
Gamepad API is stable. So far has only been tested with Google Chrome a Xbox 360
controller, a Playstation 3 controller and a Thrustmaster Firestorm Dual
Analog III.

Licensed under MIT License.

# Crafty support

This version of the component requires Crafty 0.7.0 or higher.
(speed is in px/sec and based on the Motion component)

For Gamepad support for Crafty 0.6.x, please use version 0.0.1 of this
component. (where speed is in px/frame)

