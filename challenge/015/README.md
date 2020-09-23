## Key Takeaway
Challenge website: [click here]()

### `JSON.parse()`
The [`JSON.parse()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/JSON/parse)
method parses a JSON string, constructing the JavaScript value or object described by the string.

### `localStorage`
The read-only [`localStorage`](https://developer.mozilla.org/en-US/docs/Web/API/Window/localStorage)
property allows you to access a [`Storage`](https://developer.mozilla.org/en-US/docs/Web/API/Storage)
object for the Document's origin; the stored data is saved across browser sessions.

### `preventDefault()`
The Event interface's [`preventDefault()`](https://developer.mozilla.org/en-US/docs/Web/API/Event/preventDefault) 
method tells the user agent that if the event does not get explicitly handled, its default action should not be taken as it normally would be.


### `JSON.stringify()`
The [`JSON.stringify()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/JSON/stringify) 
method converts a JavaScript object or value to a JSON string, 
optionally replacing values if a replacer function is specified or optionally including only the specified properties if a replacer array is specified.  
Example:
<pre><code>
  console.log(JSON.stringify({ x: 5, y: 6 }));
  // expected output: "{"x":5,"y":6}"

  console.log(JSON.stringify([new Number(3), new String('false'), new Boolean(false)]));
  // expected output: "[3,"false",false]"

  console.log(JSON.stringify({ x: [10, undefined, function(){}, Symbol('')] }));
  // expected output: "{"x":[10,null,null,null]}"

  console.log(JSON.stringify(new Date(2006, 0, 2, 15, 4, 5)));
  // expected output: ""2006-01-02T15:04:05.000Z""
 </code></pre>


### `e.target`
The [`target`](https://developer.mozilla.org/en-US/docs/Web/API/Event/target) 
property of the Event interface is a reference to the object onto which the event was dispatched. 
It is different from Event.currentTarget when the event handler is called during the bubbling or capturing phase of the event.


### `matches()`
The [`matches()`](https://developer.mozilla.org/en-US/docs/Web/API/Element/matches) 
method checks to see if the Element would be selected by the provided selectorString -- in other words -- checks if the element "is" the selector.
