## Key Takeaway
Challenge website: [click here]()

### `some()`
The [`some()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/some)
method tests whether at least one element in the array passes the test implemented by the provided function. It returns a Boolean value.  
Example:
<pre><code>
  const array = [1, 2, 3, 4, 5];

  // checks whether an element is even
  const even = (element) => element % 2 === 0;

  console.log(array.some(even));
  // expected output: true
</code></pre>

### `every()`
The [`every()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/every)
method tests whether all elements in the array pass the test implemented by the provided function. It returns a Boolean value.
Example:
<pre><code>
  const isBelowThreshold = (currentValue) => currentValue < 40;

  const array1 = [1, 30, 39, 29, 10, 13];

  console.log(array1.every(isBelowThreshold));
  // expected output: true
</code></pre>

### `find()`
The [`find()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/find) 
method returns the value of the first element in the provided array that satisfies the provided testing function.
Example:
<pre><code>
  const array1 = [5, 12, 8, 130, 44];

  const found = array1.find(element => element > 10);

  console.log(found);
  // expected output: 12
 </code></pre>
 
### `findIndex()`
The [`findIndex()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/findIndex) 
method returns the index of the first element in the array that satisfies the provided testing function. 
Otherwise, it returns -1, indicating that no element passed the test.
Example:
<pre><code>
  const array1 = [5, 12, 8, 130, 44];

  const isLargeNumber = (element) => element > 13;

  console.log(array1.findIndex(isLargeNumber));
  // expected output: 3
</code></pre>

### `splice()`
The [`splice()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/splice) 
method changes the contents of an array by removing or replacing existing elements and/or adding new elements in place.
Example: 
<pre><code>
  const months = ['Jan', 'March', 'April', 'June'];
  months.splice(1, 0, 'Feb');
  // inserts at index 1
  console.log(months);
  // expected output: Array ["Jan", "Feb", "March", "April", "June"]

  months.splice(4, 1, 'May');
  // replaces 1 element at index 4
  console.log(months);
  // expected output: Array ["Jan", "Feb", "March", "April", "May"]
</code></pre>

### `slice()`
The [`slice()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/slice) 
method returns a shallow copy of a portion of an array into a new array object selected from start to end (end not included) 
where start and end represent the index of items in that array. The original array will not be modified.
Example:
<pre><code>
  const animals = ['ant', 'bison', 'camel', 'duck', 'elephant'];

  console.log(animals.slice(2));
  // expected output: Array ["camel", "duck", "elephant"]

  console.log(animals.slice(2, 4));
  // expected output: Array ["camel", "duck"]

  console.log(animals.slice(1, 5));
  // expected output: Array ["bison", "camel", "duck", "elephant"]
</code></pre>
