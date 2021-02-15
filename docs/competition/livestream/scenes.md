# Scenes

This page documents a few of the core scenes which are used for livestreams. Not all of them are applicable to all events, but most are.

The various assets useful for creating these scenes can be found [here](https://drive.google.com/drive/folders/1pr1vKpnonxFoO8O5chsH5DF7Vsd0Tfih?usp=sharing).

## Technical difficulties

Things occasionally go wrong during events, so wrong it may be necessary to cut the whole feed. In this case, we show a "Technical difficulties" screen, comprised of a single image, and mute audio whilst we work on a solution.

## Countdown

We will usually "go live" prior to the scheduled start time, so viewers know we're preparing, and to build some atmosphere. Before the event starts, we put up a countdown screen, showing a live countdown to the event start time.

We have our own branded [stream countdown](https://github.com/srobo/stream-countdown) to handle this, which uses OBS' browser source to embed into the stream.

## Thanks for watching

When ending a stream, we finish with few seconds of a "Thanks for watching". This screen mostly just shows some quick bits of useful information on future events (if any). The exact content for this screen differs for each event, but is generally just a single image source.

## Back soon

Depending on the length of a livestream, we may take a break in the middle. Cutting the stream at this time would lead to a drop off in users, so instead we show a "Back soon" screen. This may be a simple image, or may be combined with the [overlay](./matches.md#overlay) to show the actual return time.

## Cameras

If the livestream is going to have a few key presenters, it's helpful to have a scene which shows their faces on stream. Depending on how the presenters are communicating, this may be implemented in a few different ways.

If they're communicating using Google Meet, or another video chat service, a screen capture of that can be cropped and embedded into OBS.

If they're in the same room, a simple video capture is enough.

In the case there's a hybrid, it depends on the nature. Often webcam devices can't be captured by OBS and used in a video call. Depending on the layout and number of people, passing the webcam to Google Meet and capturing your own feed through it may be the best option.

When showing camera feeds, it may also be helpful to show the [overlay](./matches.md#overlay) to add some additional context, reference and timing information.

## League table

For competition events, it's useful to run through the league table with it on screen. This means rather than simply listening, viewers have something read along with.

The competition website serves a [web page](https://studentrobotics.org/comp/league) which shows the current status of the league table. This table will automatically update with changes. By changing the width, height, and vertical scroll of the webpage, you can create a source which contains just the league table, and present that alongside an appropriate background image.

## Informational screens

At the start of events, it's useful to talk briefly about some background, especially around the rules of the game and structure of the stream.

In these cases, it's helpful to have some informational graphics up, showing what's likely going to be talked about. For example:

- [The rules](https://youtu.be/xBPVqsb_Ydk?t=275)
- [The simulator robot](https://youtu.be/xBPVqsb_Ydk?t=466)
