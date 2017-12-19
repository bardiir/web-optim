# web-optim
Fully featured web optimizer for (mostly) static pages

## WIP
This is a Work-in-progress but based on the learnings from the auto-caesium, auto-dash-hls etc projects done by [@majamee](https://github.com/majamee) and me over the last weeks the following features/optimizations are planned:

Milestone 1:
- Optimize JPG Images to a Quality of 80 and strip unnecessary data (like [bardiir/auto-caesium](https://github.com/bardiir/auto-caesium) does)
- Optimize PNG Images (like [bardiir/auto-caesium](https://github.com/bardiir/auto-caesium) does)
- Optimize Video Files into Multi-Bitrate Videofiles using HLS and DASH (like [majamee/auto-dash-hls](https://github.com/majamee/auto-dash-hls) does)
- Optimize Hero Video Files (hero_*) into Audio-Free Video Files (like [majamee/hero-videoptim](https://github.com/majamee/hero-videoptim) does)

Milestone 2:
- Introduce options/parameters to disable every optimization if not needed/useful
- Crush JS & CSS Files
- Compress static files (js, css, fonts,...) into .gz files alongside their uncompressed counterparts & create documentation to leverage this on a webserver level to lower overall performance usage by not compressing statics inline

Milestone 3:
- Optimize GIF Images
- Optimize/Crush SVG Images
- Optimize Fonts (remove symbols not used in the html codebase ideally)

Milestone 4:
- Automatically replace video files referenced in html files with the multi bitrate ones using PLYR
