# Document Layout Detection using Multi-Stage Transfer Learning

This repository contains an implementation of a multi-stage transfer learning approach for document layout detection, specifically targeting early modern Spanish manuscripts while maintaining generalization capabilities for various document types.

## Project Overview

I implement a progressive specialization strategy using YOLOv11n (You Only Look Once version 11 nano) to create a robust document layout detection model. The model is trained through three distinct phases of transfer learning to achieve both generalization and domain-specific accuracy.


### We will use the YOLOv11 Pretrained model and transfer training using a dataset available on Roboflow to create a more generalised model.

I will implement a multi-stage transfer learning approach:
1. Start with the YOLOv11 pretrained model as the foundation
2. First transfer learning phase: Train on research paper layouts to build general document understanding. Dataset --> [TFT-ID](https://universe.roboflow.com/huyifei/tft-id)
3. Second transfer learning phase: Fine-tune on early modern document layouts. Dataset --> [macro-segmentation-2pwqv](https://universe.roboflow.com/layoutorganisation/macro-segmentation-2pwqv/dataset/1)
4. Final specialization phase: Fine-tune specifically for the provided early modern Spanish documents. Dataset --> [Layout_organistion](https://universe.roboflow.com/layoutorganisation/layout_organistion/dataset/4)

