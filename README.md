# Safari Audio Quirks

Documents the ability of Safari to output Audio based on the combination of factors.

1. Using HTML5Audio (AudioTag/Audio Object)
2. Selected Output based on
	- If headphones are pluggined
	- If Bluetooth audio speakers are setup
	- If the Phone is streaming audio over lightning cable.
3. The current state of Ring/Slient switch (iPhone) or settings (iPad)


## HTML5 Audio

### [Test](audio.html)

| Output		| Ring		| Silent 	|
|:-:			|:-:		|:-:		|
| Speakers	|  YES		|   YES	|
| Headphones	|  YES		|   YES	|
| Bluetooth	|  YES		|   YES	|
| Lightning	|   ??		|   ??		|


## WebAudio

### [Test](webaudio.html)

| Output		| Ring		| Silent 	|
|:-:			|:-:		|:-:		|
| Speakers	|  YES		| __NO__  |
| Headphones	|  YES		|   YES	|
| Bluetooth	|  YES		|   YES	|
| Lightning	|  ?? 		|   ??		|

## Combined

### In case both HTML5 Audio and WebAudio are present on a page, Safari follows the HTML5 Audio behaviour even for audio streams coming from WebAudio.

## Notes

### If a specific tab of Safari has visited a page with an Audio Tag or Audio Object, then Safari follows the HTML5 Audio behaviour even for audio streams coming from WebAudio on all following pages (even from different domains).
