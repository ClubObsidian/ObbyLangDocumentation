# Quick Start

## Creating a script

We are going to assume that you have the plugin installed already, if you don't you should do that first. Once that is done navigate to `plugins/ObbyLang/scripts` and create a file named `test.js`

## Creating a listener

```javascript
listener.register(owner, (event) => {
  const player = event.getPlayer();
  player.sendMessage("Hello World!");
}, "BlockPlaceEvent");ja
```

## Creating a command

```javascript
command.register(owner, (sender, cmd, label, args) => {
  sender.sendMessage("Hello World!");
}, "test");j
```

## Working with commands

The base command for ObbyLang is /obbylang or /ol. Below you will find the usage of the ObbyLang commands.

/obbylang - Shows the help map

/obbylang reload \<script> - Reloads a script with the specified name

/obbylang unload \<script> - Unloads a script, will be loaded on next restart

/obbyland disable \<script> - Disabled a script, renames it to scriptname.js.dis

/obbylang enable \<script> - Enables a previously disabled script
