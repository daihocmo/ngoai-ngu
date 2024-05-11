# [Immersion with YouTube](https://tatsumoto-ren.github.io/blog/immersion-with-youtube.html)

March 20, 2022 — Tatsumoto

YouTube is a popular website where people can upload and watch videos. Through watching YouTube you can immerse with native Japanese content. Such content can be of particular interest to people who want to understand colloquial Japanese, speech with a lot of mumbling, slurs and slang. There are many language-dense streams and podcasts on YouTube that can be used for background listening. You can also find news channels with more formal speech.

---

## [](https://tatsumoto-ren.github.io/blog/immersion-with-youtube.html#how-to-access "Permanent link")

## How to access

Like many popular big tech websites today, YouTube uses proprietary JavaScript code, which is not safe to run. If you go to the website, it won't work if you block proprietary JavaScript code from running. In addition to that, YouTube contains privacy violating trackers and collects data about users. To access the videos, use various alternative ways that minimize tracking.

There are several ways you can watch YouTube.

1. [Invidious](https://github.com/iv-org/invidious). Invidious is an alternative front-end to YouTube. It lets you choose from a number of instances based on their health. A list of Invidious instances can be found on [https://api.invidious.io/](https://api.invidious.io/). Invidious gives you direct download links for every video.
2. [yt-dlp](https://wiki.archlinux.org/index.php/yt-dlp). yt-dlp is a program to download videos. To search for videos and obtain their links, you still need to use a front end such as Invidious or [youtube-viewer](https://github.com/trizen/youtube-viewer).
3. [mpv](https://wiki.archlinux.org/title/Mpv). `mpv` is a video player. It can utilize a built-in `yt-dlp` hook to play YouTube videos. I recommend downloading videos before watching them, however. Storing immersion material locally makes [sentence mining](https://tatsumoto-ren.github.io/blog/sentence-mining.html) substantially easier.
4. Not using YouTube at all. Explore privacy-respecting platforms like [PeerTube](https://joinpeertube.org/) ([https://video.076.moe](https://video.076.moe)) and [Odysee](https://odysee.com/). Chances are, you'll find Japanese immersion content there too. `yt-dlp` works on these websites as well.

## [](https://tatsumoto-ren.github.io/blog/immersion-with-youtube.html#subtitles "Permanent link")

## Subtitles

Subtitles play an important role for language learners. On YouTube, you can find a wide variety of videos in Japanese with built-in Japanese subtitles. Not every video has human-made subtitles, and auto-generated subtitles aren't accurate. Avoid using them if possible.

To find content with subtitles, open Invidious, click on `[+] Filters` and under "Features" enable "Subtitles/CC".

After downloading a video and subtitles for it, you can put it into `subs2srs` or watch it in `mpv` with `mpvacious` and make flashcards.

The following sites offer video search based on target language subtitles:

- [YouGlish](https://youglish.com/japanese)
- [CaptionPop](https://www.captionpop.com/)

We recommend utilizing their search features but using `mpv` to watch the videos.