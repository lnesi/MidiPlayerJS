# &#9836; MidiPlayerJS
[![npm version](https://badge.fury.io/js/midi-player-js.svg)](https://badge.fury.io/js/midi-player-js)
[![Build Status](https://travis-ci.org/grimmdude/MidiPlayerJS.svg?branch=master)](https://travis-ci.org/grimmdude/MidiPlayerJS)

MidiPlayerJS is a JavaScript library which reads standard MIDI files and emits JSON events in real time.  This player does not generate any audio, but by attaching a handler to the event emitter you can trigger any code you like which could play audio, control visualizations, feed into a MIDI interface, etc.

## Getting Started
Using MidiWriterJS is pretty simple.  Just create a new player by instantiating `MidiPlayer.Player` with an event handler.  Then you can load and play a MIDI file.  The event handler passed to the player constructor will be called for every MIDI event in real time while playing.
```javascript
var MidiPlayer = require('midi-player-js');

var Player = new MidiPlayer.Player(function(event) {
	console.log(event);
});

Player.loadFile('./test.mid');
Player.play();
```
## Documentation
### `MidiPlayer.Player`
* `disableTrack(trackNumber)`
* `enableTrack(trackNumber)`
* `isPlaying()`
* `loadArrayBuffer(arrayBuffer)`
* `loadDataUri(dataUri)`
* `loadFile(filePath)`
* `pause()`
* `play()`
* `stop()`
