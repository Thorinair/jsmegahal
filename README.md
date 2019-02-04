jsmegahal
=========

Implementation of the MegaHAL AI in JS for consumption with node.js

Installation
============
```
npm install github:Thorinair/jsmegahal
```

Sample Usage
============
```js
jsmegahal = require('jsmegahal');

// The first parameter lets you set the markov order you want to use. Defaults to 4.
// The second parameter lets you set the default reply when there is no data. Defaults to "".
// The third parameter lets you set the maximum number of loops. Defaults to 100.
var megahal = new jsmegahal(4, "I am jsmegahal.", 100);

// Add a single sentence.
megahal.add("This is a singular sentence and megahal will deconstruct it accordingly.");

// Add a lot of data.
megahal.addMass("This is a lot of data. Also, it is in multiple sentences!");

// Get a string based on the markov data -- this picks a random token in the sentence.
console.log(megahal.getReplyFromSentence("Pick a keyword"));

// Get a string based on the markob data -- this can take a token, or nothing at all.
console.log(megahal.getReply());
```

Projects Using This
===================
[alexa-chatterbot](https://github.com/moof2k/alexa-chatterbot)

[Princess-Luna](https://github.com/Thorinair/Princess-Luna)
