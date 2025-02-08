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

In a simulator-based competition, matches are pre-recorded. To assist with the automatic queueing and playback of matches in line with the competition schedule, we use [SRComp Mixtape](https://github.com/srobo/srcomp-mixtape). Mixtape can also control the scene transitions at either end of each match. See [Mixtape's documentation](https://github.com/srobo/srcomp-mixtape#configuration) for how to create a suitable playlist file to configure mixtape.

## Commentary

[In-match commentary](../../competition/matches/commentating.md) is usually provided by separate commentators to those handling commentary between matches, to give them a break.

The in-match commentators will likely start introducing a match at 20 seconds. For the finals, this may be increased to 30 seconds or a minute.
