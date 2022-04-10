---
title: JS Mocha and Chai
---
Status:
Tags:
Links: [Behavior Driven Development](out/behavior-driven-development.md) - [JavaScript Debugging](out/javascript-debugging.md)
___
# JS Mocha and Chai
## Principles
JS libs used for BDD
## Practices
- User-friendly testing of functions
- `describe(name, function() )` sets a header for the debugging ui
- `it(name, function() )` writes the description of the test made and the actual test being made
- `assert.equal( function() , expected)` runs the tested function and compares it to the expected result
	- Also other versions of assert
- - `before( function() )` and `after( function() )` run before and after describe content
- `beforeEach( function() )` and `afterEach( function() )` run before and after tests
___
References: https://javascript.info/testing-mocha

Created:: 2021-05-28 18:56 PM