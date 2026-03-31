# GBAT: GazeBehavior Annotation Toolkit

GBAT is a toolkit for processing multimodal recordings of adult and children behavior. It has functions in extracting features from both egocentric and third-person video recordings. It includes three main components: a Video Synchronizer, a Gaze Target Annotator, and a Video Content Annotator.

## Why this toolkit exists

Children actively explore the world to learn its underlying causal structure. They use eye movements both to guide learning and to communicate intentions in social interactions. Head-mounted eye tracking enables researchers to study these gaze-based attentional processes in naturalistic behaviors. When combined with third-person audio and video recordings, such multimodal data also support analysis of the relationships among gaze targets, speech input, and body activity. However, these recordings are highly dense: children aged five to sixteen years make three to five saccades per second, and videos are typically recorded at tens of frames per second. This makes manual annotation of gaze targets and actions extremely labor-intensive. To facilitate the processing of multimodal recordings from egocentric and third-person videos, we developed the semi-automatic GazeBehavior Annotation Toolkit (GBAT).

This top-level repository groups the three component tools in one workspace:

- `Video_Synchronizer` for aligning recordings with audio-based synchronization
- `Sam2UI` for object segmentation and gaze-target annotation
- `video_annotator` for automated behavioral video annotation

## Repository Structure

### `Video_Synchronizer`
Tools for post-hoc alignment of video recordings using audio information.

Top-level files:

- `extract_audios_1.py`
- `video_aligner_publish_2.py`
- `gaze_frame_alignment_in_cut_3.py`

See [Video_Synchronizer/README.md](https://github.com/CaiLab-neuro/Video_Synchronizer.git).

### `Sam2UI`
Annotation and processing tools for video object segmentation built around a SAM2 workflow.

Top-level files:

- `install.py`
- `sam2_ui.py`
- `process_annotations.py`
- `gazed_object_published_version.py`
- `segment.py`

See [Sam2UI/README.md](https://github.com/CaiLab-neuro/Sam2UI.git).

### `video_annotator`
Pipeline for generating time-resolved behavioral annotations from video.

Top-level files:

- `install.py`
- `annotate_video.py`
- `run_prompt_presets.py`
- `eaf_to_csv.py`
- `visualizer.py`

Supporting directories:

- `data`
- `profiles`
- `prompts`
- `scripts`
- `tarsier`

See [video_annotator/README.md](https://github.com/CaiLab-neuro/video_annotator.git).

## Suggested Workflow

1. Use `Video_Synchronizer` to align recordings.
2. Use `Sam2UI` to segment objects and support gaze-target annotation.
3. Use `video_annotator` to generate behavioral annotations from video segments.

## Installation

Each component has its own setup steps and dependencies. Install and run them from their respective directories using the instructions in their local READMEs.

## Contact
Yanbin Xu (yxx744@miami.edu)
Dr. Mingbo Cai (mingbo.cai@miami.edu)


