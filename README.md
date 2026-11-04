# You Are An Idiot

A single-file recreation of the "You are an idiot!" meme as seen in its best-known video
demo: a Windows 98 desktop runs `idiot.exe`, Internet Explorer opens the classic two-frame
Flash loop (serif "you are an idiot", three hopping smileys, black/white strobe), then small
IE popups bounce around the screen, each flashing on its own clock, and every attempt to
close one brings up a "You are an idiot!" message box and spawns more. Every window plays its own copy of the jingle, "You are an idiot! Ha ha ha ha ha ha ha ha!",
starting when it opens, so the copies pile up as the windows multiply. The jingle is an
original recording made for this page: an offline text-to-speech voice (Piper), pitched up
into a three-voice chord and placed on the original 5-second timing. An offline speech
recognizer transcribes it as "you are an idiot | ha ha ha ha ha ha ha ha". It is embedded as a
small MP3, so the page has no external assets.

Open `index.html` in a browser. On a computer the desktop runs inside a widescreen PC
monitor at a fixed resolution (1280x800, 1024x640 or 768x480, whichever fits). On touch
screens and small windows the Windows 98 screen fills the whole viewport instead, and in
portrait it is turned sideways so it still runs landscape. The first tap or click asks for
full screen and a landscape lock where the browser allows it (iPhone Safari does not). The bezel's power button turns the monitor off
and on, and its LED blinks amber while the system is hung.

Every step is driven by you:

1. Double-click `idiot.exe` on the desktop (a single tap on touch screens).
2. A "File Download" dialog asks to run or save it. It also carries the flashing and sound
   warning and a reduced-flashing option.
3. Setup walks through Welcome, a license you must accept, an install progress bar, and
   Finish, which launches the program. Afterwards the icon runs it directly.
4. Close windows with their title-bar buttons, the Delete key, the message boxes' OK and
   Cancel, or bring them forward from the taskbar. None of it goes well.
5. Try Start > Shut Down, press any key on the blue screen, then Restart.

## How it plays out

The run follows the meme videos, driven by how many windows are open:

1. **Normal.** Internet Explorer plays the page, then four popups appear. A window bounces and "you are an idiot, ha ha ha ha" repeats on a 5 s loop.
2. **Bugging (8+ windows).** The desktop stops repainting, so windows leave staircase
   trails, motion turns choppy, and more windows open on their own.
3. **Hung (20+ windows).** Trails take over the whole screen. The cursor turns to an hourglass, the clock stops, and clicks answer late. A second and third copy of the phrase
   start overlapping, and the sound skips and stutters.
   Closing a window now brings up Internet Explorer's "This browser window ... is busy"
   box, which also appears on its own at 40 windows. Start > Shut Down dims the screen
   and then gives up, as in the video.
4. **Crash (56 windows).** Everything freezes and the sound sticks into a looping buzz that
   carries on behind a Windows 98 blue screen. Any key ends it, then the screen shows
   "It's now safe to turn off your computer."

Every effect is simulated inside the page. It opens no real windows and puts no real load
on the device: the lag is throttled redraws and deliberate pauses.

Press Esc, or the monitor's power button, to stop it at any point. Start > Shut Down works
only until the system hangs.
