# projectionMapper

A projection mapping starter template in p5.js, by PhilaCon Valley. You build a p5.js sketch on
your laptop. Then you map it onto a real object with a projector.

Built for PATCH 003: Projection Mapping Lab, at Pennovation Works on Wednesday, September 30, 2026.

![The template on a laptop: art stretched across four pink corner handles](docs/preview.jpg)

**Status:** used live at PATCH 003 on 09/30/2026. Waskar and Jay keep improving it.

**Try it first, with nothing to install:** [philaconvalley.github.io/projectionMapper](https://philaconvalley.github.io/projectionMapper/).
Drag the pink corners to see how it works. To change the art, get your own copy below.

## Run it on your machine

No build step. p5.js is in `lib/`, so it works with no Wi-Fi.

**No git? Download it.** On this page, click the green **Code** button, then **Download ZIP**.
Unzip the folder and open `index.html` in Chrome. That folder is yours to keep.

**With git:**

```bash
git clone https://github.com/philaconvalley/projectionMapper.git
cd projectionMapper
open index.html
```

**Want your own copy on GitHub?** Click the green **Use this template** button at the top of this
page, then **Create a new repository**. You get a clean copy under your own account that you can
change and share. A template copy cannot send changes back here. To fix or add something in this
repo, fork it instead and follow [CONTRIBUTING.md](CONTRIBUTING.md).

| Key or mouse | Action |
|---|---|
| Drag a pink corner | Move that corner onto the corner of your surface |
| Drag inside the shape | Move the whole shape without changing it |
| E | Hide or show the corners. Hide them before you project |
| F | Full screen |
| B | Blackout: the projector goes dark at once. Press B again to bring the art back |

## Edit it with the text editor you already have

You do not need a code editor. Notepad (Windows) and TextEdit (Mac) work.

**First, unzip the folder.** The page cannot load files from inside a ZIP.

- **Windows:** right-click the ZIP, then **Extract All**.
- **Mac:** double-click the ZIP.

**Windows, with Notepad:**

1. In the unzipped folder, right-click `art.js`. Choose **Open with**, then **Notepad**.
2. Change the art. Save with **Ctrl+S**.
3. Open `index.html` in Chrome. After each save, press **Ctrl+R** to reload.

**Mac, with TextEdit:**

1. Open TextEdit. In the menu bar, click **Edit**, then **Substitutions**. Turn off **Smart
   Quotes**. TextEdit otherwise changes `"` into curly quotes, and the code stops working.
2. In the unzipped folder, right-click `art.js`. Choose **Open With**, then **TextEdit**.
3. Change the art. Save with **Cmd+S**.
4. Open `index.html` in Chrome. After each save, press **Cmd+R** to reload.

**Nothing shows up?** In Chrome, press **Cmd+Option+J** (Mac) or **Ctrl+Shift+J** (Windows). The
red text names the line in `art.js` with the mistake.

A version in the [p5.js Web Editor](https://editor.p5js.org), with nothing to download, is planned
but not ready yet.

## Put it on a projector

1. **Connect the projector** to your laptop. Most laptops need a USB-C to HDMI adapter.
2. **Extend your display, do not mirror it.** On a Mac: System Settings, then Displays. If the two
   screens show the same thing, turn mirroring off.
3. **Open `index.html` in Chrome.**
4. **Drag the Chrome window onto the projector's screen.** It sits off one edge of your laptop
   screen.
5. **Click the page, then press F** for full screen.
6. **Drag the four pink corners onto the corners of your object.** Watch the wall, not your laptop.
7. **Press E** to hide the corners. Your art now sits only on the object.

Set the corners after you go full screen. If you leave full screen, set them again.

**Tip:** the room has to be dark. Anything that is not black on your screen shows up as light on
the wall.

## Make your own art

Open `art.js`. It is the only file you need to change. `drawArt(g)` draws one frame of your art.
Draw into `g` the way you draw into a normal p5.js canvas: `g.circle(...)`, not `circle(...)`.

Want a head start? The `examples/` folder has seven art files:

| File | What it does |
|---|---|
| `examples/stripes.js` | Stripes slide across the surface. Good for showing edges |
| `examples/noise.js` | A slow, living color field |
| `examples/text.js` | A word that pulses. Change it to your own word |
| `examples/particles.js` | Drifting dots with trails. Shows how to use `setupArt()` |
| `examples/matrix.js` | Green letters raining down, like The Matrix |
| `examples/skyline.js` | A quiet city skyline at night. Good as a background |
| `examples/subway.js` | An 8-bit New York subway pillar. Map it onto a real column or box |

To use one, copy the whole example file, and paste it over all of `art.js`. Some examples need
more than `drawArt()`, so copy every line. Or open `index.html` and change `art.js` to the
example's path.

`setupArt(g)` is optional. It runs once at the start. Use it for anything you create only one time.

## What the template does

1. **Corners.** Drag the four pink corners onto the corners of your object.
2. **Warp.** Your art stretches to fit those four corners, in perspective. On a tilted surface, the
   far side gets less room, the way the projector sees it.
3. **Move.** Drag inside the shape to move it without changing it.
4. **Preview.** You see the result on your laptop before you get projector time.

**A corner stops moving?** The four corners must make a proper four-sided shape. If a drag would
cross two edges into a bow-tie, or push one corner in to make a dent, the corner stays at its last
good place. Drag it back the other way.

**Coming next:** more than one surface, so you can map each panel of a board or each face of a
box. After that, saving your corner positions so a reload does not reset them.

**Known limit:** when the window changes size, the corners scale with it, so the shape keeps its
place on the screen. The window edges also move when you enter or leave full screen, so on a
projector the shape can shift by a few pixels. Set the corners after you go full screen.

## Files

- `index.html`: the page. It loads the styles and the scripts, and holds no code of its own.
- `style.css`: the page styles. A black, full-window canvas with no scroll bars.
- `art.js`: your art. Start here.
- `examples/`: seven art files to copy from.
- `sketch.js`: the mapping engine. You do not need to change it. It warps your art in perspective,
  with math called a homography. `GRID` splits the surface into small cells so the image does not
  bend along the diagonal.
- `lib/p5.min.js`: p5.js 1.11.13, saved in the repo for offline use.

## Contribute

Made art you want to share, or found a bug? See [CONTRIBUTING.md](CONTRIBUTING.md).

## License

The code uses the MIT license. See `LICENSE`. p5.js uses the LGPL 2.1 license.

## PhilaCon Valley

A Philadelphia tech community, by us, for us. Come build with us:
[Discord](https://philaconvalley.com/discord).
