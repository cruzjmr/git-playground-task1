# Notes

## Added `randomInt` helper to `lib/config.js`

Added a new function to the exported config object:

```js
// Returns a random integer between min and max (inclusive).
randomInt: (min, max) => Math.floor(Math.random() * (max - min + 1)) + min,
```

- **What it does:** returns a random whole number from `min` to `max`, including both ends.
- **Usage:**

  ```js
  const config = require('./lib/config');
  config.randomInt(1, 10); // e.g. 7
  ```

- **Impact:** the existing `SESSION_TIMEOUT_MINUTES` setting is unchanged.
