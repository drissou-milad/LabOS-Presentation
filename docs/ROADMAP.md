# LabOS — Development Roadmap

## 1. Vision

LabOS aims to become an AI-assisted research workspace for biological microscopy image analysis, helping researchers investigate cellular behaviour, track cells over time and reconstruct cell lineages.

The long-term vision is to bring image processing, cell detection, tracking, division analysis, lineage reconstruction and quantitative reporting into a unified workflow.

This roadmap describes the planned evolution of the project from its current research prototype toward a more reliable and scientifically validated platform.

## 2. Development Strategy

Development is organised into progressive phases. Each phase has technical objectives and validation requirements.

The roadmap is flexible: priorities may evolve based on experimental findings and feedback from researchers.

## 3. Development Phases

### Phase 1 — Core Architecture and Foundations

**Status: Implemented foundation**

Objectives:
- Establish the main project architecture.
- Develop the initial image-analysis workflow.
- Implement core cell-tracking functionality.
- Introduce data structures for representing cell observations and tracks.
- Develop lineage-related processing.
- Establish automated software testing.

Expected outcome:

A functional software foundation for developing and evaluating cell-analysis workflows.

### Phase 2 — Tracking and Lineage Development

**Status: Implemented foundation / ongoing improvement**

Objectives:
- Improve cell association across consecutive frames.
- Handle challenging inter-frame displacement.
- Develop division-related event handling.
- Improve parent–daughter relationship reconstruction.
- Evaluate tracking and lineage behaviour on biological image sequences.

Expected outcome:

A more robust tracking and lineage-analysis workflow capable of supporting further biological evaluation.

### Phase 3 — AI-Assisted Cell Detection

**Status: Experimental**

Objectives:
- Develop and evaluate AI-assisted cell detection approaches.
- Investigate image preprocessing and normalisation strategies.
- Improve detection under weak-signal and noisy conditions.
- Reduce false-positive detections.
- Evaluate performance on held-out data.
- Investigate the limitations of the current experimental detector.

Expected outcome:

An experimentally evaluated detection component with clearly documented strengths and limitations.

### Phase 4 — Benchmarking and Scientific Evaluation

**Status: In progress**

Objectives:
- Establish reproducible evaluation procedures.
- Compare selected tracking approaches with established tools.
- Evaluate detection and tracking using appropriate quantitative metrics.
- Investigate performance under challenging image conditions.
- Analyse errors and inconsistencies in datasets and annotations.
- Obtain independent feedback from biological and bioimage-analysis researchers.

Expected outcome:

A stronger evidence base for assessing the technical performance and scientific relevance of LabOS.

### Phase 5 — Researcher-Oriented Workspace

**Status: Planned**

Objectives:
- Improve the user interface and workflow organisation.
- Provide clearer visualisation of cell tracks.
- Display cell division events and lineage relationships.
- Organise quantitative analysis outputs.
- Support exportable results and research reports.
- Improve usability for researchers who are not software developers.

Expected outcome:

A more accessible research environment for exploring and analysing biological microscopy data.

### Phase 6 — Broader Biological Evaluation

**Status: Future objective**

Objectives:
- Evaluate LabOS on additional independent biological datasets.
- Investigate generalisation to different cell types and imaging conditions.
- Explore applications in developmental biology and other research domains.
- Investigate potential use in cancer research through dedicated experiments.
- Collaborate with research laboratories for domain-specific evaluation.

Expected outcome:

A clearer understanding of the scientific applications, generalisation limits and potential research value of LabOS.

### Phase 7 — Research Platform Maturity

**Status: Long-term vision**

Objectives:
- Improve software reliability and maintainability.
- Strengthen reproducibility and experiment management.
- Improve documentation and installation procedures.
- Establish a structured validation process.
- Develop research collaborations and collect systematic user feedback.
- Assess the requirements for wider research deployment.

Expected outcome:

A mature research software platform supported by documented evaluation, reproducible workflows and scientific collaboration.

## 4. Current Priorities

The immediate priorities are:

| Priority | Development objective |
|---|---|
| 1 | Improve AI-assisted cell detection |
| 2 | Strengthen tracking under large displacement |
| 3 | Improve division and lineage consistency |
| 4 | Expand evaluation on challenging microscopy images |
| 5 | Complete systematic benchmark analysis |
| 6 | Obtain structured feedback from researchers |
| 7 | Improve the presentation of results and limitations |

## 5. Validation Strategy

LabOS development will be guided by measurable technical and scientific evidence.

The validation strategy includes:

- Automated software tests.
- Quantitative evaluation on annotated datasets.
- Held-out experimental evaluation.
- Comparison with established bioimage-analysis approaches.
- Visual inspection of challenging cases.
- Feedback from biologists, computational biologists and bioimage analysts.
- Further evaluation on independent research data.

The completion of a development phase will depend on its evaluation criteria, not only on the implementation of its features.

## 6. Research Collaboration

Collaboration is an important part of the project's development.

LabOS seeks feedback from:

- Developmental biology researchers.
- Computational biologists.
- Bioimage-analysis specialists.
- Computer vision and artificial intelligence researchers.
- Microscopy laboratories.

Researcher feedback will help identify practical needs, prioritise improvements and define meaningful evaluation scenarios.

## 7. Long-Term Direction

The long-term objective is to develop LabOS into a research-oriented platform that helps scientists move from microscopy images to structured cellular observations and lineage-based analysis.

Rather than focusing only on implementing more features, the project aims to improve the reliability, interpretability and reproducibility of biological image analysis.

**LabOS is being developed progressively, with scientific validation and researcher needs guiding its evolution.**
