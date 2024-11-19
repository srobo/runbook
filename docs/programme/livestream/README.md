# Livestream

Some events are livestreamed, such as kickstart events to archive the presentation and get a wider audience, or competitions so family and friends can follow along too.

## Platforms

Events are streamed to the Student Robotics [YouTube](https://www.youtube.com/user/studentrobotics) channel.

## Software

We use [OBS Studio](https://obsproject.com/) as the livestreaming software used to transmit the video feeds to YouTube. OBS deals with mixing, scene transmission and screen capture.

OBS configuration is split into 2 fundamental objects: Scenes and Sources. A scene is the thing shown on screen, which is made up of multiple sources.

For virtual competition livestreams we use [SRComp Mixtape](https://github.com/srobo/srcomp-mixtape) to automate the playback of match videos and the scene transitions at either end of each match. See [Mixtape's documentation](https://github.com/srobo/srcomp-mixtape#configuration) for how to create a suitable playlist file to configure mixtape.

Additional software may be needed if the hosts are [remote](./remote-content.md).

## Hardware

The hardware requirements for hosting a livestream are not large, however a stable internet connection is a must. A dedicated GPU is useful to ensure the system isn't taxed too heavily.
