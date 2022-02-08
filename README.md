# Javascript Array Methods

## Q1

> Create a function named getLength which takes a string as an argument, and
> returns the length of the string.

✨ For example:

getLength('foo') should return 3

getLength('hello') should return 5

```
function getLength(arg) {
    return arg.length;
};

console.log('Q1 -> '+getLength('hello'));
```

## Q2

> Create a function named concatenate which takes two strings, as arguments and
> returns a single string composed of, those two strings without spaces.

✨ For example:

concatenate('foo','bar') should return 'foobar'

concatenate('hello','world') should return 'helloworld'


```
function concatenate(s,t) {
    return s+t;
};

console.log('Q2 -> '+concatenate('foo','bar'));
```

## Q3

> Create a function named difference which takes two integers, as arguments and
> returns the absolute value of the difference.

✨ For example:

difference(1, 2)  should return 1

difference(-5, 5) should return 10

```
function difference(a,b) {
  return Math.abs(a-b);
};

console.log('Q3 -> '+difference(-5,5));
```

## Q4

> Create a function named isOdd which accepts an integer, as an argument and
> returns true if the value is odd. An odd integer is not wholly divisible by
> two.

✨ For example:

isOdd(4) should return false

isOdd(5) should return true

```
function isOdd(integer) {
    return integer%2===1;
};

console.log('Q4 -> '+isOdd(5));
```

## Q5

> Create a function named addTwo which takes an array of integers as an argument
> and returns an array where each value has been incremented by two.

✨ For example:

addTwo([1, 2, 3]) should return [3, 4, 5]

addTwo([0, 0]) should return [2, 2]

```
function addTwo(arr) {
    return arr.map(el => el+2);
};

console.log('Q5 -> '+addTwo([1,2,3]));
```

## Q6

> Create a function named convertHexadecimal which takes as an argument a string
> representing a hexadecimal integer (base-16) and returns a decimal integer
> (base-10).

✨ For example:

convertHexadecimal('10') should return 16

convertHexadecimal('af') should return 175

```
function convertHexadecimal(str) {
    return Number('0x'+str);
};

console.log('Q6 -> '+convertHexadecimal(10));
```

## Q7

> Create a function named onlyTruthy which takes as an argument an array of
> values and returns an array consisting of only those values which are truthy
> (equivalent to true).

✨ For example:

onlyTruthy([false, true, true]) should return [true, true]

onlyTruthy([0, 1, '','a']) should return [1, 'a']

```
function onlyTruthy(arr) {
    return arr.filter(el => el);
};

console.log('Q7 -> '+onlyTruthy([false, true, true]));
```

## Q8

> Create a function named sum which takes as an argumend a non-empty array of
> integers and returns the sum of those integers.

✨ For example:

sum([1, 2, 3]) should return 6

sum([0, 4, 4, 4]) should return 12

```
function sum(arr) {
    return arr.reduce((el,sum) => sum+el,0);
};

console.log('Q8 -> '+sum([1,2,3]));
```

## Q9

> Create a function named removeVowels which takes a string as an argument and
> returns that string with all vowels removed. Vowels are considered the
> following characters: a, e, i, o, u, A, E, I, O, U

✨ For example:

removeVowels('Hello World') should return 'Hll Wrld'

removeVowels('FOOBAR') should return 'FBR'

```
function removeVowels(str) {
    let al = [ 'a', 'e', 'i', 'o', 'u',
               'A', 'E', 'I', 'O', 'U' ];
    let result = "";

    for(let i = 0; i < str.length; i++)
    {

        if (!al.includes(str[i]))
        {
            result += str[i];
        }
    }
    return result;
};

console.log('Q9 -> '+removeVowels("Hello World"));
```

## Q10

> Create a function removeDuplicates which takes a non-empty array as a value
> and returns an array with only one copy of any of the original array's values.

✨ For example:

removeDuplicates([0, 0, 1, 2, 2]) should return [0, 1, 2]

removeDuplicates(['a','a', 'a']) should return ['a']

