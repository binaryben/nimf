<br /><br /><div align="center">

# ⚙️ Nim Conf
<br />

![ISC License](https://img.shields.io/badge/license-ISC-green?style=for-the-badge) &nbsp; ![Project Status](https://img.shields.io/badge/status-💡%20PROPOSAL-yellow?style=for-the-badge)

<strong>Simple config handling for ~~Node~~ <ins>Nim</ins> — directly inspired by [sindresorhus/conf](https://github.com/sindresorhus/conf)</strong><br />
<sub>The `nimf` library handles all of the dull details of how and where to store simple config data. Just like `conf`, all you have to care about is what to persist.</sub>

<br /></div>

![Divider](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/solar.png)

## ✨ &nbsp; Core features

* Support for JSON and INI formats

![Divider](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/solar.png)

## ⌛️ &nbsp; Quick start

### Installation

```shell
$ nimble install nimf
```

### Basic usage

```nim
import nimf

let config = nimf()

config.set("example", "foobar")
echo config.get("example")
# foobar

# Use dot-notation to access nested properties
config.set('foo.bar', true)
echo config.get('foo')
# true (bool)

config.delete('example')
echo config.get('example')
# empty string
```

### Define a schema

```nim
const schema = 
```


![Divider](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/solar.png)

## 📝 &nbsp; API Docs

Full documentation can be found below for:

* [Configuration](#)
  * [Options](#)
  * [Schema](#)
* [Instance methods](#)
  * [.get()](#)
  * [.set()](#)
  * [.reset()](#)
  * [.clear()](#)
  * [.has()](#)
  * [.delete()](#)
  * [.size()](#)
  * [.store()](#)
  * [.path()](#)
  * [.validate()](#)