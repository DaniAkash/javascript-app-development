# Event Emitter
## Events
We all know that Node JS is an asynchronous, Event-Driven model.
To explain events in a simpler way, suppose if one particular action takes place, then the event has been triggered to do some function for that action. Like if we double click the folder it immediately emits the function to open the folder and show the files in that folder.

> In node js most of its core APIs are built on this event driven method where the objects emit some  action when they listen to events.

**For example,**
In http module the server listens to a port, If any request (event) has been sent to that port it emits an function and gives back the response for that corresponding request.

- Node js helps us to create and handle our own custom events with the help of `EventEmitter` class which lies `inside the Event module`.
- All the objects that emit the events belong to the EventEmitter class.
- Whenever the EventEmitter objects emits an event, all the functions that are attached to that events are called synchronously.

## Initiating EvenEmitter
```javascript
// Importing the EventEmitter class of events module
const { EventEmitter } = require('events');

//create an object of EventEmitter class
const customEventEmitter = new EventEmitter();
```
As we mentioned earlier EventEmitter is a class,
- In the above piece of code we are importing that particular class from the events module.
- Then we are creating an instance customEventEmitter for that class.

## emit () and on ()
There are lot of events available for this EventEmitter class, First we are going to see the two most important methods.
- `on()` - It will add (register) a listener to an event. It has two parameters event name and the callback funtion.
- `emit()` - It contains the event name. It will trigger the event that is mentioned in the parameter.

```javascript
const { EventEmitter } = require('events');
const customEventEmitter = new EventEmitter();

function choosePokemon(){
	console.log("I Choose Pikachu");
}
// Registering our first event
customEventEmitter.on("pokemon",choosePokemon);

//Firing our event
customEventEmitter.emit("pokemon");
```
Here first we are adding our event listener with a event name pokemon, Then the pokemon event has been fired/triggered. Now the listener will execute the callback function and print the output.

## Multiple Listeners
```javascript
const { EventEmitter } = require('events');
const customEventEmitter = new EventEmitter();

function choosePokemon(){
	console.log("I Choose Pikachu");
}
// Registering multiple listener for particular event
customEventEmitter.on("pokemon",choosePokemon);
customEventEmitter.on("pokemon",choosePokemon);
customEventEmitter.on("pokemon",choosePokemon);

//Firing our event
customEventEmitter.emit("pokemon");

//ouput
I Choose Pikachu
I Choose Pikachu
I Choose Pikachu
```
In this multiple listeners are listening to the event. when the event is fired all the listeners for that event will be executed synchronously.

**Procedure to write listeners**
```javascript
const { EventEmitter } = require('events');
const customEventEmitter = new EventEmitter();

function choosePokemon(){
	console.log("I Choose Pikachu");
}

customEventEmitter.on("pokemon",choosePokemon);

customEventEmitter.emit("pokemon");

customEventEmitter.on("pokemon",choosePokemon);  // It won't be triggered

//ouput
I Choose Pikachu

```
In this case the the second listener wont be triggered because the emit method will trigger all the listeners that are declared above them in a synchronous manner.

There are lot of other methods that can be used with  the EventEmitter, some of them were listed below :

|  Method | Description  |
| :------------: | :------------: |
| once(event, listener) | Adds a listener at the end of the listeners array for the specified event. No checks are made to see if the listener has already been added. Multiple calls passing the same combination of event and listener will result in the listener being added multiple times. Returns emitter, so calls can be chained.  |
| removeListener(event, listener) | Removes all listeners, or those of the specified event. It's not a good idea to remove listeners that were added elsewhere in the code, especially when it's on an emitter that you didn't create (e.g. sockets or file streams). Returns emitter, so calls can be chained.  |
|  setMaxListeners(n) | By default, EventEmitters will print a warning if more than 10 listeners are added for a particular event. This is a useful default which helps finding memory leaks. Obviously not all Emitters should be limited to 10. This function allows that to be increased. Set to zero for unlimited.|
|   listeners(event) | Returns an array of listeners for the specified event. |


