# osu! Replay Parser
The ultimate osu! replay (.osr) parsing package that supports both osu! standard and osu!mania. It parses each replay frame in a clearly formatted object.

# Installation & Usage
* Install the package from npm `npm install osureplayparser --save`
* Import the package and follow the basic usage guide: 

```js
const osuReplayParser = require('osureplayparser');

const replayPath = "./path/to/your/replay.osr";
const replay = osuReplayParser.parseReplay(replayPath);

console.log(replay);
```
