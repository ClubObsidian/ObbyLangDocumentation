# Commands

## Creating a command

```javascript
command.register(owner, (sender, cmd, label, args) => {
  sender.sendMessage("Hello World!");
}, "test");
```

{% hint style="info" %}
**Good to know:** This API method was created using the API Method block, it's how you can build out an API method documentation from scratch. Have a play with the block and you'll see you can do some nifty things like add and reorder parameters, document responses, and give your methods detailed descriptions.
{% endhint %}

## Checking command arguments

```javascript
command.register(owner, (sender, cmd, label, args) => {
  if(args.length == 1 && args[0] === "bar") {
    sender.sendMessage("foo bar");
    return true;
  }
  sender.sendMessage("Incorrect arguments use /foo foo");
  return true;
}, "foo");
```

## Checking if command sender is a player

```javascript
command.register(owner, (sender, cmd, label, args) => {
  if(sender.isPlayer()) {
    const player = sender.asPlayer();
    const loc = player.getLocation();
    const x = loc.getBlockX();
    const y = loc.getBlockY();
    const z = loc.getBlockZ();
    sender.sendMessage("Your current location is: " + x + ", " + y + ", " + z); 
    return true;
  }
  return true;
}, "checkloc");
```

{% hint style="info" %}
**Good to know:** This API method was auto-generated from an example Swagger file. You'll see that it's not editable – that's because the contents are synced to an URL! Any time the linked file changes, the documentation will change too.
{% endhint %}

## Registering multiple command aliases

```javascript
command.register(owner, (sender, cmd, label, args) => {
  if(label === "test1") {
    //Do something
    return true;  
  } 
  //Do something else
  return true;
}, "test", "test1", "test2");
```
