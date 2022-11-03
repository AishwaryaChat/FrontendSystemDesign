# Event Emitter

## Problem Statement

Implement an EventEmitter that supports following standard operations

1. EventEmitter.on(): Adding a listener
2. EventEmitter.emit(eventName): Emiting an event
3. EventEmitter.off(eventName, listener): Remove the given listener
4. EventEmitter.once(eventName, listener): Register the event, call it only once

## Solution Guidelines

Implement the solution using vanila javascript.

Run the following expressions to test your implementation

```js
let EventEmitter = new eventEmitter();
EventEmitter.on("pramp", responseToEvent);
EventEmitter.emit("pramp", "1st"); // 1st
EventEmitter.emit("pramp", "2nd"); // 2nd
EventEmitter.once("pramp", function (msg) {
    console.log(msg + " just once!");
});
EventEmitter.off("pramp", responseToEvent);
EventEmitter.emit("pramp", "3rd"); // 3rd  just once!
EventEmitter.emit("pramp", "1st"); // blank, since the listeners were removed
```
