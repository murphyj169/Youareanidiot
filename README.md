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

Press Esc, or use Start > Turn Off Computer, to stop it.
