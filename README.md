mpv osc script forked from [modern](https://github.com/maoiscat/mpv-osc-modern)

![mpv-shot0007](https://user-images.githubusercontent.com/84557113/205270820-86e17e7f-a679-4b05-b874-d1bf50754d75.jpg)


# Installation

modern.lua --> "\~\~/scripts/" (!!REMOVE OTHER OSC SCRIPTS!!)

material-design-iconic-font.ttf --> "\~\~/fonts" ([FONT LINK](https://zavoloklom.github.io/material-design-iconic-font/))

Then edit "\~\~/mpv.conf", add the following lines to the end

```
osc=no

[Idle]
profile-cond=p["idle-active"]
profile-restore=copy-equal
title=' '
keepaspect=no
background=1
```
# Configuration

Config file locates at "\~\~/script-opts/osc.conf". Supported options are listed below.

```
    showwindowed=yes/no             -- show OSC when windowed?
    showfullscreen=yes/no           -- show OSC when fullscreen?
    scalewindowed=1                 -- scaling of the controller when windowed
    scalefullscreen=1               -- scaling of the controller when fullscreen
    scaleforcedwindow=2             -- scaling when rendered on a forced window
    vidscale=yes/no                 -- scale the controller with the video?
    hidetimeout=1000                -- duration in ms until the OSC hides if no mouse movement. enforced non-negative for the user but internally negative is 'always-on'.
    fadeduration=500                -- duration of fade out in ms 0=no fade
    minmousemove=3                  -- minimum amount of pixels the mouse has to move between ticks to make the OSC show up
    iamaprogrammer=yes/no           -- use native mpv values and disable OSC internal track list management (and some functions that depend on it)
    font='mpv-osd-symbols'          -- default osc font
    seekrange=yes/no                -- show seekrange overlay
    seekrangealpha=128              -- transparency of seekranges
    seekbarkeyframes=yes/no         -- use keyframes when dragging the seekbar
    title='${media-title}'          -- string compatible with property-expansion to be shown as OSC title
    showtitle=yes/no                -- show title and no hide timeout on pause
    timetotal=yes/no                -- display total time instead of remaining time?
    visibility=auto/yes/no          -- only used at init to set visibility_mode(...)
    windowcontrols=auto/yes/no      -- whether to show window controls
    volumecontrol=yes/no            -- whether to show mute button and volumne slider
    processvolume=yes/no            -- volume bar show processd volume
    language=eng/chs                -- eng=English chs=Chinese
    boxalpha=80                     -- alpha of the background box,0 (opaque) to 255 (fully transparent)
```

# Button Actions

Some buttons may accept multiple mouse actions, here is a list:

(NOTE: mbtn = mouse button)

## seekbar
* mbtn_left: seek to chosen position.
* mbtn_right: seek to the head of chosen chapter
## skip_back/forward
* mbtn_left: add chapter -1/1.
* mbtn_right: skip 90 seconds.
* shift+mbtn_left: frame-step/frame-back-step
## playlist_back/forwad
* mbtn_left: play previous/netx file.
* mbtn_right: show playlist.
## cycle_audio/subtitle
* mbtn_left: cycle to next track.
* mbtn_right: show track list.
