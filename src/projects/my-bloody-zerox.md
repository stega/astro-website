---
title: "My Bloody Zerox"
categories: sound-programming
summary: "Playing with Spectral flatness, aka tonality coefficient, in two audio files."
keywords: segmentation, bpm, python, rms, spectral_flatness
---

So the plan was to take two audio files, chop them up in some random way, mix up the pieces and stitch them back together again in a totally different order. Doesn’t have to be musical, they said. Well, just to make sure, I decided to chose two pieces of music that weren’t particularly musical to begin with - _Only Shallow_ by shoegaze band My Bloody Valentine, and _Zerox_ by post punk combo Adam and the Ants.

<figure>
    <iframe src="https://www.youtube.com/embed/FyYMzEplnfU" frameborder="0" width="500" height="300" allowfullscreen></iframe>
    <figcaption>My Bloody Valentine - Only Shallow</figcaption>
</figure>

<figure>
    <iframe src="https://www.youtube.com/embed/TRwyR86M_oc" frameborder="0" width="500" height="300" allowfullscreen></iframe>
    <figcaption>Adam and the Ants - Zerox</figcaption>
</figure>

Firstly, the slicing. Being predominantly white noise, Only Shallow is pretty much lacking in any transients, so using the tracks bpm and length to slice by beat made sense here.

As shoegaze bands tend to sound fuzzy and noisy, and post punk is often described as spiky and angular - a more tonal-leaning noise perhaps - I thought it could be interesting to get some spectral flatness involved in the analysis. Spectral flatness, aka tonality coefficient, measures how tone-like a sound is, verses how noise-like. Despite being pretty noisy itself, I expected the Adam and the Ants song to veer towards the more tonal side of things, if only in relation to the My Bloody Valentine track. So the sliced segments were sequenced using RMS and spectral flatness, which gave a nice smooth increasing curve when plotted.

![My Bloody Zerox](/zerox.png)

As you can see from the plot, Zerox is mostly concentrated at the loud, tonal size of the spectrum. It makes sense that Only Shallow is seen as less tonal, but its also lower in energy / loudness. I guess this is due to the compressed nature of the track, whereas the spikiness of Zerox means it cuts through so much more easily.

For those that are interested in the resultant car-crash of an audio file, it is embedded below. They did say it didn’t have to be musical.

<figure>
  <audio controls>
    <source src="https://www.uio.no/english/studies/programmes/mct-master/blog/assets/audio/2020_12_04_stephedg_my_bloody_zerox.mp3" type="audio/mpeg">
  </audio>
  <figcaption></figcaption>
</figure>
