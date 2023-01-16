| [Homepage](https://aidanasingh.github.io) | [**Projects**](https://aidanasingh.github.io/Projects/) | [Music](https://aidanasingh.github.io/published_music/) | [Experience](https://aidanasingh.github.io/experience/) | 

# Ambisonics Encoder

## Motivation

Ambisonics is a multichannel audio format that stores the directionality of audio irrespective of the equipment used for recording or playback. For this reason, it is used in the field of machine listening, where computers are being trained to localize and label objects in space from sound with deep learning. Ambisonics provides a standardized format that can be encoded from any microphone array recording, though encoders are often proprietary and made for one array, making data standardization difficult when audio is presented in the raw recorded form.

## Task

To take microphone array datasets and convert them to ambisonic spherical harmonic channels, I programmed an encoder that takes features of the microphone array as arguments rather than being array-specific. Since this encoding problem was previously solved for in the context of audio plug-ins by Leo McCormack with Array2SH, my contribution is translating his code to python for dataset aggregation.

## Outcomes

[My code](https://github.com/aidanasingh/micarraylib/blob/4a359b3a49d625c9d5bf6e6ccb9183ad73388d3c/micarraylib/utils.py#L33-L277) produces the encoding matrix for an Eigenmike 32, but further work is needed to compute the time-frequency representation of the input signal, which in Array2SH is a combination of Discrete Fourier Transforms and Discrete Cosine Transforms with zero padding and windowing. Once the time-frequency representation is programmed, I plan on expanding the functionality to other microphones/mic arrays.

I am pursuing implementing this time-frequency transform ("afSTFT" by Juha Vilkamo) for my senior capstone project under Dr. Brian McFee.

## Poster

<img src="assets/Singh_Ambisonics_Encoder_Poster.jpg" width="850"/>

I explored this topic through my NSF REU position (National Science Foundation Research Experiences for Undergrads) at the NYU Music and Audio Research Laboratory under Dr. Iran Roman.