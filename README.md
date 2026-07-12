# DB-Robot GIF Emoji Component

ESP-IDF component that provides **only the gifs folder** with 6 DB-Robot GIF emojis for LVGL.

## Content

- **gifs/** – 26 GIF files: `staticstate`, `sad`, `happy`, `scare`, `buxue`, `anger`, `neutral`, `relaxed`, `sleepy`, `idle`, `laughing`,`funny`, `loving`, `confident`, `winking`, `idle`, `cool`, `delicious`, `kissy`, `silly`, `relaxed`, `crying`, `angry`, `angry`, `surprised`, `shocked`, `thinking`, `confused`, `embarrassed`

- Minimal C API: version, count, and name by index

No embedded C arrays; load GIFs from filesystem or embed them in your project.

## Requirements

- ESP-IDF
- LVGL >= 9.0

## Usage

Add to your project's `idf_component.yml`:

```yaml
dependencies:
  dbrobot-emoji: "^1.1.1"
```

In code:

```c
#include "dbrobot_emoji_gif.h"

// Version and count
printf("Version: %s, Count: %d\n", dbrobot_emoji_gif_get_version(), dbrobot_emoji_gif_get_count());

// Get GIF filename by index (0..5)
const char *name = dbrobot_emoji_gif_get_name(0);  // "staticstate"
```

Copy the **gifs/** folder to your SPIFFS/image partition or embed the GIF files in your app, then use LVGL to open them (e.g. `lv_gif_set_src()` from file path).

## Layout

```
dbrobot-emoji/
├── idf_component.yml
├── CMakeLists.txt
├── gifs/           # only content – 26 GIF files
│   ├── staticstate.gif
│   ├── sad.gif
│   ├── happy.gif
│   ├── scare.gif
│   ├── buxue.gif
│   ├── anger.gif
│   ├── relaxed.gif"
│   ├── sleepy.gif"
│   ├── idle.gif"
│   ├── laughing.gif"
│   ├── funny.gif"
│   ├── loving.gif"
│   ├── confident.gif"
│   ├── winking.gif"
│   ├── cool.gif"
│   ├── delicious.gif"
│   ├── kissy.gif"
│   ├── silly.gif"
│   ├── sleepy.gif"
│   ├── crying.gif"
│   ├── angry.gif"
│   ├── surprised.gif"
│   ├── shocked.gif"
│   ├── thinking.gif"
│   ├── confused.gif"
│   ├── embarrassed.gif"
├── include/
│   └── dbrobot_emoji_gif.h
└── src/
    └── dbrobot_emoji_gif.c
```

## License

MIT
