This is a repository for 30 different projects written in JavaScript based on WesBos's course: [#JavaScript30](https://javascript30.com). You can find my result [here](https://javascript30project.herokuapp.com).
# Content
1. [Projects List](#project-list)
2. [Key Concept](#key-concept)
3. [Progress](#progress)
4. [References](#references)

# Project List
- [X] [01. JavaScript Drum Kit - 19/09/2020](https://github.com/capkimquang/javascript30/tree/master/challenge/01)
- [X] [02. CSS + JS Clock - 19/09/2020](https://github.com/capkimquang/javascript30/tree/master/challenge/02)
- [X] [03. Playing with CSS variables and JS - 20/09/2020](https://github.com/capkimquang/javascript30/tree/master/challenge/03)
- [X] [04. Array Cardio Day 1 - 20/09/2020](https://github.com/capkimquang/javascript30/tree/master/challenge/04)
- [X] [05. Flex Panels Image Gallery - 21/09/2020](https://github.com/capkimquang/javascript30/tree/master/challenge/05)
- [X] [06. Ajax Type Ahead - 21/09/2020](https://github.com/capkimquang/javascript30/tree/master/challenge/06)
- [X] [07. Array Cardio Day 2 - 21/09/2020](https://github.com/capkimquang/javascript30/tree/master/challenge/07)
- [X] [08. Fun with HTML5 Canvas - 21/09/2020](https://github.com/capkimquang/javascript30/tree/master/challenge/08)
- [X] [09. 14 Must Know Dev Tool Tricks - 22/09/2020](https://github.com/capkimquang/javascript30/tree/master/challenge/09)
- [X] [10. Hold Shift to Check Multiple Checkboxes - 22/09/2020](https://github.com/capkimquang/javascript30/tree/master/challenge/010)
- [X] [11. Custom HTML5 Video Player - 22/09/2020](https://github.com/capkimquang/javascript30/tree/master/challenge/011)
- [X] [12. Key Sequence Detection (KONAMI CODE) - 23/09/2020](https://github.com/capkimquang/javascript30/tree/master/challenge/012)
- [X] [13. Slide In on Scroll - 23/09/2020](https://github.com/capkimquang/javascript30/tree/master/challenge/013)
- [X] [14. Object and Arrays - Reference VS Copy - 23/09/2020](https://github.com/capkimquang/javascript30/tree/master/challenge/014)
- [X] [15. LocalStorage and Event Delegation - 23/09/2020](https://github.com/capkimquang/javascript30/tree/master/challenge/015)
- [X] [16. CSS Text Shadow Mouse Move Effect - 24/09/2020](https://github.com/capkimquang/javascript30/tree/master/challenge/016)
- [X] [17. Sorting Band Names without articles - 24/09/2020](https://github.com/capkimquang/javascript30/tree/master/challenge/017)
- [X] [18. Tally String Times with Reduce - 24/09/2020](https://github.com/capkimquang/javascript30/tree/master/challenge/018)
- [X] [19. Unreal Webcam Fun - 25/09/2020](https://github.com/capkimquang/javascript30/tree/master/challenge/019)
- [X] [20. Native Speech Recognition - 25/09/2020](https://github.com/capkimquang/javascript30/tree/master/challenge/020)
- [X] [21. Geolocation based Speedometer and Compass - 25/09/2020](https://github.com/capkimquang/javascript30/tree/master/challenge/021)
- [X] [22. Follow Along Links - 25/09/2020](https://github.com/capkimquang/javascript30/tree/master/challenge/022)
- [X] [23. Speech Synthesis - 25/09/2020](https://github.com/capkimquang/javascript30/tree/master/challenge/023)
- [X] [24. Sticky Nav - 25/09/2020](https://github.com/capkimquang/javascript30/tree/master/challenge/024)
- [X] [25. Event Capture, Propagation, Bubbling and Once - 25/09/2020](https://github.com/capkimquang/javascript30/tree/master/challenge/025)
- [X] [26. Stripe Follow Along Dropdown - 25/09/2020](https://github.com/capkimquang/javascript30/tree/master/challenge/026)
- [ ] 27. Click and Drag to Scroll
- [ ] 28. Video Speed Controller UI
- [ ] 29. Countdown Clock
- [ ] 30. Whack A Mole Games
- [ ] 31. That's All Folks

# Key Concept
## Callback function
### Definition
A callback function is a function passed into another function as an argument, 
which is then invoked inside the outer function to complete some kind of routine or action.  
### Example
<pre><code>
  function greeting(name) {
    alert('Hello ' + name);
  }

  function processUserInput(callback) {
    var name = prompt('Please enter your name.');
    callback(name);
  }

  processUserInput(greeting);
</code></pre>
### Asynchronous and Synchronous

### Callback Hell
#### Definition
This is a big issue caused by coding with complex nested callbacks. Here, each and every callback takes an argument that is a result of the previous callbacks. In this manner, The code structure looks like a pyramid, making it difficult to read and maintain. Also, if there is an error in one function, then all other functions get affected. (from [GeeksforGeeks](https://www.geeksforgeeks.org/what-is-callback-hell-in-node-js/))

#### [Constructing a Callback Hell](https://www.freecodecamp.org/news/how-to-deal-with-nested-callbacks-and-avoid-callback-hell-1bc8dc4a2012/)
Let’s imagine we’re trying to make a burger. To make a burger, we need to go through the following steps:
1. Get ingredients (we’re gonna assume it’s a beef burger)
2. Cook the beef
3. Get burger buns
4. Put the cooked beef between the buns
5. Serve the burger

If these steps are synchronous, you’ll be looking at a function that resembles this:
<pre><code>
  const makeBurger = () => {
    const beef = getBeef();
    const patty = cookBeef(beef);
    const buns = getBuns();
    const burger = putBeefBetweenBuns(buns, beef);
    return burger;
  };

  const burger = makeBurger();
  serve(burger);
</code></pre>
However, in our scenario, let’s say we can’t make the burger ourselves. We have to instruct a helper on the steps to make the burger. After we instruct the helper, we have to WAIT for the helper to finish before we begin the next step.

If we want to wait for something in JavaScript, we need to use a callback. To make the burger, we have to get the beef first. We can only cook the beef after we get the beef.
<pre><code>
const makeBurger = () => {
  getBeef(function(beef) {
    // We can only cook beef after we get it.
  });
};
</code></pre>
To cook the beef, we need to pass beef into the cookBeef function. Otherwise, there’s nothing to cook! Then, we have to wait for the beef to get cooked.

Once the beef gets cooked, we get buns.
<pre><code>
const makeBurger = () => {
  getBeef(function(beef) {
    cookBeef(beef, function(cookedBeef) {
      getBuns(function(buns) {
        // Put patty in bun
      });
    });
  });
};
</code></pre>
After we get the buns, we need to put the patty between the buns. This is where a burger gets formed.
<pre><code>
const makeBurger = () => {
  getBeef(function(beef) {
    cookBeef(beef, function(cookedBeef) {
      getBuns(function(buns) {
        putBeefBetweenBuns(buns, beef, function(burger) {
            // Serve the burger
        });
      });
    });
  });
};
</code></pre>
Finally, we can serve the burger! But we can’t return burger from makeBurger because it’s asynchronous. We need to accept a callback to serve the burger.
<pre><code>
const makeBurger = nextStep => {
  getBeef(function (beef) {
    cookBeef(beef, function (cookedBeef) {
      getBuns(function (buns) {
        putBeefBetweenBuns(buns, beef, function(burger) {
          nextStep(burger)
        })
      })
    })
  })
}

// Make and serve the burger
makeBurger(function (burger) => {
  serve(burger)
})
</code></pre>
### References for Callback function
- [Callback Hell in Node.js by GeeksforGeeks](https://www.geeksforgeeks.org/what-is-callback-hell-in-node-js/)
- [Deal with Callback Hell by freecodecamp.com](https://www.freecodecamp.org/news/how-to-deal-with-nested-callbacks-and-avoid-callback-hell-1bc8dc4a2012/)

## Promise
## Prototype
## fetch()
## this
## Event Delegation
## JSON
## localStorage

# Progress
<pre>
- Day 01 - 19/09/2020: **2** *projects*. => 02/31    => 0% |#                   | 100%
- Day 02 - 20/09/2020: **2** *projects*. => 04/31    => 0% |##                  | 100%
- Day 03 - 21/09/2020: **4** *projects*. => 08/31    => 0% |#####               | 100%
- Day 04 - 22/09/2020: **3** *projects*. => 11/31    => 0% |#######             | 100%
- Day 05 - 23/09/2020: **4** *projects*. => 15/31    => 0% |#########           | 100%
- Day 06 - 24/09/2020: **3** *projects*. => 18/31    => 0% |###########         | 100%
- Day 07 - 25/09/2020: **4** *projects*. => 22/31    => 0% |##############      | 100%
- Day 08 - 26/09/2020: **0** *projects*. => 22/31    => 0% |##############      | 100%
- Day 09 - 27/09/2020: **0** *projects*. => 22/31    => 0% |##############      | 100%
- Day 10 - 28/09/2020: **0** *projects*. => 22/31    => 0% |##############      | 100%
- Day 11 - 29/09/2020: **4** *projects*. => 26/31    => 0% |################    | 100%


</pre>

# References
- [How to Run a Simple HTML/CSS/Javascript Application on Heroku](https://medium.com/@winnieliang/how-to-run-a-simple-html-css-javascript-application-on-heroku-4e664c541b0b)
