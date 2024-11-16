# Visual Vox
![](https://miro.medium.com/v2/resize:fit:828/format:webp/1*CPlq_fo37oyyH_GG8Pwcdw.jpeg)
## Project Overview:
The main objective of the LipNet project is to develop an automated lip reading system that can accurately transcribe spoken words by analyzing video sequences of lip movements. This technology has significant applications in accessibility, security, and communication systems where audio may be unavailable or unreliable.
## About the Dataset:
The dataset used in this project consists of 1000+ video recordings of a person speaking, specifically focusing on lip movements. The data is structured as video files (.mpg format) along with corresponding alignment files (.align) that contain the text transcriptions. The dataset is organized in the 's1' directory and includes multiple video samples of speaker pronouncing various phrases and words.

## Data Dictionary
| Column Name | Description |
| --- | --- |
| VideoFrames | Sequence of 75 grayscale images capturing lip movements |
| FrameDimensions | 46x140 pixels per frame, focused on mouth region |
| FramePosition | Coordinates (190:236, 80:220) for consistent mouth region capture |
| Normalization | Mean and standard deviation values used for frame normalization |
| AlignmentFile | Associated text file containing ground truth transcriptions |
| Vocabulary | 41 unique characters including: |
| - Letters | 26 lowercase letters (a-z) |
| - Numbers | Digits 1-9 |
| - SpecialChars | Special characters ('?!) |
| - Space | Space character for word separation |
| - ProcessingTokens | Additional tokens for model processing |
| FrameRate | Standard frame rate for video processing |
| VideoFormat | MPG format for input videos |
| TranscriptFormat | .align format for ground truth text |
| BatchSize | Number of videos processed together (typically 2) |
| SequenceLength | Fixed length of 75 frames per video sequence |
| OutputText | Predicted text transcription from lip movements |

This LipNet implementation successfully combines 3D CNNs and Bidirectional LSTMs to convert lip movements from video input into text predictions. The model effectively processes standardized video frames and demonstrates accurate lip reading capabilities, establishing a solid foundation for visual speech recognition technology with potential for real-world applications and future enhancements.