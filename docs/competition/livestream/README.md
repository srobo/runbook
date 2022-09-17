# Livestream

Some events are livestreamed, such as kickstart events to archive the presentation and get a wider audience, or competitions so family and friends can follow along too.

## Platforms

Events are streamed to the Student Robotics [YouTube](https://www.youtube.com/user/studentrobotics) channel.

## Software

We use [OBS Studio](https://obsproject.com/) as the livestreaming software used to transmit the video feeds to YouTube. OBS deals with mixing, scene transmission and screen capture.

OBS configuration is split into 2 fundamental objects: Scenes and Sources. A scene is the thing shown on screen, which is made up of multiple sources.

For virtual competition livestreams we use [SRComp Mixtape](https://github.com/srobo/srcomp-mixtape) to automate the playback of match videos and the scene transitions at either end of each match. See [Mixtape's documentation](https://github.com/srobo/srcomp-mixtape#configuration) for how to create a suitable playlist file to configure mixtape.

## Hardware

The hardware requirements for hosting a livestream are not large, however a stable internet connection is a must. A dedicated GPU is useful to ensure the system isn't taxed too heavily.

## Music

As background music during livestreams, we'll often play quiet music.

For finals events, more dramatic music is played vs other sessions, to emphasize the importance. For finals events, we have heavily used [Monstercat](https://www.monstercat.com/) in the past, and for other events [incompetech](https://incompetech.com/), as these sources can be used without purchasing a licence, provided the required attribution is given.

There is no simple playlist used for each event. The playlists for each event are built off the previous, with any new finds added and disliked tracks removed.

During live events, the music played throughout the venue needs to be stripped out, usually through a separate audio feed.

Audio can either be played directly through OBS using the VLC source, or through a desktop audio player, so long as any other system sound effects are muted. When playing audio, be sure to [normalize it](https://www.alphr.com/normalize-volume-vlc) to ensure the volume doesn't vary.
