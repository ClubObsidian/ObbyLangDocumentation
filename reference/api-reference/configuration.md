---
description: 'ObbyLang supports configuration files written in: yaml, json, hocon and xml.'
---

# Configuration

## Loading a configuration file

```javascript
const config = configuration.load("file-name.yml");
```

{% hint style="info" %}
You can load any file from the configuration folder with the file extensions: yaml, json, conf or xml.
{% endhint %}

## Getting a value

{% code title="test.yml" %}
```yaml
foo: "bar"
```
{% endcode %}

```javascript
const config = configuration.load("test.yml");
const foo = config.get("foo");
```

You can see all the methods that you can use to get values here&#x20;

{% embed url="https://github.com/ClubObsidian/wrappy/blob/master/src/main/java/com/clubobsidian/wrappy/ConfigurationSection.java" %}
