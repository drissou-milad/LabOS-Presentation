# LabOS – Selected Experimental Results

## 1. Purpose

This document presents selected technical development activities and preliminary experimental results from LabOS.

The objective is to provide evidence of ongoing software development, computational experimentation and evaluation work.

The results presented here should be interpreted within their specific experimental conditions. They do not establish complete system reliability or generalisation across biological microscopy datasets.

## 2. Development and Evaluation Activities

The development process has included several technical activities:

- Implementation of cell tracking functionality.
- Development of lineage reconstruction logic.
- Work on division-related tracking behaviour.
- Evaluation using biological image datasets.
- Investigation of AI-based cell detection.
- Benchmark methodology development.
- Dataset and evaluation consistency auditing.

These activities represent different stages of development and validation.

## 3. Cell Tracking and Lineage Development

LabOS includes an assignment-based cell tracking implementation using the Hungarian algorithm.

The tracking component associates detections across consecutive frames using distance-based constraints.

The lineage component aims to reconstruct parent–daughter relationships and represent cellular development across generations.

Development and testing have covered cases including:

- Cell association across frames.
- Division-related relationships.
- Empty detections and frames.
- Lineage reconstruction.
- Dataframe and CSV data handling.

These tests provide evidence of software implementation and functional testing. They should not be interpreted as proof of biological accuracy on all microscopy datasets.

## 4. Benchmark and Dataset Evaluation

The project has included work on:

- Cell Tracking Challenge (CTC) benchmark methodology.
- TrackMate baseline integration.
- Biological dataset evaluation.
- Distance-gated evaluation.
- Experimental detector development.
- Held-out evaluation procedures.

The objective is to establish a reproducible evaluation approach and investigate the behaviour of LabOS components under defined experimental conditions.

## 5. Preliminary AI Detector Evaluation

One experimental evaluation was conducted using a held-out test split from the detector development workflow.

### 5.1 Experimental configuration

| Parameter | Recorded configuration |
|---|---|
| Experiment | Run13 |
| Dataset context | 20-sample training dataset |
| Evaluation split | Held-out test split |
| Input patch | 32 × 32 pixels |
| Central region | 16 × 16 pixels |
| Zoom factor | 2.0 |
| Image normalisation | Robust normalisation |
| Model | CellCNNNoClassifierReLU |
| Positive patches | 111 |
| Negative patches | 16,476 |
| Total patches | 16,587 |

The evaluation used a held-out test set. The reported patch counts describe the evaluated patch collection.

### 5.2 Preliminary results

| Metric | Result |
|---|---:|
| ROC-AUC | 0.6560 |
| PR-AUC | 0.01439 |
| Balanced accuracy | 0.5955 |
| Precision | 0.00946 |
| Recall | 0.64865 |
| F1-score | 0.01865 |

### 5.3 Confusion matrix

At the evaluated threshold of 0.50:

| | Predicted negative | Predicted positive |
|---|---:|---:|
| Actual negative | 8,936 | 7,540 |
| Actual positive | 39 | 72 |

### 5.4 Interpretation

These results show that the experimental detector remains limited.

Although the measured recall was approximately 0.649, precision was very low at approximately 0.0095.

The low precision indicates that many predicted positive patches were false positives.

The PR-AUC of 0.01439 also indicates weak performance under the evaluated class-imbalanced conditions.

Consequently, these results do not establish that the detector is sufficiently reliable for general biological image analysis.

Further work is required to investigate:

- Class imbalance.
- False-positive reduction.
- Detection threshold selection.
- Generalisation to additional biological samples.
- The effect of detection errors on downstream tracking.
- Performance under weak-signal and noisy imaging conditions.

**The detector must be described as experimental, not validated or production-ready.**

## 6. Dataset and Evaluation Consistency Audit

A separate audit examined the consistency between patch metadata and ground-truth cell annotations.

The recorded audit included:

| Audit item | Result |
|---|---:|
| Total audited rows | 155,116 |
| Positive labels | 1,847 |
| Negative labels | 153,269 |
| Training rows | 105,476 |
| Validation rows | 29,964 |
| Test rows | 19,676 |
| Manifest-to-patch consistency flags | 0 |

The audit found zero rows flagged for the specific consistency condition tested: a manifest nearest-ground-truth distance below 16 pixels while the corresponding patch search found no ground-truth cell inside the patch.

This result supports consistency for that particular audit condition. It does not establish that the entire dataset or annotation process is error-free.

The audit also identified negative-labelled patches containing ground-truth cells within a 32-pixel region:

- Training: 3,671
- Validation: 1,285
- Test: 419

These cases require careful interpretation because the presence of a ground-truth cell within a broader region does not necessarily mean that the cell lies inside the central labelled region.

Further investigation is required before drawing conclusions about their effect on model training and evaluation.

## 7. Software Testing

Software testing has been used throughout the development of tracking and lineage components.

An earlier recorded test run reported:

**104 tests passed.**

This is evidence of software-level testing at that development stage. It does not constitute independent scientific validation or demonstrate that every component performs reliably on real-world biological data.

## 8. Current Experimental Limitations

The current experimental work has several limitations:

1. The AI detector has weak preliminary precision.
2. Detection performance requires further improvement.
3. Additional biological datasets are needed for broader evaluation.
4. Tracking reliability must be examined under difficult imaging conditions.
5. Division detection requires further independent assessment.
6. Lineage reconstruction requires additional biological validation.
7. More comparative experiments are needed.

## 9. Future Experimental Priorities

The next experimental stages should focus on:

- Improving detector precision.
- Investigating class imbalance and threshold selection.
- Evaluating detection and tracking together.
- Testing large inter-frame displacement cases.
- Analysing tracking interruptions and incorrect associations.
- Evaluating division-event reconstruction.
- Comparing appropriate components against established tools.
- Obtaining independent researcher feedback.
- Testing with additional real laboratory microscopy data.

## 10. Conclusion

The experimental development of LabOS demonstrates ongoing technical work in biological image analysis, cell tracking, lineage reconstruction and AI-based detection.

The preliminary detector results also reveal important limitations that must be addressed before broader scientific claims can be made.

LabOS therefore remains a research software project under development, with further technical improvement and independent validation as essential next steps.

---

**Project:** LabOS  
**Developer:** Milad Ouiam Drissou  
**Country:** Algeria  
**Research domains:** Artificial Intelligence · Computer Vision · Bioimage Analysis · Computational Biology

*Results are reported for their specific experimental configurations and should not be generalised beyond the evaluated conditions.*
