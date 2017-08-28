# osu! Replay Parser
The ultimate osu! replay (.osr) parsing package that supports both osu! standard and osu!mania. It parses each replay frame in a clearly formatted object.

# Installation
* Install the package from npm `npm install osureplayparser --save`

# Usage
* It's best if you take a look at the example in the [tests](https://github.com/Swan/osuReplayParser/blob/master/tests/test-suite.js)
```js
const osuReplayParser = require('osureplayparser');

const replayPath = "./path/to/your/replay.osr";
const replay = osuReplayParser.parseReplay(replayPath);

console.log(replay);
```

# Documentation
The replay object returned is very simple, however it differentiates for both osu! and mania.

**Base Replay Data**

Here is the base data of what you'll get with every replay. You have all data that was parsed from the original package: [node-osr](https://github.com/vignedev/node-osr) plus some added stuff.
```json
{
  "gameMode": 3,
  "gameVersion": 20150414,
  "beatmapMD5": "c486f38146e0a14057ed1e3d3908c0c8",
  "playerName": "Swan",
  "replayMD5": "aed34df46c7c4a0f955edca59ca52fe1",
  "number_300s": 1384,
  "number_100s": 11,
  "number_50s": 6,
  "gekis": 1417,
  "katus": 89,
  "misses": 9,
  "score": 906808,
  "max_combo": 1161,
  "perfect_combo": 0,
  "mods": 0,
  "life_bar": "",
  "timestamp": "0001-01-01T00:00:00.000Z",
  "replay_length": 13625,
  "replay_data": [],
  "raw_replay_data": "0|256|1|0,0|256|1|0,0|256|1|0,0|256|1|0,0|256|1|0,0|256|1|0,0|256|1|0,0|256|1|0,0|256|1|0,0|256|1|0,0|256|1|0...."
```

**Replay Data**

The replay data object for mania and the other game modes are different. It should be self-explanatory and easy to read.

**osu! Standard Replay Data Example**

```json
{
  "timeSinceLastAction": 11,
  "x": 108.4803,
  "y": 187.5656,
  "keyPressedBitwise": 10,
  "keysPressed": {
    "K1": false,
    "K2": true,
    "M1": false,
    "M2": false
  }
},
```    
