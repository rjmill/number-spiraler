#TODO

- [ ] publish the module on npm
- [ ] rename n to currentNumber
- [ ] probably define the getters outside the returned object in SpiralMaker
- [ ] decide how error handling should work
  - I should probably wait to see how callback-y this ends up being
- [ ] sanitize input
  - numbers only
  - no negatives
  - no zero
- [ ] look into reorganizing the logic for the directions. Have directions just
be an object with each direction and the function for the movement logic. Then
do the other steps involved elsewhere.
- [ ] find a sensible way to get private methods and variables in es6 classes.
- [ ] put es6 version on github
- [ ] update the es6 version to more closely match the es5 version
- [ ] wire up babel to make the es6 version actually work
- [ ] improve documentation.
- [ ] I want a composable filter step to basically define a bunch of filters
that are evaluated.
  - do I really though? For now, it seems a tad unnecessary.
- [ ] see if there isn't a way to make the grid elements more expressive.
  - it looks like in JavaScript, Arrays are just Objects with numbers as keys.
  If this is the case, is the potential performance hit of using objects instead
  of arrays significant enough to justify not using objects?
  - test that.
- [ ] write SpiralMaker so that it doesn't segfault with obscenely large numbers
  - why yes, I did manage to get a literal segfault in JavaScript. I am both
  proud and ashamed.
  - incredibly low priority for now. It works well enough for what I want.
- [ ] play more with performance
- [x] get rid of default size functionality
- [x] write the tests
- [x] modify the point setting function to be more flexible with how it tags
primes. As of right now, it's practically useless for tagging other things.
  - probably use plaintext flags for that, so you can use them as classes
  verbatim and for legibility
  - for now, I've switched it to each element being an array with the index 0
  containing the number, and each element after it containing tags
- [x] add a flag to each number to show primality (make it flexible enough to
easily add filtering divisibility by any old number)
- [x] write a function to render the grid
  - this is not in the repo at this point because it feels dirty to combine the
  rendering logic in the same module as the grid logic. That being said, I did
  it in a jsfiddle here: https://jsfiddle.net/rjmill/125uue4h/2/
  - [ ] make a repo that includes the rendering logic
- [x] do whatever needs to be done to make this an actual importable npm module
- [x] write a prime number checker (don't you dare optimize it yet though)
  - [ ] ~~go ahead and optimize it. This is low priority for now, since the way
  it is now, it runs plenty fast.~~ _That logic isn't part of this module
  anymore_
- [x] extract prime seive out of the SpiralMaker module. It doesn't fit in
logically, and now that I've got the filterGrid function, we don't need it in
there.
- [x] filter functions that can run on already made spirals.