```
function removeDuplicates(arr) {
    return Array.from(new Set(arr));
};

console.log('Q10 -> '+removeDuplicates([0,0,1,2,2]));
```

## Q11

> Create a function named join which takes two arrays as argument and returns a
> single array consisting of all the values of those two arrays.

✨ For example:

join([0, 1], [1, 2]) should return [0, 1, 1, 2]

join(['a', 'b'], ['c']) should return ['a', 'b', 'c']

```
function join(arr1,arr2) {
    return [...arr1, ...arr2];
};

console.log('Q11 -> '+join([0, 1], [1, 2]));
```

## Q12

> Create a function named getLast which takes a non-empty array of unspecified
> length and returns the last element of the array.

✨ For example:

getLast([1, 2, 3]) should return 3

getLast([9, 7, 5]) should return 5

```
function getLast(arr) {
    return arr[arr.length-1];
};

console.log('Q12 -> '+getLast([1,2,3]));
```

## Q13

> Create a function named reverse which takes a non-empty array as an argument
> and returns a reversed array without mutating the input.

✨ For example:

reverse([1, 2, 3]) should return [3, 2, 1]

reverse([1, 0]) should return [0, >1]

```
function reverse(arr) {
    let result = Array.from(arr);
    result.reverse();
    return result;
};

console.log('Q13 -> '+reverse([1,2,3]));
```

## Q14

> Created a function named toArray which takes an unspecified number of
> arguments and returns an array with those arguments as values.

✨ For example:

toArray(1, 2, 3) should return [1, 2, 3]

toArray('a') should return ['a']

```
function toArray(string) {
    return [...string];
};

console.log('Q14 -> '+toArray('123'));
```

## Q15

> Create a function named allGreaterThanThree which accepts an unspecified
> number of integer arguments and returns true only if all passed arguments are
> greater than 3.

✨ For example:

allGreaterThanThree(1, 3, 5) should return false

allGreaterThanThree(4, 6) should return true

```
function allGreaterThanThree(integer) {
    return [...arguments].every(el => el>3);
};

console.log('Q15 -> '+allGreaterThanThree((4, 6)));
```

## Q16

> Create a function named anyGreaterThanThree which accepts an unspecified
> number of integer arguments and returns true if any passed argument is greater
> than 3.

✨ For example:

anyGreaterThanThree(2, 3) should return false

anyGreaterThanThree(2, 3, 4) should return true

```
function anyGreaterThanThree(){
 return [...arguments].some(el => el>3);
};

console.log('Q16 -> '+anyGreaterThanThree(2,3,4));
```

## Q17

> Create a function named getValues which takes an object and returns an array
> of the enumerable property values of the object. ✨ For example: getValues({
> a: 1, b: 2}) should return [1, 2] getValues({ c: 'foo' }) should return
> ['foo']

```
function getValues(obj){
   return Object.values(obj);
};

console.log('Q17 -> '+getValues({ a: 1, b: 2}));
```

## Q18

> Create a function named arity which takes a function as an argument and
> returns the number of defined arguments the function accepts.

✨ For example:

If,

const add = (a, b) => a + b

const addOne = (a) => a + 1

Then, arity(add)

should return 2 arity(addOne) should return 1

```
function arity(fn) {
    const add = (a, b) => a + b;
      return fn.length-1;
};

console.log('Q18 -> '+arity(add));
```

## Q19

> Create a function called functionalize which takes a value and returns a
> function, which when executed, returns that value.

✨ For example:
functionalize('a')() should return 'a'

functionalize(false)() should return false

```
function functionalize(arg) {
    return function(){
      return arg;
    }
}

console.log('Q19 -> '+functionalize('a')());
```

## Q20

> Create a function named setDefault which takes an argument of any value and
> returns a function, which when passed a truthy argument, returns that truthy
> argument, and when passed a falsy argument, returns the original argument
> passed to setDefault.

✨ For example:

setDefault(72)(true) should return true

setDefault('foobar')(false) should return 'foobar'

```
function setDefault(a) {
 return function(b){
     if(b){
       return b
  }
return a
  }
}


console.log('Q20 -> '+setDefault(72)(true));
```
