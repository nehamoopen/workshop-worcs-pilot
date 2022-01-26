# Writing A Reproducible Manuscript in R with WORCS

This repository contains the documentation, exercises and datasets of the single day workshop ['Writing a Reproducible Paper in R with WORCS'](https://www.uu.nl/en/research/research-data-management/training-workshops/introduction-to-r-data) at Utrecht University.
The workshop is organised by [Research Data Management Support](https://www.uu.nl/en/research/research-data-management).

## Workshop description

Open Science is becoming increasingly popular and relevant, and a world of opportunity is opening up to make your work fully reproducible. This is not without its challenges: best practices for reproducible science include a number of tools that you may never have used or even heard of before. *(Are you using version control? How are you managing your dependencies? Are you writing your manuscript as an executable document?)*

For those who would like to get started with an open and reproducible workflow, without dealing with a mountain of new tools and platforms, we introduce [WORCS](https://psyarxiv.com/k4wde/), a Workflow for Open Reproducible Code in Science. The workflow is written for R, but you do not need to have prior programming experience to join this workshop. Having the motivation to step out of your comfort zone — and into a new one — is the most important prerequisite.

WORCS is an R package that takes you from data to published paper in a single streamlined workflow, making the entire process of your analysis, up to the submission of your manuscript, reproducible. The WORCS workflow optionally facilitates pre-registration, sharing your code and your data (safely!), and the submission of a pre-print.

This workshop will be taught by [RDM Support](https://www.uu.nl/en/research/research-data-management)  in collaboration with [Caspar van Lissa](https://github.com/cjvanlissa), the author of the `worcs` package and WORCS workflow. We will give you an overview of the workflow and introduce you to its use. You will create your first reproducible project by going through all steps of the workflow yourself. 

![WORCS workflow](https://github.com/cjvanlissa/worcs/raw/master/paper/workflow_graph/workflow.png)

## Upcoming workshops
This is a pilot workshop. For upcoming workshops check [uu.nl/rdm](https://www.uu.nl/en/research/research-data-management/training-workshops/introduction-to-r-data) for upcoming workshops.
Registration is mandatory, and opens 2 months in advance of the course.

## Installation requirements
Work through the [Setup vignette: Setting up your computer for WORCS](https://cjvanlissa.github.io/worcs/articles/setup.html)

## Schedule
Most activities are done independently, using the step-by-step guides provided.
We are always available for 1:1 support during these times, and reconvene in the main channel at stated times.

| Time | Activity |
|---:|:---|
| 9:00 | Walk-in, tech support |
| 10:00 | Introductions |
| 10:15 | Introduction to WORCS |
| 10:45 | Explanation of workshop programme |
| 11:00 | Phase 1: _Study design_ |
| 11:45 | Recap & Questions |
| **12:00** | **Lunch break** |
| 12:30 | Phase 2: _Writing & analysis_ |
| 13:15 | Recap & Questions |
| 13:30 | Phase 3: _Submission & publication_ |
| 14:15 | Recap & Questions |
| 14:30 | General Discussion |
| 15:00 | **End** |


## Data 
You are encouraged to use your own data, code and manuscript text during the workshop.  
If you do not have own data, you can use [Allison Horst's Penguin dataset](https://github.com/allisonhorst/palmerpenguins).

You can use this data by entering the following code in the `prepare_data.R` script:

``` r
install.packages("remotes")
remotes::install_github("allisonhorst/palmerpenguins")
data <- palmerpenguins::penguins
```

## Workshop programme
Links to a step-by-step guide for each part of the workshop are provided below, taken from the [WORCS Workflow vignette](https://cjvanlissa.github.io/worcs/articles/workflow.html)


| Subject | Link | Additional information |
|:--------|:-------|:------|
| Phase 1: Study materials | [Step-by-step guide](https://cjvanlissa.github.io/worcs/articles/workflow.html#phase-1-study-design) | - |
| Phase 2: Writing & analysis | [Step-by-step guide](https://cjvanlissa.github.io/worcs/articles/workflow.html#phase-2-writing-and-analysis) | [Citing references in worcs](https://cjvanlissa.github.io/worcs/articles/citation.html) |
| Phase 3: Submission and publication | [Step-by-step guide](https://cjvanlissa.github.io/worcs/articles/workflow.html#phase-3-submission-and-publication) |  |

### Notes for cautious researchers

Some researchers might want to share their work only once the paper is accepted for publication. In this case, we recommend creating a "Private" repository in Step 1, and completing Steps 13-17 upon acceptance by the journal.


## Additional resources
This [paper in Data Science](https://doi.org/10.3233/DS-210031) introduces the WORCS workflow, explains the underlying tools, and illustrates how the `worcs` package can be used to create a new project that follows the workflow.


**Sample WORCS projects**
For a list of sample `worcs` projects created by the authors and other users, see the [`README.md` file on the WORCS GitHub page](https://github.com/cjvanlissa/worcs). This list is regularly updated.


## Acknowledgements
The workshop 'Introduction to R & data' is developed and maintained by [Research Data Management Support](https://www.uu.nl/en/research/research-data-management) at Utrecht University.
All videos were recorded by [Jacques Flores](https://www.uu.nl/medewerkers/jpflores).
The workshop documentation was written by [Neha Moopen Vreede](https://github.com/nehamoopen) and [Bianca Kramer Vreede](https://github.com/bmkramer), based on an earlier versions by [Barbara Vreede](https://github.com/bvreede).


**Image attribution**  
The [Git Logo](https://git-scm.com/) by Jason Long is licensed under the Creative Commons Attribution 3.0 Unported License. The [OSF logo](https://osf.io/) is licensed under CC0 1.0 Universal. Icons in the workflow graph are obtained from [Flaticon](https://www.flaticon.com); see [detailed attribution](https://github.com/cjvanlissa/worcs/blob/master/paper/workflow_graph/Attribution_for_images.txt).
