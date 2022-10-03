| [Homepage](https://aidanasingh.github.io) | [Projects](https://aidanasingh.github.io/#projects) | [Music](https://aidanasingh.github.io/#music) | [Contact](https://aidanasingh.github.io/#contact) | 

# Ambisonics Encoder
## Motivation

Ambisonics is an audio format that provides a solution to storing the directionality of audio irrespective of the equipment used for recording or playback. For this reason, it shows promise in the field of machine listening, where computers are being trained to localize and label objects in space from sound only with deep learning. Ambisonics leverages a standardized format that can be encoded from any microphone array recording, though the encoders are often proprietary and have different functionality, making data standardization difficult when audio is presented in the raw recorded form.

To take microphone array datasets and convert them to ambisonics B-format, I pursued coding an open-source encoder that considers features of the microphone array rather than being array-specific. Since this encoding problem was previously solved for in the context of audio plug-ins by Leo McCormack with Array2SH, my contribution is translating his code to python for dataset aggregation.

My code success

I explored this topic through my NSF REU position (National Science Foundation Research Experience for Undergrads) at NYU Music and Audio Research Laboratory under Dr. Iran R Roman.