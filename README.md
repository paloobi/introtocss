# Intro to CSS - Lecture Slides

How to open and run the slides locally:

1. Run `npm install` to install all modules
2. Run `npm run build` to run marp build on all files
3. Output file will be in `./slides` (Input files are in `./source`)
4. Open the `./slides/introtocss.html` in your browser
5. Press `p` to use Presenter View, which includes a timer and the slide notes.

To export notes as a separate text file, run:

1. Run `npm run build-notes`
2. Notes will be added to `./notes`

## How These Slides Were Made

* This slide deck was written in markdown using the marp framework
* Slides are built using marp-cli: https://github.com/marp-team/marp-cli
* The diagrams were made in [Excalidraw](https://excalidraw.com/). You can load the diagram files into Excalidraw if you want to make changes to them. I've included some of the diagrams in `./diagrams`.