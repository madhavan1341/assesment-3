1.a)anonomous 
var add = (function(a, b) {
  return a + b;
})(5, 10);
console.log(add);
IIFE version:
(function(a, b) {
  var add = a + b;
  console.log(add);
})(5, 10);

1. b)var stringArray = ["hello", "world", "javascript"];

var titleCaseArray = (function(arr) {
  return arr.map(function(str) {
    return str.charAt(0).toUpperCase() + str.slice(1);
  });
})(stringArray);

console.log(titleCaseArray);

1.c)anonomous

var numbers = [1, 2, 3, 4, 5];
var sum = (function(arr) {
  var result = 0;
  for (var i = 0; i < arr.length; i++) {
    result += arr[i];
  }
  return result;
})(numbers);

console.log(sum);
iife:
var numbers = [1, 2, 3, 4, 5];
(function(arr) {
  var sum = 0;
  for (var i = 0; i < arr.length; i++) {
    sum += arr[i];
  }
  console.log(sum);
})(numbers);

1.d)anonomous
var numbers = [2, 3, 4, 5, 6, 7, 8, 9, 10];
var primes = (function(arr) {
  function isPrime(number) {
    if (number <= 1) {
      return false;
    }
    
    for (var i = 2; i <= Math.sqrt(number); i++) {
      if (number % i === 0) {
        return false;
      }
    }
    
    return true;
  }
  
  var primeNumbers = [];
  
  for (var i = 0; i < arr.length; i++) {
    if (isPrime(arr[i])) {
      primeNumbers.push(arr[i]);
    }
  }
  
  return primeNumbers;
})(numbers);

console.log(primes);
iife
var numbers = [2, 3, 4, 5, 6, 7, 8, 9, 10];
(function(arr) {
  function isPrime(number) {
    if (number <= 1) {
      return false;
    }
    
    for (var i = 2; i <= Math.sqrt(number); i++) {
      if (number % i === 0) {
        return false;
      }
    }
    
    return true;
  }
  
  var primeNumbers = [];
  
  for (var i = 0; i < arr.length; i++) {
    if (isPrime(arr[i])) {
      primeNumbers.push(arr[i]);
    }
  }
  
  console.log(primeNumbers);
})(numbers);
2.a)const numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
const oddNumbers = numbers.filter((x) => x % 2 !== 0);
oddNumbers.forEach((number) => {
  console.log(number);
});
2.b)const strings = ["hello", "world", "javascript", "example"];
const titleCaseStrings = strings.map((str) => str.charAt(0).toUpperCase() + str.slice(1).toLowerCase());
console.log(titleCaseStrings);
2.c)const numbers = [1, 2, 3, 4, 5];
const sum = numbers.reduce((total, num) => total + num, 0);
console.log(sum);
2.d)const numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
const primeNumbers = numbers.filter((num) => {
  if (num < 2) {
    return false;
  }
  for (let i = 2; i <= Math.sqrt(num); i++) {
    if (num % i === 0) {
      return false;
    }
  }
  return true;
});

console.log(primeNumbers);
2.e)const numbers = [121, 123, 345, 787, 555, 212];
const palindromeNumbers = numbers.filter((num) => {
  const reversedNum = parseInt(num.toString().split("").reverse().join(""));
  return num === reversedNum;
});
console.log(palindromeNumbers);
