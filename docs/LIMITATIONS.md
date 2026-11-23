# LabOS — Current Limitations and Development Challenges

## 1. Purpose of This Document

This document describes the current technical and scientific limitations of LabOS.

LabOS is an independently developed research software project. Its development involves ongoing experimentation, evaluation and refinement. The limitations described below define the current scope of the project and identify areas requiring further investigation.

They are not presented as permanent limitations, but as challenges guiding future development.

## 2. AI-Based Cell Detection

The AI-assisted cell detection component is still experimental.

Current challenges include:

- Distinguishing cells from background structures.
- Detecting cells when image signals are weak or noisy.
- Maintaining detection quality under variations in image contrast.
- Reducing false-positive and false-negative detections.
- Improving generalisation to microscopy images that differ from the development data.

Preliminary experiments have been conducted, but the current detection performance is not yet sufficient to claim reliable general-purpose cell detection.

Further training, dataset refinement, threshold analysis and independent evaluation are required.

## 3. Cell Tracking Reliability

Cell tracking is affected by changes in cell position, appearance and image quality between consecutive frames.

Important challenges include:

- Large displacement between consecutive frames.
- Rapid cellular movement.
- Temporary detection failures.
- Similarity between neighbouring cells.
- Cells entering or leaving the observable field.
- Maintaining consistent cell identities over longer sequences.

Assignment-based tracking provides a foundation for associating cells across frames. However, its reliability under complex biological conditions requires further evaluation.

## 4. Cell Division and Lineage Reconstruction

Cell division introduces additional complexity because one parent cell may produce two daughter cells.

Although LabOS includes division-related logic and lineage reconstruction capabilities, further work is needed to evaluate:

- Correct identification of division events.
- Accurate parent–daughter relationships.
- Missing or delayed detections around division events.
- Incorrect associations between neighbouring cells.
- Long-term consistency of reconstructed lineage trees.

The biological accuracy of lineage reconstruction must be assessed using appropriate annotated microscopy sequences and expert feedback.

## 5. Image Quality and Acquisition Conditions

Microscopy data can vary significantly depending on acquisition conditions.

LabOS still requires broader testing with challenging image conditions, including:

- Out-of-focus images.
- Low signal-to-noise ratios.
- Uneven illumination.
- Weak cellular boundaries.
- Motion and acquisition artefacts.
- Changes in image contrast across time.

These conditions can affect detection, tracking and subsequent lineage analysis.

## 6. Dataset Coverage and Generalisation

The initial development focuses on biological microscopy data, particularly developing zebrafish embryo imaging.

The current evaluation does not establish that LabOS generalises to every biological model, cell type, microscope or imaging protocol.

Additional datasets are needed to investigate:

- Performance across different biological samples.
- Differences between imaging technologies.
- Variations in cell density and morphology.
- Differences in temporal resolution.
- Generalisation to independent research datasets.

Any extension to other biological domains will require domain-specific evaluation.

## 7. Experimental Validation

The project has undergone technical development and preliminary experiments. However, further validation is necessary before making strong claims about scientific reliability.

Future validation should include:

- More extensive testing on independent datasets.
- Comparison with established bioimage-analysis tools.
- Quantitative evaluation using appropriate tracking and detection metrics.
- Expert review of detection, tracking and lineage results.
- Testing under realistic and challenging microscopy conditions.

Software tests can verify expected computational behaviour, but they do not independently establish biological accuracy.

## 8. Research Scope and Clinical Limitations

LabOS is currently intended as a research-oriented software project.

It is not:

- A clinically validated diagnostic system.
- A certified medical device.
- A replacement for biological expertise.
- A validated cancer detection or diagnosis system.
- A production-ready solution for clinical decision-making.

Potential applications in cancer research and other biological fields remain future research directions requiring dedicated datasets, experiments and validation.

## 9. Current Development Priorities

The main priorities for addressing these limitations are:

1. Improve the reliability of AI-assisted cell detection.
2. Strengthen tracking under large inter-frame displacement.
3. Improve division-event identification and lineage consistency.
4. Expand evaluation using challenging microscopy images.
5. Compare results with established analysis tools.
6. Obtain structured feedback from biologists and bioimage-analysis researchers.
7. Evaluate the system on additional independent datasets.

## 10. Conclusion

LabOS is an ongoing research and development project with an initial technical foundation in biological image analysis, cell tracking and lineage reconstruction.

Its current limitations highlight the need for further experimentation, scientific collaboration and independent validation.

The development strategy is therefore focused on progressively improving reliability and demonstrating the scientific value of the system through measurable results rather than making unsupported performance claims.
