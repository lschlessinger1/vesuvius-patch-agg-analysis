# Analysis of Patch Aggregation Methods in Ink Detection
[Vesuvius Challenge]([url](https://scrollprize.org/)) analysis of patch aggregation methods in ink detection

## Overview
This repository contains an analysis of different **patch aggregation methods** used for **ink detection** in the Vesuvius Challenge. The analysis explores various approaches to merging patch-based predictions into a reconstructed ink prediction.

The full analysis is available in the PDF: [**Analysis_of_patch_aggregation_methods_in_ink_detection.pdf**](https://github.com/lschlessinger1/vesuvius-patch-agg-analysis/blob/main/Analysis_of_patch_aggregation_methods_in_ink_detection.pdf)

## Open in Google Colab
To interact with the analysis notebooks, click the corresponding button below:

- **Generate and Save Patch Aggregations:**  
  [![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/14iBMVDkNcDRHMc6mpCRYPmhYUNygzMv9)

- **Quantitative Analysis:**  
  [![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1fedW_PF8FSFPKfRhOPDg9cK0xmZp5rms)

- **Qualitative Analysis:**  
  [![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1AJb0cOkotw3zg77dQ4RNI-XDYTQh-8KH)

## Summary of Methods
The following **patch aggregation** techniques were evaluated:
- **Averaging** – Each patch contributes equally to the final reconstructed image, reducing bias towards any particular pixel.
- **Gaussian** – A 2D Gaussian window emphasizes the central part of each patch, reducing boundary artifacts and smoothing transitions.
- **Cropping** – Center-cropping overlapping patch predictions before averaging, reducing the impact of window edges and corners.
- **Hanning** – A 2D Hann window emphasizes the center of each patch while smoothly tapering at the edges.

## Results
- **Evaluation Metrics:** The effectiveness of different methods was quantified using Average Precision (AP) and F0.5 score.
- **Visualization:** The repository includes qualitative comparisons of aggregated results vs. ground truth, analyzing the impact of stride, window size, and patch aggregation method on the final predictions.
