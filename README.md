# JSON HELPER

This project provides utility functions to easily read, write, and modify JSON files. Using simple functions, you can easily handle Json data.

## Installation

To install and use this project, follow the steps below.

1. Running this command on terminal.

```
npm install help-json
```

2. Once installed, you're ready to use the functions :

- loadJSON: Reads a JSON file and converts it into an object.

- saveJSON: Saves an object to a JSON file.

- updateJSON: Updates a specific key's value in the JSON file.

- addKeyToJSON: Adds a new key-value pair to the JSON file.

- prettyPrintJSON: Pretty prints a JSON object.

## Function Usage

1. `loadJson(filePath)`

This function reads a JSON file and converts it into a JavaScript object.

Example
```js
loadJSON('data.json')
    .then((data) => {
        console.log('Loaded JSON data:', data);
    })
    .catch((error) => {
        console.error(error);
    });
```

2. `saveJSON(filePath, data)`

This function saves a JavaScript object as a JSON file.

Example
```js
const data = { name: 'Alice', age: 25 };
saveJSON('data.json', data)
    .then((message) => {
        console.log(message); 
    })
    .catch((error) => {
        console.error(error); 
    });

```

3. `updateJSON(filePath,key,value)`

This function reads a JSON file, updates the value of a specific key, and then saves it.

Example
```js
updateJSON('data.json', 'age', 30);
```

4. `addKeyToJSON(filePath, key, value)`

This function adds a new key-value pair to the JSON file.

Example

```js
addKeyToJSON('data.json', 'address', '123 Main St');
```

5. `prettyPrintJSON(data)`

This function pretty prints a JSON object for easier readability, typically useful for debugging.

Example

```js
prettyPrintJSON({ name: 'Bob', age: 40 });
```


## Use Cases

This utility makes it easy to handle JSON files. For example, it can be useful in applications that use JSON files as a lightweight database.

## Contributing

Feel free to submit a Pull Request if you would like to contribute. Contributions for new features or bug fixes are always welcome!

## License

MIT License.
