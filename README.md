<div align="center" markdown>

<img src="https://i.imgur.com/UdBujFN.png" width="250" /> <br>

# Sugar Beet Multiview Tracking Sample

<p align="center">
  <a href="#overview">Overview</a> •
  <a href="#use-cases-for-farmers">Use cases for farmers</a> •
  <a href="#download">Download</a>
</p>

[![](https://img.shields.io/badge/slack-chat-green.svg?logo=slack)](https://supervisely.com/slack)
![GitHub release (latest SemVer)](https://img.shields.io/github/v/release/supervisely-ecosystem/agro-field-tracking-video-sample-annotated)
[![views](https://app.supervisely.com/img/badges/views/supervisely-ecosystem/agro-field-tracking-video-sample-annotated.png)](https://supervisely.com)
[![downloads](https://app.supervisely.com/img/badges/downloads/supervisely-ecosystem/agro-field-tracking-video-sample-annotated.png)](https://supervisely.com)

</div>

## Overview

This is an annotated multiview sample project featuring tractor-mounted camera data of a sugar beet field capturing growing leaves in both RGB (color) and NIR (near-infrared) spectrums. The project includes both images and videos, demonstrating object tracking capabilities with pre-annotated masks created using automated annotation tools [Serve Segment Anything 2.1](https://dev.internal.supervisely.com/ecosystem/apps/serve-segment-anything-2?id=330) and [AutoTrack](https://docs.supervisely.com/labeling/labeling-toolbox/videos-3.0#auto-tracking), eliminating the need for manual frame-by-frame annotation. The multiview setup provides synchronized RGB and NIR data streams, simulating real-world multi-spectral agricultural monitoring scenarios where different spectral bands help distinguish vegetation from soil and detect plant health variations.

This sample project is based on data from the [Sugar Beets 2016 dataset](https://datasetninja.com/sugar-beets-2016), an agricultural robot dataset collected on a sugar beet farm near Bonn, Germany, focusing on plant classification, localization, and mapping.

<img src="https://github.com/supervisely-ecosystem/agro-field-tracking-video-sample-annotated/releases/download/v1.0.0/agro-field.png" />

## Use cases for farmers

This type of annotation is directly applicable to real-world precision agriculture workflows. Farmers and agri-tech teams can use similar labeled data to:

- **Monitor field boundaries** — automatically detect and track the edges of cultivated plots across seasons to control land use and identify encroachments
- **Analyze tractor routes** — track machinery paths to optimize coverage, reduce fuel consumption, and detect missed or overlapping passes
- **Assess road and access conditions** — identify dirt roads and field access routes to plan logistics and maintenance
- **Detect crop zone changes** — track vegetation patterns over time to spot areas of poor growth, waterlogging, or pest damage early
- **Support precision farming systems** — feed annotated video data into AI models for autonomous machinery guidance, yield prediction, and soil health analysis

Using the Supervisely platform, farmers and agronomists can:

- Upload drone footage directly and annotate it with [Segment Anything 2.1](https://dev.internal.supervisely.com/ecosystem/apps/serve-segment-anything-2?id=330)
- Use [AutoTrack](https://docs.supervisely.com/labeling/labeling-toolbox/videos-3.0#auto-tracking) to automatically propagate annotations across video frames, significantly reducing labeling time
- Train and deploy custom CV models on their own field data using [Supervisely training pipelines](https://docs.supervisely.com/neural-networks/overview)
- Build end-to-end labeling and model deployment workflows without leaving the platform

<img src="https://github.com/supervisely-ecosystem/agro-field-tracking-video-sample-annotated/releases/download/v1.0.0/agro-field-demo.gif" />

All annotations are stored in Supervisely format, compatible with the platform's video annotation tools and export options.

## Source Dataset & License

This sample project is derived from the **Sugar Beets 2016** dataset:

- **Dataset Homepage**: [Sugar Beets 2016 on Dataset Ninja](https://datasetninja.com/sugar-beets-2016)
- **Original Source**: [University of Bonn](https://www.ipb.uni-bonn.de/data/sugarbeets2016/)
- **License**: [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/legalcode)
- **Citation**: Chebrolu, N., Lottes, P., Schaefer, A., Winterhalter, W., Burgard, W., & Stachniss, C. (2017). Agricultural robot dataset for plant classification, localization and mapping on sugar beet fields. _The International Journal of Robotics Research_.

The original dataset was collected using the BoniRob agricultural robot platform equipped with multi-spectral cameras, RGB-D sensors, lidar, and GPS sensors over a three-month period in spring 2016.

## Download

This project sample in Supervisely format: [Download ZIP archive](https://github.com/supervisely-ecosystem/agro-field-tracking-video-sample-annotated/releases/download/v1.0.0/project.zip)
