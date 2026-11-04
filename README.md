# You Are An Idiot

A single-file recreation of the "You are an idiot!" prank program: a fake Windows XP
desktop runs `youareanidiot.exe`, the classic two-frame Flash loop (serif "you are an idiot",
three hopping smileys, black/white strobe) bounces around the screen, and every attempt to
close the window spawns more of them. The choir and the laugh are synthesized with the
Web Audio API, so there are no external assets. The synthesis was tuned against onset and
spectral analysis of the original 5.0 s clip: six sung syllables on a B major chord, then
sixteen shrill laughs around B4, with the screen inverting every 333 ms (4 frames at 12 fps)
as in the original Flash file. `window.renderIdiotLoop(seconds)` renders one loop offline
for checking.

Open `index.html` in a browser. It starts with the XP "Open File - Security Warning" dialog,
which also carries the photosensitivity and sound warning and a reduced-flashing option.

## How it plays out

The run follows the meme videos, driven by how many windows are open:

1. **Normal.** One window bounces and "you are an idiot, ha ha ha ha" repeats on a 5 s loop.
2. **Bugging (6+ windows).** Closing a window spawns smaller ones. The desktop stops
   repainting, so windows leave staircase trails. Motion turns choppy, and a second copy
   of the phrase starts overlapping.
3. **Not responding (16+ windows).** Title bars read "(Not Responding)", the cursor turns
   busy, the clock stops, and clicks answer late. More copies of the phrase pile up, and the
   sound skips and stutters.
4. **Crash (40 windows).** Everything freezes, the sound sticks into a looping buzz, the
   screen cuts to black, then shows "It's now safe to turn off your computer."

Every effect is simulated inside the page. It opens no real windows and puts no real load
on the device: the lag is throttled redraws and deliberate pauses.

Press Esc, or use Start > Turn Off Computer, to stop it at any point.
