## call, apply

The call and applymethod on a function, makes me call the function with a `given this value`

In the following code I've created a person1 function to be used to print person2, which means changing the this value

```js
const person1 = {
  firstName: 'Ahmed',
  secondName: 'Kashkoush',
  printFullName(str, age) {
    console.log(`${this.firstName} ${this.secondName} age:${age}, str:${str}`);
  },
};
person1.printFullName();
const person2 = {
  firstName: 'Khalid',
  secondName: 'Rabee',
};
// I want to use printFullName on person2 without coping it to person 2
// How 🤔
// Solution ⭐⭐⭐
person1.printFullName.call(person2, 'hi', 27); // Khalid Rabee age:27, str:hi
person1.printFullName.apply(person2, ['hi', 27]); // apply accept array arguments
```

## bind

Same but the Difference is it returns a callback function, and not called right away

```js

const person1 = {
  firstName: 'Ahmed',
  secondName: 'Kashkoush',
  printFullName(str, age) {
    console.log(`${this.firstName} ${this.secondName} age:${age}, str:${str}`);
  },
};
const person2 = {
  firstName: 'Khalid',
  secondName: 'Rabee',
};
// bind ⭐⭐⭐⭐⭐⭐⭐⭐

const print = person1.printFullName.bind(person2); // this arguments will never change
print('hello', 50); // will use the preset arguments

// bind is important for setting this without calling the function
// [Explanation]🌃
const cairoAirPort = {};
cairoAirPort.planes = 50; // planes in the airport;
// I want to make function that buy new Plan
cairoAirPort.buyPlane = function () {
  console.log(this);
  this.planes++;
  console.log(this.planes);
};

// I want to call function when click on the button
document
  .querySelector('.buy')
  .addEventListener('click', cairoAirPort.buyPlane.bind(cairoAirPort));

// without using the bind method ==> will use the button this, not object this
// why didn't use call, or apply
// --> will call the function and I need callback
// ⭐⭐⭐ use bind method to set this keyword and without calling the funciton
```

---

[Function notes](Function%20notes)
