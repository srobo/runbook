# Remote content

All of the content for a livestream may not be coming from the same machine, for example if the hosts are remote.

!!! warning
    For anything which requires high quality, such as full-screen video, this should be handled by the livestream machine wherever possible.

## Video

To stream video, it's recommended to use [vdo.ninja](https://vdo.ninja), as this creates high-quality low-latency video sources which only need a browser to function. `vdo.ninja` also allows hosts to mute themselves, and add background effects such as blurs and green-screening.

!!! note
    For on-site cameras, it may also be useful to use NDI with [`obs-ndi`](https://github.com/obs-ndi/obs-ndi)

For hosts, visit [vdo.ninja](https://vdo.ninja/), and click "Add your Camera to OBS". You'll then be able to select the correct video and audio sources, before clicking "START". At the top of the page is a URL (starting `vdo.ninja/?view=...`) which should be sent to the person running OBS.

For producers, add the link provided by the host (if the link contains `?push=...`, change it to `?view=...`) as a [Browser Source](https://obsproject.com/kb/browser-source). The source can then be positioned in the scene as needed, and the host's mic appears as an audio source.

## Slides

For presenting slides, it's recommended to run the slides on the livestream machine, so any animated content or videos are as smooth as possible.

If a remote host(s) needs to control the slides, it's recommended to use [Remote for Slides](https://limhenry.xyz/slides/), which also supports showing presenter notes.

To ensure the host can see the slides, use a Google Meet call to share the presentation.
