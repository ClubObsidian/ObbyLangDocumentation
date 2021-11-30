# Commands

## Creating a command

```javascript
command.register(owner, (sender, cmd, label, args) => {
  sender.sendMessage("Hello World!");
}, "test");
```

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

## Checking if a command sender is a player

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

## Registering multiple command aliases

```javascript
command.register(owner, (sender, cmd, label, args) => {
  if(label === "test1") {
    //Do something
    return true;  
  } 
  //Do something else
  return true;
}, ["test", "test1", "test2"]);
```
