

# GBAT: GazeBehavior Annotation Toolkit

GBAT is a toolkit for processing multimodal recordings of adult and children behavior. It has functions in extracting features from both egocentric and third-person video recordings. It includes three main components: a Video Synchronizer, a Gaze Target Annotator, and a Video Content Annotator.

## Why this toolkit exists
Children actively explore the world to learn its underlying causal structure. They use eye movements both to guide learning and to communicate intentions in social interactions. Head-mounted eye tracking enables researchers to study these gaze-based attentional processes in naturalistic behaviors. When combined with third-person audio and video recordings, such multimodal data also support analysis of the relationships among gaze targets, speech input, and body activity. However, these recordings are highly dense: children aged five to sixteen years make three to five saccades per second, and videos are typically recorded at tens of frames per second. This makes manual annotation of gaze targets and actions extremely labor-intensive. To facilitate the processing of multimodal recordings from egocentric and third-person videos, we developed the semi-automati GazeBehavior Annotation Toolkit (GBAT).

## Toolkit components

### Tool 1: Video Synchronizer
This post-hoc video synchronizer estimates temporal discrepancies among different video recordings based on spectrograms derived from corresponding audio recordings. It uses one-dimensional convolution to compute cross-correlations between these spectrograms over a range of temporal lags.

- Repository: [https://github.com/CaiLab-neuro/Video_Synchronizer.git]

### Tool 2: Gaze Target Annotator
This Gaze Target Annotator enables semi-automatic segmentation of major objects
appearing in the scene cameras of head-mounted eye trackers.
The annotator includes two stages: 1. object segmentation
based on a prompt-based video segmentation mode Segment
Anything Model 2 (SAM2) 2. alignment between time
stamps of gaze coordinate and that of the video frames to
infer gaze targets based on object segmentation masks.
A SAM2-based user interface (UI) is also included, which allows users to provide positive prompts (points
placed within the target object) and negative prompts (points
placed on visually similar but irrelevant regions) to guide the
segmentation. 

- Repository: [https://github.com/CaiLab-neuro/Sam2UI.git]

### Tool 3: Video Content Annotator
Video Content Annotator utilizes
a state-of-the-art open-source model Tarsier 2 (specifically,
the variant Tarsier2-7B) to generate time-resolved annota-
tions of video contents. 
- Repository: [https://github.com/CaiLab-neuro/video_annotator.git]

## End-to-end workflow
1. Synchronize videos
2. Annotate gaze targets
3. Annotate video content
4. Export structured outputs

## Installation
Explain that each tool is installed separately.

## Example data
Link to toy/example dataset.

## Citation
Tell people to use the GitHub citation widget or the BibTeX below.

## License

## Contact
