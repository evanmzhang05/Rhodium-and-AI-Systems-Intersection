# Rhodium-and-AI-Systems-Intersection
A case study analysis on the use of Python library Rhodium to develop fail cases and determine vulnerabilities in a system driven by machine learning.

**Author:** Evan Zhang (emz44)
**Course:** ENGMT5980: Decision Framing and Analytics, Cornell University

## Goals:
1. Gain an understanding of PRIM and CART and how these scenario discovery techniques divide a parameter space into separate outcome regions
2. Learn and apply Rhodium and its PRIM, CART implementation in a case study AI system, such as a simple classifier trained on public urban geospatial data
3. Perform sensitivity analysis via Rhodium to identify input parameters and model weights that lead to fail cases
4. Draw connections between findings from the case study to course concepts, specifically the concept of value alignment to discuss how different values define a different failure region, and what constitutes an error in a system
5. Document a potential workflow for performing scenario discovery and sensitivity analysis via Rhodium on AI systems to define failure regions and determine vulnerabilities

## Final Deliverable:
A working implementation of Rhodium on a case study AI system and a documented, generalizable workflow for conducting scenario discovery and sensitivity analysis on AI systems.

## Known Challenges
A potential challenge of this project is to have Rhodium perform and generalize well on even a simple case study AI system. Rhodium was not built with the intention of being integrated into a high-dimensional AI system. This is the reason why I will be using a simple AI system, although this does limit the generalizability of the workflow produced for large-scale/deep AI systems

In addition, another technical challenge is defining bounds in the input parameter space based on observed failure cases. The features of an AI system are derived from the inputs, and they may be dependent and highly correlated. By defining bounds in the input space, the resulting space must reflect real-world inputs and should not represent unfeasible data.

Another challenge is applying the concept of value alignment on quantitative scenario discovery via Rhodium. Values are difficult to quantify, and defining a measurable failure condition based on values may oversimplify the concept.

## Repository Structure
 
```
.
├── configs/            Project configuration
├── data/
│   ├── raw/            Downloaded source data
│   └── processed/      Cleaned data
├── src/
│   ├── data/           Data loading and preprocessing
│   ├── models/         Model training and evaluation
│   └── utils/          Plotting helpers
└── report/             
    └── slides/         Final slides

```

## Timeline
 
| # | Milestone | Date | % of Effort | Certainty of Success |
|---|-----------|------|-------------|----------------------|
| 1 | Review Rhodium documentation, install Rhodium and dependencies, create work environment (GitHub repo) | Oct 9 | 5% | High |
| 2 | Identify and download case study dataset and simple ML model | Oct 14 | 5% | High |
| 3 | Develop system (dataset and model) to be compatible with Rhodium | Oct 22 | 10% | Moderate-High |
| 4 | Perform scenario discovery via Rhodium (PRIM/CART), map failure regions | Nov 3 | 17.5% | Moderate |
| 5 | Perform sensitivity analysis via Rhodium, identify input parameters leading to failure | Nov 12 | 17.5% | Moderate |
| 6 | Write about the connection between value alignment and the quantitative findings | Nov 19 | 15% | Moderate |
| 7 | Document generalizable workflow | Nov 26 | 10% | Moderate-High |
| 8 | Synthesize findings, prepare visual slideshow (if applicable) | Dec 1 | 10% | High |
| 9 | Finalize report | Dec 11 | 10% | High |

## Course Concepts:
This project draws connections to multiple course concepts, most notably to the Python library Rhodium as this project will focus on its integration in an AI system. Outside of Rhodium, this project will also connect to scenario discovery and sensitivity analysis. Certain scenario discovery techniques we learn through coursework, including Patient Rule Induction Method (PRIM) and Classification and Regression Trees (CART) will be utilized for failure region mapping and defining fail cases. Sensitivity analysis serves to evaluate AI system performance and detect vulnerabilities. This project will also connect to course discussions regarding decision framing and values as the failure space is dynamically defined (which errors matter and to which stakeholders).
