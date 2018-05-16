# EventEmitter
What is Event Emitter?

## Getting Started
```js
let input = document.querySelector('input[type="text"]');
let button = document.querySelector('button');
let h1 = document.querySelector('h1');
let unsubscribe;
button.addEventListener('click', () => {
    emitter.emit('event:name-changed', {
        name: input.value
    });
    unsubscribe();
});

let emitter = new EventEmitter();
unsubscribe = emitter.subscribe('event:name-changed', data => {
    h1.innerHTML = `Your name is: ${data.name}, ${Date.now()}`;
});
```
