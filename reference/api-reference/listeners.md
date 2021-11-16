# Listeners

## Creating a listener

```javascript
listener.register(owner, (event) => {
  const player = event.getPlayer();
  player.sendMessage("Hello World!");
}, "BlockPlaceEvent");
```

## Registering with a different event priority

```javascript
listener.register(owner, (event) => {
  const player = event.getPlayer();
  player.sendMessage("Hello World!");
}, "BlockPlaceEvent", "LOWEST");
```

{% hint style="info" %}
Events can have different priority and they run in the specified order

* LOWEST
* LOW
* NORMAL
* HIGH
* HIGHEST
* MONITOR
{% endhint %}

## Unregistering script listeners

```javascript
listener.unregister(owner);
```

{% hint style="info" %}
Listeners are already unregistered when a script is unloaded, disabled or reloaded but you can still unregister a listener if you need to.
{% endhint %}

##

