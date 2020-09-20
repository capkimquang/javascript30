## Key Takeaway
Challenge website: [click here]()

### Arrow function
Read more about arrow function [here](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Arrow_functions)

### `filter()`
The [`filter()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/filter)
method creates a new array with all elements that pass the test implemented by the provided function.  
Example:
<pre><code>
  const words = ['spray', 'limit', 'elite', 'exuberant', 'destruction', 'present'];
  const result = words.filter(word => word.length > 6);
  console.log(result);
  // expected output: Array ["exuberant", "destruction", "present"]
</code></pre>

### `map()`
The [`map()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map)
method creates a new array populated with the results of calling a provided function on every element in the calling array.  
Example: 
<pre><code>
const array1 = [1, 4, 9, 16];
// pass a function to map
const map1 = array1.map(x => x * 2);
console.log(map1);
// expected output: Array [2, 8, 18, 32]
</code></pre>

### `sort()`
The [`sort()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/sort)
method sorts the elements of an array in place and returns the sorted array. 
The default sort order is ascending, built upon converting the elements into strings, then comparing their sequences of UTF-16 code units values.  
Example:
<pre><code>
  const months = ['March', 'Jan', 'Feb', 'Dec'];
  months.sort();
  console.log(months);
  // expected output: Array ["Dec", "Feb", "Jan", "March"]

  const array1 = [1, 30, 4, 21, 100000];
  array1.sort();
  console.log(array1);
  // expected output: Array [1, 100000, 21, 30, 4]
</code></pre>

### `reduce()`
The [`reduce()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/reduce)
method executes a reducer function (that you provide) on each element of the array, resulting in single output value.
Example: 
<pre><code>
  const array1 = [1, 2, 3, 4];
  const reducer = (accumulator, currentValue) => accumulator + currentValue;

  // 1 + 2 + 3 + 4
  console.log(array1.reduce(reducer));
  // expected output: 10

  // 5 + 1 + 2 + 3 + 4
  console.log(array1.reduce(reducer, 5));
  // expected output: 15
</code></pre>

### `split()`
The [`split()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/split) 
method divides a String into an ordered list of substrings, puts these substrings into an array, and returns the array.  
The division is done by searching for a pattern; where the pattern is provided as the first parameter in the method's call.  
Example:
<pre><code>
  const str = 'The quick brown fox jumps over the lazy dog.';

  const words = str.split(' ');
  console.log(words[3]);
  // expected output: "fox"

  const chars = str.split('');
  console.log(chars[8]);
  // expected output: "k"

  const strCopy = str.split();
  console.log(strCopy);
  // expected output: Array ["The quick brown fox jumps over the lazy dog."]
</code></pre>

