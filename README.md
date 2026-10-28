# BMSCNet

BMSCNet is a lightweight video violence recognition network built on MobileNetV2. It combines bidirectional temporal modeling with sensitivity-calibrated attention for video-level recognition.

## Method

- **Bi-EMSG (Bidirectional Extended Motion-Shift Gating)** combines compact motion features, extended local temporal context, and direction-aligned gating to dynamically fuse information across frames.
- **PSCA (Perturbation Sensitivity Calibration Attention)** uses frame-level perturbation sensitivity to guide temporal attention during training. At inference, the learned attention head directly aggregates frame features in a single pass.

## Results

The following results are means over three random seeds, as reported in the manuscript.

| Dataset | Accuracy (%) | F1 Score (%) |
| --- | ---: | ---: |
| Crowd Violence | 99.080 | 99.070 |
| Hockey Fights | 98.667 | 98.662 |
| RWF-2000 | 88.917 | 88.866 |

BMSCNet outperforms the three MobileNetV2-based temporal baselines under the same evaluation protocol across all three datasets. The reported resource costs on RWF-2000 are **17.00 MB** of parameter storage and **5.0 GFLOPs**.
