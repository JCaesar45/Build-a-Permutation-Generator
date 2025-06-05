````markdown
# Permutation Generator

## Project Overview
This project implements a **Permutation Generator** function in JavaScript that takes a string input and returns all possible unique permutations of its characters. It uses recursion to generate permutations and ensures that duplicates are removed from the results.

---

## Features
- Generates all permutations of the input string.
- Handles strings with duplicate characters by returning only unique permutations.
- Supports empty strings and single-character strings.
- Uses recursion for elegant and efficient permutation generation.

---

## Function Signature
```javascript
function permuteString(str, prefix = "", results = [])
```

### Parameters

* `str` (string): The input string to generate permutations for.
* `prefix` (string): A helper string used to accumulate characters for the current permutation (default is an empty string).
* `results` (array): An array to store the unique permutations (default is an empty array).

### Returns

* An array of unique permutation strings.

---

## How It Works

1. The function checks if the input string `str` is empty.

   * If empty, it adds the current `prefix` (which holds a full permutation) to the results array (if not already included).
2. If not empty, the function loops through each character in `str`.
3. For each character, it:

   * Removes the character from `str`.
   * Adds the character to the `prefix`.
   * Recursively calls itself with the updated `str` and `prefix`.
4. This continues until all characters have been used and all unique permutations have been generated.

---

## Usage Example

```javascript
console.log(permuteString("cat"));
// Output: ["cat", "cta", "act", "atc", "tca", "tac"]

console.log(permuteString("fcc"));
// Output: ["fcc", "cfc", "ccf"]
```

---

## Testing

The function has been tested with:

* Regular strings (e.g., `"far"`, `"walk"`)
* Strings with duplicate characters (e.g., `"fcc"`)
* Single character strings (e.g., `"p"`)
* Empty strings (`""`)

---

## Installation & Running

This is a pure JavaScript function and can be run in any JavaScript environment including browsers or Node.js.

1. Copy the function into your JavaScript file.
2. Call the function with the desired string.
3. Capture the returned array of permutations.

---

## License

This project is open source and free to use.

---

## Author

Created by \[Your Name]

---

Feel free to reach out if you want enhancements or integration help!

```
