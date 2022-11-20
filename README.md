# Synesthesia Colorization of Moby-Dick for NaNoGenMo 2022

This is an old idea of mine, I wanted to try it for several years, maybe this time I'll do it.

~5 years ago, I made an [pet-project for a color2color_name generation](https://medium.com/altsoph/yet-another-neural-network-generated-color-names-f0aad5d45081).

As a side artifact I had a 10K+ colors with names dataset, so I used it for the reversed task: taken a fasttext vector for the word as an input, predict the RGB (or HSL, to be precise) components of it's color.
Suddenly, it worked pretty well, so the majority of the color-words were colored right. But also, it colorised other words in some interesting ways. 

I tried to train another classifier head to guess, if the word have a color information at all. Still, it thinks some non-color words have some significant colorization, for example:
* words like `ocean`, `sky`, `pool`, `sea`, `water` tend to have blue or cyan color;
* `night`, `dark`, `sleep` are dark gray or dark blue;
* `burnt`, `wine`, `flame`, `fire` are red.

It colors the random words in some strange ways as well :) 
For example, frost and frozen have red bias somewhy.

Now, I decided to use this classifier to colorize words of Moby-Dick.
