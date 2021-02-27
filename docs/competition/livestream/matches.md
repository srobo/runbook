# Matches

One of the most common things broadcast during livestreams is matches. These may come either from some live camera feeds of the arena(s), or pre-recorded video from the simulator.

## Overlay

Whilst matches are playing, we show an [overlay](https://github.com/srobo/livestream-overlay) on top of the videos to present some additional information:

- The match number of the current match
- The teams competing in the current match (TLA and team name)

And outside of matches, it also shows:

- Current league schedule
- Times until the next match
- Upcoming match information

The overlay live updates with changes as they happen. It may occasionally get out of sync, in which case just needs a simple refresh.

The overlay is brought into OBS as a webpage. To ensure content behind it can be shown a [chroma key filter](https://obsproject.com/wiki/Filters-Guide#color-key-and-chroma-key), and the appropriate similarity and smoothness values found until the background is transparent, but the rest of the colours are still showing correctly.

The overlay should be present on all scenes which display matches, and perhaps a few others depending on context.

## Video Scheduler

In a simulator-based competition, matches are pre-recorded. To assist with the automatic queueing and playback of matches in line with the competition schedule, we have a [video scheduler](https://github.com/RealOrangeOne/livestream-video-scheduler).

The video scheduler is currently a fork of the [overlay](#overlay), with much of the functionality removed. Therefore, it's brought into OBS in the same way, just without the chroma key.

### Playback issues

Due to issues with the OBS browser, some videos will not play directly through it. This manifests as it requesting the video file, but not being able to play it. There are a few solutions to this:

- Transcode the videos to `webm`, as this can be played correctly
- Open the scheduler in an external browser, and add to OBS via a screen share.

This issue has mostly been seen on Linux, and a long-term solution is being looked for.
