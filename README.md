# beatmachine
record samples directly from your record player and make instant music.

## Usage

Make sure you have Max 8 installed. Before opening Max, plug your USB turntable and your MIDI controller into your computer.

Open Max and navigate to `Options > Audio Status...` Set the Input Device to your USB turntable. Test the audio by turning on audio in Max (click bottom right power button and any `startwindow` message). Then, play something on your turntable. You should hear the audio coming from Max. If not, further debugging is required.... 

To record, locate your `horiz/slider/01` and press it. This puts you in `record` mode. Now, when you press and hold any one of your pads, you map whatever audio is playing during the duration of the press to that pad as a sample. 

Note: The odot route objects currently are mapped to an AKAI MPK Mini Play, so you may have to adjust the mappings so that your MIDI controller works as expected. 

To play back your samples, locate `horiz/slider/02` on your MIDI pad and press it. Now you're in `play` mode. When you press any of your previously-loaded pads your sample should play (make sure you adjust the live.gains accordingly -- left is meant for monitoring during recording mode, so you'll want to mute this one).

A last convenience is the sfrecord~ block at the bottom. Hit `open` right above it to name a file that will be your 'final' ('aggregate,' maybe ?) sample. Hit the `1` and play your heart out on the pads. Then, hit `0` and go find the sample you just created in your files. Isn't it marvelous?

### TODO: 
1. UI
2. Get a better MIDI controller.
3. Map record `final` sample button to MIDI
4. Recursively store loops to pads
5. Effects
