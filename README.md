# better-cl

## Setup

### Install

```bash
npm install better-cl
```

### Usage

#### Bare minimum

```javascript
require("better-cl").setup();
```

#### With options

```javascript
require('better-cl').setup(console, methods, path, showTimestamp, showLabel);
```

`console` the console object to override. The standard `console` object is the default.

`levels` is an array of additional methods to add to the console object. The default methods are `log`, `warn`, `error`, `info`, `debug` and `success`. The default is `[]`.

`path` is the location of the logs folder. if undefined, no logs will be saved. The default is `undefined`.

`showTimestamp` is a boolean, if true, the timestamp will be shown. The default is `true`.

`showLabel` is a boolean, if true, the label will be shown. The default is `true`.

## Example

### Code

```javascript
require("better-cl").setup(console, [
{
  name:"simple",
  value: 1,
  color: "red"
}
], "logs");
console.simple("A simple example.");
```

### Output

```txt
[hh:mm:ss.ddd] [SIMPLE] A simple example.
```
