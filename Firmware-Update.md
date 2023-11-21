# W/: Firmware Update Procedure
 
## How it works

The update procedure is done by playing a sound-file into the IN jack of W/. You'll need to use an audio playback device (like a computer or smart phone) to send the appropriate bits. Holding 'record' at boot will startup W/ in bootloader mode awaiting its new wisdom.

*WARNING* _If updating from v1.x to v2.x, all your audio & cue points will be lost. Make sure to dub any important audio before making the transition. If updating from any v2.x firmware to another 2.x firmware will *not* affect your data, and you'll simply change the available features._

We use a modified version of Émilie Gillet's [stm-audio-bootloader](https://github.com/trentgill/stm-audio-bootloader) on W/.

### Download

First you'll need to download the [latest firmware](https://github.com/whimsicalraps/wslash/releases/latest). Make sure it's on the device you'll use for playback!

You can also grab previous firmware files if you want to travel back in time, from the [github page](https://github.com/whimsicalraps/wslash).

### Get Connected

* Turn off your synthesizer
* Connect a patch cable between the IN jack & your playback device

### Prepare your playback

* Set your sample-rate output to 48kHz (automatic on smart phones)
* Turn up the volume! 3/4 should be plenty.
* Turn off notifications / sound effects (Do not disturb / Airplane mode is best)

### Let's Go!

* While holding record, turn on your synthesizer
* The white record light should be slowly pulsing
* Start playback of the audio file, and the white lights should climb up and down the module. Input level is shown above the IN jack
* Every ~20seconds, all the lights will do an animation (as it writes the new firmware to memory!). This will happen ~6 times
* W/ will automatically restart, exactly as if you just power-cycled your synthesizer

Fun fact, there's a little generative composition that plays at the OUT jack while you're updating the fimrware!
 
## Troubles Had?

If something above doesn't seem to reflect your reality, then read on.

### Yellow record light flashing

This is the general 'failure' indicator. It usually means the audio received at IN was not what the module expected. This could be caused by a number of issues:

* Wrong sample rate: Set your playback device's sample rate to 48kHz
* Interrupted audio: Turn off notifications on your device (use airplane mode and/or turn off wifi)
* Audio too quiet: Turn your playback device up to ~75% volume
* Audio too loud: If you're sending the file in via a line->modular preamp module, turn the volume down below 50%
* Bad download: Try re-downloading the firmware wav file.

### White record continues to pulse & nothing happens

Once audio playback begins you should see the lights above the IN jack flickering to show that signal is present. If there's no indication there, it means W/ is not receiving the audio from your device:

* Bad Connection: The W/ jacks are a little stiff- make sure to double-check the cable is fully inserted into IN & your device's output, or try a different cable altogether
* Too quiet: Try turning your device's volume all the way up to see if signal starts to register
