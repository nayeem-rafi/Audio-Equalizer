# Audio Equalizer
By [Naimur Rahman](https://github.com/nayeem-rafi)

## [Click for Open Source of Project Details & Video](https://drive.google.com/drive/folders/143pPSeegIlqwhsBaHHmNfdwPBPDkPjsw?usp=drive_link)
## [Click for Full Audio Effect Processor](https://github.com/nayeem-rafi/Audio-Effect-Processor)
## [Click for Audio De-Effect Processor](https://github.com/nayeem-rafi/Audio-De-Effect-Processor)

## Introduction
The Audio Equalizer Project is designed to provide users with a powerful and flexible tool for audio enhancement through frequency manipulation. Equalizers are indispensable in music production, sound design, and audio engineering, allowing users to fine-tune sound profiles according to their preferences or specific requirements. This project utilizes a 9-band equalizer, enabling users to adjust the balance of bass, mids, and treble frequencies, thereby enhancing their overall listening experience.

## Overview
At its core, this equalizer features both Infinite Impulse Response (IIR) and Finite Impulse Response (FIR) filters. The choice between these filter types allows for flexibility in audio processing. IIR filters are efficient and can achieve sharper frequency cut-offs with fewer coefficients, making them suitable for real-time applications. Conversely, FIR filters, while typically requiring more coefficients, offer better stability and linear phase response, ensuring that the audio waveform shape remains intact during processing.

The project comes equipped with two built-in audio presets—"Old Radio" and "Lo-Fi." These presets are designed to provide immediate enhancements to audio playback, creating nostalgic and vintage sound characteristics.

## Objectives
The primary objectives of this project are:
- To develop a functional audio equalizer that allows users to manipulate audio frequency ranges effectively.
- To provide a user-friendly interface for customizing gain settings across different frequency bands.
- To demonstrate the significant impact of EQ adjustments on audio playback and overall sound quality.
- To educate users on the principles of audio equalization and its applications in various contexts.
- To promote experimentation and creativity in sound design through user-defined presets.

## What is an Equalizer?
An equalizer (EQ) is a tool used to adjust the balance of specific frequency ranges within an audio signal. By manipulating these frequencies, users can enhance or attenuate various aspects of the sound. For instance, boosting low frequencies can add depth and warmth, while cutting high frequencies can reduce harshness or noise. Equalizers are commonly used in music production, broadcasting, and personal audio setups, allowing listeners to tailor their sound experience to their liking.
<h1 align= "center">

**Equalizer**
</h1>
<p align="center">
<img src="https://github.com/user-attachments/assets/89855dde-875b-46de-a3bd-bcee200ec225", width="720">
</p>

### Types of Equalizers
- **Graphic Equalizers:** Feature fixed frequency bands with sliders to adjust gain levels visually.
- **Parametric Equalizers:** Allow for adjustable frequency, bandwidth (Q), and gain, providing more precise control over sound.
- **Dynamic Equalizers:** Combine the functions of an EQ and a compressor, adjusting gain based on the signal level.

## How the Equalizer Works
This project implements a 9-band equalizer that operates across a range of frequency bands, each corresponding to specific sound ranges. The designated frequency bands are as follows:
1. **85 Hz** - Low bass frequencies essential for providing a solid foundation in music.
2. **280 Hz** - Low-mid frequencies contribute warmth to instruments and vocals.
3. **450 Hz** - Mid frequencies are crucial for clarity in speech and many musical elements.
4. **1 kHz** - This band marks the middle of the spectrum, influencing the presence of sounds.
5. **3 kHz** - Important for the definition of vocals and the attack of percussive instruments.
6. **6 kHz** - Enhances the brightness and airiness of the sound.
7. **10 kHz** - Frequencies here add sparkle to the audio and can enhance the clarity of cymbals.
8. **13 kHz** - Very high frequencies contribute to the overall brightness and can introduce a sense of space.
9. **16 kHz** - Ultra-high frequencies are used for special effects and can improve the perceived detail in the sound.

Users can choose between IIR and FIR filter types based on their specific needs, allowing for tailored audio processing.

## Code Functionality
The provided MATLAB code enables users to input gain values for each of the nine frequency bands, effectively adjusting the audio output according to their preferences. The implementation includes both a user interface for direct input and preset options for quick adjustments.

### Gain Adjustment
Users can specify gain values in decibels (dB) for each band. Here’s how the adjustment works:
- **Bass Frequencies:** Focus on boosting bands 1 to 3 (85 Hz to 450 Hz) to enhance the depth and warmth of music.
- **Mid Frequencies:** Adjust bands 4 and 5 (1 kHz to 3 kHz) to bring clarity to vocals and instruments.
- **Treble Frequencies:** Modify bands 6 to 9 (6 kHz to 16 kHz) to increase brightness and definition in the sound.

### Reversing Equalization
To reverse the effect of the EQ settings and return to the original audio profile, users can simply set each band’s gain to its negative counterpart. For example, if the gain for a band was adjusted to +6 dB, setting it to -6 dB will effectively negate the boost, restoring the original audio characteristics.

## Implementation Details
The equalizer utilizes a series of digital filters that process the audio signal in real-time. Here are some key points about the implementation:
- **Filter Design:** The IIR and FIR filters are designed based on standard filter design techniques to ensure that they meet the desired frequency response. Kept the filters in 'Filters.mat' file.
- **Filter Application:** The audio signal is passed through each filter corresponding to its designated frequency band, and the output is summed to create the final equalized audio signal.
- **Performance Optimization:** Care is taken to minimize latency, ensuring that audio playback remains smooth and responsive during equalization.

## Input Analysis

### Suggested Gains for Different Audio Characteristics
#### 1. Bass Enhancement
To enhance the bass frequencies, you can boost the lower bands:

- **85 Hz:** +10 dB
- **280 Hz:** +6 dB
- **450 Hz:** +4 dB
- **1 kHz:** 0 dB
- **3 kHz:** -2 dB
- **6 kHz:** -4 dB
- **10 kHz:** -6 dB
- **13 kHz:** -8 dB
- **16 kHz:** -10 dB

#### 2. Midrange Clarity
For improving midrange clarity, you would generally increase the mid frequencies:

- **85 Hz:** -4 dB
- **280 Hz:** +8 dB
- **450 Hz:** +6 dB
- **1 kHz:** +10 dB
- **3 kHz:** +6 dB
- **6 kHz:** +2 dB
- **10 kHz:** 0 dB
- **13 kHz:** -2 dB
- **16 kHz:** -4 dB

#### 3. Treble Brightness
To enhance treble frequencies, you might boost the upper bands:

- **85 Hz:** -10 dB
- **280 Hz:** -6 dB
- **450 Hz:** 0 dB
- **1 kHz:** +4 dB
- **3 kHz:** +6 dB
- **6 kHz:** +8 dB
- **10 kHz:** +10 dB
- **13 kHz:** +12 dB
- **16 kHz:** +15 dB

#### Summary
These gain settings allow users to tailor the audio output based on their specific listening preferences:

- **Bass Enhancement** focuses on boosting low-frequency bands for a richer sound.
- **Midrange Clarity** targets the mid frequencies to ensure that vocals and instruments are clear and present.
- **Treble Brightness** enhances the higher frequencies to add brightness and detail to the audio.

## Output Analysis
### Random Input Sample Gains
Here is an example of random gain inputs for the nine frequency bands:

- **Gain for 85 Hz:** -20 dB
- **Gain for 280 Hz:** -16 dB
- **Gain for 450 Hz:** -14 dB
- **Gain for 1 kHz:** -8 dB
- **Gain for 3 kHz:** -4 dB
- **Gain for 6 kHz:** 0 dB
- **Gain for 10 kHz:** 4 dB
- **Gain for 13 kHz:** 10 dB
- **Gain for 16 kHz:** 12 dB

<h1 align= "center">

**Output for Random Input**
</h1>
<p align="center">
<img src="https://github.com/user-attachments/assets/91a1369a-1d7e-4c9f-95dc-d87eb3c3aead", width="620">
</p>

<h1 align= "center">

**Output for Built in Old-Radio**
</h1>
<p align="center">
<img src="https://github.com/user-attachments/assets/92253f71-70e7-437b-8f35-211c28395949", width="620">
</p>

<h1 align= "center">

**Output for Built in Lo-Fi**
</h1>
<p align="center">
<img src="https://github.com/user-attachments/assets/f5d5424f-b84a-4e9c-ae6a-8bae4156e19c", width="620">
</p>

## Running the Code
To run the equalizer code, follow these steps:
1. Ensure you have MATLAB installed on your system.
2. Place your audio file (e.g., `music.mp3`) in the same directory as the MATLAB script.
3. Open the script in MATLAB and execute it.
4. Follow the prompts in the command window to input your desired gain values for each frequency band or select one of the preset effects.
5. After processing, listen to the output and adjust the gain settings as necessary for your preferred sound profile.


## Applications
The audio equalizer can be used in various contexts, including:
- **Music Production:** Enhance and refine audio tracks during the mixing and mastering processes.
- **Live Sound Engineering:** Adapt audio outputs for different venues and audiences, ensuring optimal sound quality in real-time.
- **Personal Use:** Tailor audio settings on personal devices for an improved listening experience across various genres and media.
- **Research and Development:** Analyze the effects of various EQ settings in academic studies or product development.

## Conclusion
The Audio Equalizer Project empowers users to manipulate audio frequencies effectively, enabling them to customize their sound experience to their liking. Through adjustable gain settings across nine distinct frequency bands, users can enhance the depth, clarity, and brightness of audio playback. This project not only serves practical audio needs but also offers educational insight into the principles of audio equalization and its importance in sound design and engineering.

## Future Enhancements
Potential future improvements to the project could include:
- **Advanced Visualizations:** Integrating visual feedback for users to see real-time changes in frequency response.
- **User Presets:** Allowing users to save their custom EQ settings for future use.
- **Additional Filters:** Incorporating more advanced filter types and configurations for greater audio manipulation capabilities.
- **Cross-Platform Compatibility:** Developing the code to be compatible with other programming languages and platforms, broadening accessibility for users.

## Acknowledgments
This project acknowledges the foundational work in digital signal processing that has made it possible to implement effective audio equalization. Special thanks to contributors and resources that provided insights into filter design and audio processing techniques.

