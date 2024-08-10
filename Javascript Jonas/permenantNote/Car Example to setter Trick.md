# Implementation

```js
class Car {
  constructor(speed, make) {
    // validate speed by setter
    this.speed = speed
    // this.speed calls setter ⭐
    this.make = make
    console.log(this.speed, this.make)
  }
}
```

## set&get Validate

```js
set speed(speed) {
	// make actual Property Private _
	this._speed = speed < 0 ? 0 : speed;
}

get speed() {
	// return Actual Property
	return this._speed;
}
```
