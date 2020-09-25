# Keet Health Coding Challenge

Write a class called `Copier` which copies the given argument.  
The solution should be written in **Javascript**.

- You should be able to initialize the class using `new`
- The class should take 1 argument.
- The argument will be a value of type `string`, `integer`, or `object`, which can be a plain object or an instance of `Array`.
- If no argument is given, the argument should default to `undefined`
<!-- -->
- The class should implement a method `get()`, which returns the original object after 1 second.
- `get()` should return a `Promise`
<!-- -->
- The class should implement a method `delete()`, which throws an `Error` object after 2 seconds with the message `Cannot delete!`
- `delete()` should return a `Promise`
<!-- -->
- The class should implement a method called `copy()`.  
  If source value is an object, it should return a **deep copy** of the original object.
- `copy()` method should iterate over the source object recursively.
<!-- -->

```javascript
const src = 'a';
const copier = new Copier(src);
const dest = copier.copy();
// => a

const src = { a: 'b', c: { d: 'e', f: ['g', { h: 'i' }] } };
const copier = new Copier(src);
const dest = copier.copy();
// => { a: 'b', c: { d: 'e', f: ['g', { h: 'i' }] } }
dest === src;
// => false
```

Once you are satisfied with your work, write a few lines of code demonstrating each method.

### Requirements and Comments

- Do not use a utility library such as `lodash`.
- If the source value is an object, the resulting value should not equal the source.
- Above instructions specified `Promise`, but you are free to use either the class or `async/await` syntax.

### Additional Notes

- We just want to see how you code, so this exercise is not meant to be too hard or take too long.
- If you spend more than an hour on this, stop coding and finalize by adding some notes about what you would do if you had more time.
