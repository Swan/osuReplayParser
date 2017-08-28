# osu! Replay Parser
The ultimate osu! replay (.osr) parsing package that supports both osu! standard and osu!mania. It parses each replay frame in a clearly formatted object.

# Installation & Usage
* Install the package from npm `npm install osureplayparser --save`

```js
const osuReplayParser = require('osureplayparser');

const replay = osuReplayParser.parseReplay(replayPath);
console.log(replay);
```
