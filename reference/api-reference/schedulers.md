# Schedulers

## Creating a synchronous task

```javascript
scheduler.sync(owner, () => { //This will run one tick after it is queued
  //Do something on the main thread
});
```

## Creating a repeating synchronous task

```javascript
scheduler.syncRepeating(owner, () => {
  //Do something that repeats
}, 1000, 1000); 
//Time in millis for how over it should repeat
```

{% hint style="info" %}
Remember that a tick is 50 milliseconds
{% endhint %}

## Creating a asynchronous task

```javascript
scheduler.async(owner, () => {
  //Do something that runs on a seperate thread
});
```

## Creating a repeating asynchronous task

```javascript
scheduler.asyncRepeating(owner, () => {
  //Do something that repeats on a seperate thread
}, 1000, 1000);
```
