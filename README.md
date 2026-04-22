<div align="center" markdown>

<img src="https://i.imgur.com/UdBujFN.png" width="250" /> <br>

# Sugar Beet Multiview Tracking Sample

<p align="center">
  <a href="#overview">Overview</a> •
  <a href="#use-cases-for-farmers">Use cases for farmers</a> •
  <a href="#source-dataset--license">Source Dataset & License</a> •
  <a href="#labeling-interface">Labeling Interface</a> •
  <a href="#download">Download</a> •
</p>

[![](https://img.shields.io/badge/slack-chat-green.svg?logo=slack)](https://supervisely.com/slack)
![GitHub release (latest SemVer)](https://img.shields.io/github/v/release/supervisely-ecosystem/SugarBeet-Multiview-Sample-project-annotated)
[![views](https://app.supervisely.com/img/badges/views/supervisely-ecosystem/SugarBeet-Multiview-Sample-project-annotated.png)](https://supervisely.com)
[![downloads](https://app.supervisely.com/img/badges/downloads/supervisely-ecosystem/SugarBeet-Multiview-Sample-project-annotated.png)](https://supervisely.com)

</div>

## Overview

This is an annotated multiview sample project featuring tractor-mounted camera data of a sugar beet field capturing growing leaves in both RGB (color) and NIR (near-infrared) spectrums. The project includes both images and videos, demonstrating object tracking capabilities with pre-annotated masks. The multiview setup provides synchronized RGB and NIR data streams, simulating real-world multi-spectral agricultural monitoring scenarios where different spectral bands help distinguish vegetation from soil and detect plant health variations.

This sample project is based on data from the [Sugar Beets 2016 dataset](https://datasetninja.com/sugar-beets-2016), an agricultural robot dataset collected on a sugar beet farm near Bonn, Germany, focusing on plant classification, localization, and mapping.

<img src="https://github.com/supervisely-ecosystem/SugarBeet-Multiview-Sample-project-annotated/releases/download/v1.0.0/beetroot.png" />

## Use cases for farmers

This type of annotation is directly applicable to real-world precision agriculture workflows. Farmers and agri-tech teams can use similar labeled data to:

- **Distinguish crops from weeds** — automatically identify and segment sugar beet plants from weeds to enable targeted weed control and reduce herbicide usage
- **Enable precision weeding** — train AI models for robotic weed removal systems that can mechanically eliminate weeds without damaging crops
- **Monitor crop health using multi-spectral data** — leverage NIR imagery alongside RGB to detect early signs of plant stress, disease, or nutrient deficiency
- **Track plant growth stages** — automatically monitor sugar beet development from emergence to maturity for optimal timing of field operations
- **Optimize crop spacing and density** — analyze plant distribution patterns to assess field uniformity and identify areas requiring replanting or thinning
- **Support autonomous farming robots** — provide training data for agricultural robots that navigate fields and perform targeted interventions on individual plants

Using the Supervisely platform, farmers and agronomists can:

- Upload drone footage directly and annotate it with [Segment Anything 2.1](https://dev.internal.supervisely.com/ecosystem/apps/serve-segment-anything-2?id=330)
- Use [AutoTrack](https://docs.supervisely.com/labeling/labeling-toolbox/videos-3.0#auto-tracking) to automatically propagate annotations across video frames, significantly reducing labeling time
- Train and deploy custom CV models on their own field data using [Supervisely training pipelines](https://docs.supervisely.com/neural-networks/overview)
- Build end-to-end labeling and model deployment workflows without leaving the platform

All annotations are stored in Supervisely format, compatible with the platform's video annotation tools and export options.

## Source Dataset & License

This sample project is derived from the **Sugar Beets 2016** dataset:

- **Dataset Homepage**: [Sugar Beets 2016 on Dataset Ninja](https://datasetninja.com/sugar-beets-2016)
- **Original Source**: [University of Bonn](https://www.ipb.uni-bonn.de/data/sugarbeets2016/)
- **License**: [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/legalcode)
- **Citation**: Chebrolu, N., Lottes, P., Schaefer, A., Winterhalter, W., Burgard, W., & Stachniss, C. (2017). Agricultural robot dataset for plant classification, localization and mapping on sugar beet fields. _The International Journal of Robotics Research_.

The original dataset was collected using the BoniRob agricultural robot platform equipped with multi-spectral cameras, RGB-D sensors, lidar, and GPS sensors over a three-month period in spring 2016.

## Labeling Interface

### Images Project

In the **images project**, the multiview labeling interface displays RGB and NIR images side by side. Each image pair represents a single frame, and **each annotation is unique and independent** — meaning that annotations on one frame do not automatically appear on other frames. This format is ideal for:

- Detailed frame-by-frame analysis
- Training instance segmentation models
- Cases where plant appearance varies significantly between frames

<img src="https://github.com/supervisely-ecosystem/SugarBeet-Multiview-Sample-project-annotated/releases/download/v1.0.0/images_li.png" />

### Videos Project

In the **videos project**, the multiview interface provides synchronized playback of RGB and NIR video streams. Annotations use **object tracking** — when you annotate an object on one frame, it is automatically tracked across subsequent frames, maintaining the same object ID throughout the video. This approach:

- Significantly reduces annotation time
- Enables temporal analysis and motion tracking
- Maintains object identity across the entire video sequence

<img src="https://github.com/supervisely-ecosystem/SugarBeet-Multiview-Sample-project-annotated/releases/download/v1.0.0/beetrootdemo.gif" />

## Source Dataset & License

This sample project is derived from the **Sugar Beets 2016** dataset:

- **Dataset Homepage**: [Sugar Beets 2016 on Dataset Ninja](https://datasetninja.com/sugar-beets-2016)
- **Original Source**: [University of Bonn](https://www.ipb.uni-bonn.de/data/sugarbeets2016/)
- **License**: [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/legalcode)
- **Citation**: Chebrolu, N., Lottes, P., Schaefer, A., Winterhalter, W., Burgard, W., & Stachniss, C. (2017). Agricultural robot dataset for plant classification, localization and mapping on sugar beet fields. _The International Journal of Robotics Research_.

The original dataset was collected using the BoniRob agricultural robot platform equipped with multi-spectral cameras, RGB-D sensors, lidar, and GPS sensors over a three-month period in spring 2016.

## Download

This project is available in two formats in Supervisely format:

- **Video project** (with tracking annotations): [Download ZIP archive](https://github.com/supervisely-ecosystem/SugarBeet-Multiview-Sample-project-annotated/releases/download/v1.0.0/project_videos.zip)
- **Images project** (frame-by-frame annotations): [Download ZIP archive](https://github.com/supervisely-ecosystem/SugarBeet-Multiview-Sample-project-annotated/releases/download/v1.0.0/project_images.zip)

### How to Import

Since this is a **multiview project** with synchronized RGB and NIR data streams, follow these steps to import it correctly:

1. Go to **Projects** in your Supervisely workspace
2. Click **+ New** → **New Project**
3. Choose the data type: **Videos** or **Images** (depending on which archive you downloaded)
4. In the **Labeling interface** select **Multiview**
5. Upload the downloaded ZIP archive
6. The multiview structure (RGB + NIR pairs) will be automatically preserved

<img src="https://github.com/supervisely-ecosystem/SugarBeet-Multiview-Sample-project-annotated/releases/download/v1.0.0/import.png" />
