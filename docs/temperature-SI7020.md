<!--remove-start-->

# Temperature - SI7020

<!--remove-end-->






##### SI7020



![docs/breadboard/temperature-SI7020.png](breadboard/temperature-SI7020.png)<br>

Fritzing diagram: [docs/breadboard/temperature-SI7020.fzz](breadboard/temperature-SI7020.fzz)

&nbsp;




Run with:
```bash
node eg/temperature-SI7020.js
```


```javascript
var five = require("../");
var Tessel = require("tessel-io");
var board = new five.Board({
  io: new Tessel()
});

board.on("ready", function() {
  var temp = new five.Temperature({
    controller: "SI7020",
    port: "A"
  });

  temp.on("change", function() {
    console.log(this.celsius);
  });
});

```









## Learn More

- [SI7020 - I2C Temperature Sensor](https://tessel.io/docs/climate)

&nbsp;

<!--remove-start-->

## License
Copyright (c) 2012, 2013, 2014 Rick Waldron <waldron.rick@gmail.com>
Licensed under the MIT license.
Copyright (c) 2014, 2015 The Johnny-Five Contributors
Licensed under the MIT license.

<!--remove-end-->
