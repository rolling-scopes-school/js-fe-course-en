# Unit tests

## Task
Your task is to implement 'custom' version of the lodash library following next requirements:
1. Usage of `Array.prototype.*` or `Object.prototype.*` methods is **strictly forbidden**. (!!! Do not mix up *methods* and *properties* )
2. You can create your own additional service functions (if needed).
3. You should use ES6+ features (any feature which supported by latest stable Chrome).
4. Lodash chain is out of scope

And **cover your code by unit tests** following next requirements:
1. You should use Jest for the current task
2. You should follow TDD (Test-driven development)
3. The code coverage should be at least 80% (branches and functions)

## Methods to implement:
### Arrays:
* [chunk](https://lodash.com/docs/4.17.11#chunk)
* [compact](https://lodash.com/docs/4.17.11#compact)
* [drop](https://lodash.com/docs/4.17.11#drop)
* [dropWhile](https://lodash.com/docs/4.17.11#dropWhile)
* [take](https://lodash.com/docs/4.17.11#take)
* [filter](https://lodash.com/docs/4.17.11#filter)
* [find](https://lodash.com/docs/4.17.11#find)
* [includes](https://lodash.com/docs/4.17.11#includes)
* [map](https://lodash.com/docs/4.17.11#map)
* [zip](https://lodash.com/docs/4.17.11#zip)

### Objects:
* [merge](https://lodash.com/docs/4.17.11#merge)
* [omit](https://lodash.com/docs/4.17.11#omit)
* [omitBy](https://lodash.com/docs/4.17.11#omitBy)
* [pick](https://lodash.com/docs/4.17.11#pick)
* [pickBy](https://lodash.com/docs/4.17.11#pickBy)
* [toPairs](https://lodash.com/docs/4.17.11#toPairs)

### Scoring criteria (maximum 160 points)
You will get **10 points** for each method if you covered it fully (mean check not only correct way of method, but error cases as well. 
Example. Let's have the function sum(a, b), that summarizes two numbers. 
I should cover next cases: 
 * sum of positive numbers, 
 * sum of negative numbers, 
 * sum of fractional numbers, 
 * sum when one of numbers is 0, 
 * sum of infinitive numbers, 
 * sum when one of element is string, 
 * sum when one of function properties didn't provide, 
 * sum when one of properties is NaN
)

### Useful links
[Array](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)
[Object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object)
