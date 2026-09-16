
Boards support for Olimex [ESP32-P4-PC](https://www.olimex.com/Products/IoT/ESP32-P4/ESP32-P4-PC/open-source-hardware).

See my [blog entry](https://freehackers.org/thomas/2026/09/16/board-support-packages-for-olimex-esp32-p4-pc-on-esp-idf-6-2/) for details.

There are two variants, with or without LVGL support, as done upstream

Changelog
---------
* basic renaming/cleaning + photo
* ported to esp-idf 6.2
* remove stuff not found on olimex card:
    * touchscreen (gt911)
    * lcd brightness control
    * other outputs than HDMI (ili9881c, ek79007)

How to
------
If you want to use it, instead of cloning/copying, I recommend using
the official components manager from ESP-IDF. Add this in your `idf_component.yml`:

```
dependencies:
  olimex_esp32_p4_pc_noglib:
    git: https://github.com/orzel/olimex-bsp.git
    path: olimex_esp32_p4_pc_noglib
```

(or `olimex_esp32_p4_pc` of course)

