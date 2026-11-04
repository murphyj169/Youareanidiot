# You Are An Idiot

A single-file recreation of the "You are an idiot!" meme as seen in its best-known video
demo: a Windows 98 desktop runs `idiot.exe`, Internet Explorer opens the classic two-frame
Flash loop (serif "you are an idiot", three hopping smileys, black/white strobe), then small
IE popups bounce around the screen, each flashing on its own clock, and every attempt to
close one brings up a "You are an idiot!" message box and spawns more. The choir and the laugh are synthesized with the
Web Audio API, so there are no external assets. The synthesis was tuned against onset and
spectral analysis of the original 5.0 s clip: six sung syllables on a B major chord, then
sixteen shrill laughs around B4, with the screen inverting every 333 ms (4 frames at 12 fps)
as in the original Flash file. `window.renderIdiotLoop(seconds)` renders one loop offline
for checking.

Open `index.html` in a browser. The desktop runs inside a widescreen PC monitor at a fixed
resolution (1280x800, 1024x640 or 768x480, whichever fits) scaled to the window, so it is
made for landscape. On a phone, turn it sideways and tap Full screen on the monitor's bezel;
supported browsers also lock to landscape. The bezel's power button turns the monitor off
and on, and its LED blinks amber while the system is hung.

 It starts with the XP "Open File - Security Warning" dialog,
which also carries the photosensitivity and sound warning and a reduced-flashing option.

## How it plays out

The run follows the meme videos, driven by how many windows are open:

1. **Normal.** Internet Explorer plays the page, then four popups appear. A window bounces and "you are an idiot, ha ha ha ha" repeats on a 5 s loop.
2. **Bugging (8+ windows).** Closing a window spawns smaller ones. The desktop stops
   repainting, so windows leave staircase trails. Motion turns choppy, and a second copy
   of the phrase starts overlapping.
3. **Hung (20+ windows).** The cursor turns to an hourglass, the clock stops, and clicks answer late. More copies of the phrase pile up, and the
   sound skips and stutters.
4. **Crash (44 windows).** Everything freezes and the sound sticks into a looping buzz that
   carries on behind a Windows 98 blue screen. Any key ends it, then the screen shows
   "It's now safe to turn off your computer."

Every effect is simulated inside the page. It opens no real windows and puts no real load
on the device: the lag is throttled redraws and deliberate pauses.

Press Esc, or use Start > Turn Off Computer, to stop it at any point.
