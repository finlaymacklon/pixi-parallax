# pixi-parallax
Use this script to add a parallax background (animated/translating layers) to your PixiJS game

## Usage

### Example

[Caber Catch game source code](https://github.com/asgaardlab/canvas-visual-bugs-testbed/tree/main/game)

```js
// import the function from the script
import { addParallaxBackground } from './parallax.js'

// create the PixiJS app 
app = new PIXI.Application(
  {
      width: 1280 / window.devicePixelRatio, // feel free to change this
      height: 720 / window.devicePixelRatio, // feel free to change this
      autoResize: false,                     // maybe necessary (need to check)
      resolution: window.devicePixelRatio,   // feel free to change this
  }
);

// define the folder name for parallax background assets
const background_folder = 'assets/forest/';
// define the file name for each layer
const background_files = [
    '_00_sea.png',
    '_01_ground.png',
    '_02a_bunny.png',
    '_02_trees and bushes.png',
    '_03a_bunny.png',
    '_03_distant_trees.png',
    '_04_bushes.png',
    '_05_hill1.png',
    '_06_hill2.png',
    '_07_huge_clouds.png',
    '_08_clouds.png',
    '_09_distant_clouds1.png',
    '_10_distant_clouds.png',
    '_11_background.png'
].reverse();
// define the change in x-direction (dx) for each layer 
const dxs = [
  0,
    0,
    13,
    0,
    -9,
    0,
    0,
    0,
    0,
    1,
    4,
    3,
    2,
    0
].reverse();
// define the change in y-direction (dy) for each layer 
const dys = [0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0];
// add the background
addParallaxBackground(app, background_folder, background_files, dxs, dys);
```

## Contributing

Suggestions and contributions welcome!
