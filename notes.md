
## Template Literal
```JavaScript
console.log(`hello! I'm a string`);

console.log("string text 1\n" + "string tex2");

console.log(`Hello i'm a string
continue son this line`);

const name = "Maurice"
const day = "Wednesday"
const instructor = {
    name: "Maurice",
    lesson: "ES6",
    greet: function () {
        return `Hello ${this.name} whatever lesson is ${this.lesson}`
    }
}

console.log("Hewwo" + name + "I hope you have a gwate day on" + day)

console.log(`hello ${name} i hope ${day} goes well!`)

console.log(`Hello ${instructor.name} whatever leson is ${instructor.lesson}`)

console.log(instructor.greet())

function foo() {
    let x = true;
    if (x) {
        var usingVar = "im using var";
    }
    console.log(usingVar)
}

foo(); // undefined
```
## Arrow Functions
```JavaScript
const teacher = {
    name: "Jimm",
    speak: function () {

        let boundFunction = function(){
            console.log('Later my name is' + this.name);
        }
    };
    setTimeout(boundFunction, 1000);
};
teacher.speak();

let students = [{name: "a"}, {name: "b"}, {name: "c"}, {name: "d"}];
let names = students.map( (student) => student.name);
//same as 
let namess = students.map((student) =>{
    return student.name
})

console.log(names)
```
## Next Section
```JavaScript
function add(){
    console.log("arguments object:", arguments);

    var numbers = Array.prototype.slice.call(arguments);

    var sum = 0;

    numbers.forEach(function (number) {
        sum += number;
    });
    return sum;
}

console.log(add(1,2,3,4,5,6,7,8));

let add = (...numbers) => {
    console.log("rest parameters", numbers);

    let sum = 0;

    numbers.forEach(function (number) {
        sum += number;
    });
    return sum;
}

let add = (...numbers) => numbers.reduce((sum, number) => sum += number, 0);

console.log(add(1,2,3,4,5,6,7,8))
```
##
```JavaScript
let random = ["Hello", "World", true, 99]
let newArray = [1, 2, ...random, 3]

console.log(newArray);
let copmletedHomework = () => {
    return ["julian", "AJ", "Matt"];
}

let [x,y,z] = copmletedHomework()

console.log(x,z)
function Person (name, job){
    this.name = name;
    this.job = job;
}
Person.prototype.getName = function getname(){
    return this.name
}
Person.prototype.getJob = function getJob(){
    return this.job
}

var goodGuy = new Person ("Aang", "Airbender");

console.log(goodGuy.getName())
class Person {
    constructor (name, job){
        this.name;
        this.job;
    }
    getName(){
        return this.name;
    }
    getJob(){
        return this.job;
    }
}

let goodGuy = new Person('Neo', 'the one');
console.log(goodGuy)
class Person {
    constructor(name, job) {
        this.name = name;
        this.job = job;
    }
    getName() {
        return this.name;
    }
    getJob() {
        return this.job;
    }
}
```
## 
```JavaScript
class SuperHero extends Person {
    constructor (name, heroName, superPower) {
        super(name);
        this.heroName = heroName;
        this.superPower = superPower;
    }
    secretIdentity() {
        return `${this.heroName} is ${this.name}!!`
    }
}

let batman = new SuperHero("Bruce Wayne", "im Batman")
console.log(batman.secretIdentity())
class Person {
    constructor (name){
        this.name = name;
    }
    set name(name){
        this._name = name;
    }
    get name(){
        return this._name
    }
}

let goodGuy = new Person('Jim Gordon');
console.log(goodGuy.name)
goodGuy.name = "James Gordon"
console.log(goodGuy.name)
```