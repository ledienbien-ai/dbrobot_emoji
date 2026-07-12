# DB_robot GIF emoji component (gifs folder only)
#
# This component provides only the gifs folder with 6 GIF files.
# Use LVGL to load them from filesystem or embed in your project.

# Minimal source for component registration
set(COMPONENT_SRCS "src/dbrobot_emoji_gif.c")

# Register component
idf_component_register(
    SRCS ${COMPONENT_SRCS}
    INCLUDE_DIRS "include"
    REQUIRES "lvgl"

    EMBED_FILES 
        "gifs/staticstate.gif"
        "gifs/sad.gif"
        "gifs/happy.gif"
        "gifs/scare.gif"
        "gifs/buxue.gif"
        "gifs/anger.gif"
        "gifs/neutral.gif"
        "gifs/relaxed.gif"
        "gifs/sleepy.gif"
        "gifs/idle.gif"
        "gifs/laughing.gif"
        "gifs/funny.gif"
        "gifs/loving.gif"
        "gifs/confident.gif"
        "gifs/winking.gif"
        "gifs/cool.gif"
        "gifs/delicious.gif"
        "gifs/kissy.gif"
        "gifs/silly.gif"
        "gifs/relaxed.gif"
        "gifs/crying.gif"
        "gifs/angry.gif"
        "gifs/surprised.gif"
        "gifs/shocked.gif"
        "gifs/thinking.gif"
        "gifs/confused.gif"
        "gifs/embarrassed.gif"
)

target_compile_definitions(${COMPONENT_LIB}
    PRIVATE DBROBOT_EMOJI_GIF_VERSION="1.1.1"
)

message(STATUS "DB_robot Emoji GIF Component: gifs only at ${CMAKE_CURRENT_SOURCE_DIR}/gifs")
