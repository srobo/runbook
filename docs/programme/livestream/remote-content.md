# Remote content

All of the content for a livestream may not be coming from the same machine, for example if the hosts are remote.

!!! warning
    For anything which requires high quality, such as full-screen video, this should be handled by the livestream machine wherever possible.

## Video

To stream video, it's recommended to use [vdo.ninja](https://vdo.ninja), as this creates high-quality low-latency video sources which can be easily dropped into streaming software as a browser source.

`vdo.ninja` also allows hosts to mute themselves, and add background effects such as blurs and green-screening.

For on-site cameras, it may also be useful to use NDI with [`obs-ndi`](https://github.com/obs-ndi/obs-ndi)

## Slides

For presenting slides, it's recommended to run the slides on the livestream machine, so any animated content or videos are as smooth as possible.

If a remote host(s) needs to control the slides, it's recommended to use [Remote for Slides](https://limhenry.xyz/slides/), which also supports showing presenter notes.

To ensure the host can see the slides, use a Google Meet call to share the presentation.
