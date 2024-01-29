# Audio

## Audio sources

!!! tip
    On Windows, you can use [VoiceMeeter](https://vb-audio.com/Voicemeeter/) to create "virtual" audio devices to allow OBS to distinguish between incoming application audio.

It's recommended to avoid Global Audio Devices unless the source is intended to be available to every scene (eg host microphones). Adding sources per scene is more work, but reduces the need to manually mute and un-mute certain sources when changing scenes.

## Music

As background music during livestreams, we'll often play quiet music.

For finals events, more dramatic music is played vs other sessions, to emphasize the importance. For finals events, we have heavily used [Monstercat](https://www.monstercat.com/) in the past, and for other events [incompetech](https://incompetech.com/), as these sources can be used without purchasing a licence, provided the required attribution is given. We have also used [Epidemic Sound](https://www.epidemicsound.com/), however this is a paid-for service.

There is no simple playlist used for each event. The playlists for each event are built off the previous, with any new finds added and disliked tracks removed.

During live events, the music played throughout the venue needs to be stripped out, usually through a separate audio feed.

Audio can either be played directly through OBS using the VLC source, or through a desktop audio player, so long as any other system sound effects are muted. When playing audio, be sure to [normalize it](https://www.alphr.com/normalize-volume-vlc) to ensure the volume doesn't vary.
