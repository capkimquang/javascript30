## Key Takeaway
Challenge website: [click here]()

### Regular Expressions
Read more about Regular Expressions [here](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_Expressions)
#### RegExp
The [RegExp](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/RegExp)
object is used for matching text with a pattern.
#### Regular Expression flags
Regular expressions have six optional flags
that allow for functionality like global and case insensitive searching. 
These flags can be used separately or together in any order, and are included as part of the regular expression.
Example:
<pre><code>
  var re = /pattern/flags;
  var re = new RegExp('pattern', 'flags');
</code></pre>

### `match()`
The [`match()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/match)
method retrieves the result of matching a string against a regular expression.  
Example:
<pre><code>
  const paragraph = 'The quick brown fox jumps over the lazy dog. It barked.';
  const regex = /[A-Z]/g;
  const found = paragraph.match(regex);

  console.log(found);
  // expected output: Array ["T", "I"]
</code></pre>

### `join()`
The [`join()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/join) 
method creates and returns a new string by concatenating all of the elements in an array (or an array-like object), 
separated by commas or a specified separator string. If the array has only one item, then that item will be returned without using the separator.  
Example:
<pre><code>
  const elements = ['Fire', 'Air', 'Water'];

  console.log(elements.join());
  // expected output: "Fire,Air,Water"

  console.log(elements.join(''));
  // expected output: "FireAirWater"

  console.log(elements.join('-'));
  // expected output: "Fire-Air-Water"
</code></pre>

### Element.innerHTML
Read more about innerHTML [here](https://developer.mozilla.org/en-US/docs/Web/API/Element/innerHTML)


