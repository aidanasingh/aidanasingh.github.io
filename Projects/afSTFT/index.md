
| [Homepage](https://aidanasingh.github.io) | [**Projects**](https://aidanasingh.github.io/Projects/) | [Music](https://aidanasingh.github.io/published_music/) | [Experience](https://aidanasingh.github.io/experience/) | 

# afSTFT Implementation

## Motivation

I am implementing the alias free STFT, or "afSTFT", by Juha Vilkamo in python for my senior capstone at NYU. This transform is used by an open-source Ambisonics encoder I have translated from c to python, see my ambisonics encoder project for broader motivations about this encoder.

The afSTFT is a time-frequency transform designed to avoid the circular effects of multiplying signals in the frequency domain (convolution). The aliasing referred to in the transform's name is temporal aliasing (opposed to frequency or spatial aliasing).

Higher-Order Ambisonics (HOA) encoding leverages filtering in the frequency domain. In its simplest form, encoded ambisonics signals are a linear combinations of microphone capsule signals. Intuitively, the need for filtering can be understood by how an ambisonic mic's body is a directionally dependent filter, where shorter wavelengths have more difficulty phasing around a rigid body. Intuition can also come from the fact that the individual microphone capsules' directivity is frequency dependent. Therefore filtering is necessary for the most accurate HOA encoders.

# Task

I am currently working on this project, stay tuned for updates!