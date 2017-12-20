# ** Work in Progress - This currently is neither complete nor functional - Do not use (yet)! **
# web-optim

Fully featured web optimizer for (mostly) static pages

## Usage
```
docker pull bardiir/web-optim
docker run -v /path/to/your/web/folder:/in -v /path/to/the/optimized/output:/out [-v /tmp/cache:/cache] bardiir/web-optim [options]
```

`-v /path/to/your/web/folder:/in` - This is the data folder you want to optimize, replace `/path/to/your/web/folder` with the real source  
`-v /path/to/the/optimized/output:/out` - This is where the optimized data is saved to, replace `/path/to/the/optimized/output` with the real target  
`-v /tmp/cache:/cache` (optional) - Save cache data to this directory, this speeds up subsequent runs a lot if the output folder gets cleared in between, replace `/tmp/cache` with the caching location


## WIP
This is a Work-in-progress but based on the learnings from the auto-caesium, auto-dash-hls etc projects done by [@majamee](https://github.com/majamee) and me over the last weeks the following features/optimizations are planned:

Milestone 1:
- [ ] Optimize JPG Images to a Quality of 80 and strip unnecessary data (like [bardiir/auto-caesium](https://github.com/bardiir/auto-caesium) does)
- [ ] Optimize PNG Images (like [bardiir/auto-caesium](https://github.com/bardiir/auto-caesium) does)
- [ ] Optimize Hero Video Files (hero_*) into Audio-Free Video Files (like [majamee/hero-videoptim](https://github.com/majamee/hero-videoptim) does)

Milestone 2:
- [ ] Add caching and locking to prevent multiple runs of optimization if not necessary
- [ ] Save optimized files to cache for faster lookup if out is cleared (for example in build pipelines)

Milestone 3:
- [ ] Optimize Video Files into Multi-Bitrate Videofiles using HLS and DASH (like [majamee/auto-dash-hls](https://github.com/majamee/auto-dash-hls) does)

Milestone 4:
- [ ] Introduce options/parameters to disable every optimization if not needed/useful
- [ ] Crush JS & CSS Files
- [ ] Compress static files (js, css, fonts,...) into .gz files alongside their uncompressed counterparts & create documentation to leverage this on a webserver level to lower overall performance usage by not compressing statics inline

Milestone 5:
- [ ] Optimize GIF Images
- [ ] Optimize/Crush SVG Images
- [ ] Optimize Fonts (remove symbols not used in the html codebase ideally)
- [ ] Garbage collection in cache directory

Milestone 6:
- [ ] Automatically replace video files referenced in html files with the multi bitrate ones using PLYR
