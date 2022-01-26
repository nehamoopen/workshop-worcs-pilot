# Writing A Reproducible Manuscript in R with WORCS

[![go to the course website](https://img.shields.io/badge/go%20to%20the-course%20website-blue)](https://nehamoopen.github.io/workshop-worcs-pilot/)
<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/80x15.png" /></a>

This repository contains materials for the single-day workshop ['Writing a Reproducible Paper in R with WORCS'](https://www.uu.nl/en/events/writing-a-reproducible-paper-in-r-with-worcs) at Utrecht University.  

## Workshop Description

Open Science is becoming increasingly popular and relevant, and a world of opportunity is opening up to make your work fully reproducible. This is not without its challenges: best practices for reproducible science include a number of tools that you may never have used or even heard of before - *Are you using version control? How are you managing your dependencies? Are you writing your manuscript as an executable document?*

For those who would like to get started with an open and reproducible workflow, without dealing with a mountain of new tools and platforms, we introduce [WORCS](https://psyarxiv.com/k4wde/), a *Workflow for Open Reproducible Code in Science*. The workflow is written for R, but you do not need to have prior programming experience to join this workshop. Having the motivation to step out of your comfort zone — and into a new one — is the most important prerequisite.

WORCS is an R package that takes you from data to published paper in a single streamlined workflow, making the entire process of your analysis, up to the submission of your manuscript, reproducible. The WORCS workflow optionally facilitates pre-registration, sharing your code and your data (safely!), and the submission of a pre-print.

This workshop will be taught by UU's [Research Data Management Support](https://www.uu.nl/en/research/research-data-management) in collaboration with [Caspar van Lissa](https://github.com/cjvanlissa), author of the `worcs` package and the WORCS workflow. We will give you an overview of the workflow and introduce you to its use. You will create your first reproducible project by going through all steps of the workflow yourself.

![WORCS workflow](https://github.com/cjvanlissa/worcs/raw/master/paper/workflow_graph/workflow.png)

## Upcoming Workshops
This is a pilot workshop. Upcoming workshopgs will be featured on RDM Support's [trainings & workshops](https://www.uu.nl/en/research/research-data-management/training-workshops) page and the university's [Events](https://www.uu.nl/en/organisation/current-affairs/events) page, in addition to the UU Intranet and various (internal) newsletters. 

## Setup & Installation Requirements
Please work through the [Setup Vignette: Setting up your computer for WORCS](https://cjvanlissa.github.io/worcs/articles/setup.html) prior to the workshop. If you run into issues during setup and installation, you can contact your instructors to help resolve them.

## Schedule
This workshop will be given online. Participants will therefore do most exercises independently, using the step-by-step guides provided.
Instructors will be available for 1:1 support during these times, and reconvene in the main channel at stated times.

| Time | Activity |
|---:|:---|
| 9:00 | Walk-in, Tech Support |
| 10:00 | Introductions |
| 10:15 | Introduction to WORCS by Caspar van Lissa|
| 10:45 | Explanation of workshop program and setup |
| 11:00 | Phase 1: _Study Design_ |
| 11:45 | Recap & Questions |
| **12:00** | **Lunch Break** |
| 12:30 | Phase 2: _Writing & Analysis_ |
| 13:15 | Recap & Questions |
| 13:30 | Phase 3: _Submission & Publication_ |
| 14:15 | Recap & Questions |
| 14:30 | General Discussion |
| 15:00 | **End** |

## Data

You are encouraged to use your own data, code, and manuscript text during the workshop.  

If you do not have your own data, you can use [Allison Horst's Penguin dataset](https://github.com/allisonhorst/palmerpenguins).  
You can use this data by entering the following code in the `prepare_data.R` script:

``` r
install.packages("remotes")
remotes::install_github("allisonhorst/palmerpenguins")
data <- palmerpenguins::penguins
```
Alternatively, you can download one of these versions of the data, and load them yourself:
- An SPSS file ([penguins.sav](https://raw.githubusercontent.com/nehamoopen/workshop-worcs-pilot/main/data/penguins.sav))
- An Excel file ([penguins.xlsx](https://raw.githubusercontent.com/nehamoopen/workshop-worcs-pilot/main/data/penguins.xlsx))
- A CSV file ([penguins.csv](https://raw.githubusercontent.com/nehamoopenworkshop-worcs-pilot/main/data/penguins.csv))

## Workshop Program
Links to a step-by-step guide for each part of the workshop are provided below, taken from the [WORCS Workflow Vignette](https://cjvanlissa.github.io/worcs/articles/workflow.html).

| Subject | Link | Additional information |
|:--------|:-------|:------|
| Phase 1: Study Materials | [step-by-step guide](https://cjvanlissa.github.io/worcs/articles/workflow.html#phase-1-study-design) | - |
| Phase 2: Writing & Analysis | [step-by-step guide](https://cjvanlissa.github.io/worcs/articles/workflow.html#phase-2-writing-and-analysis) | [citing references in WORCS](https://cjvanlissa.github.io/worcs/articles/citation.html) |
| Phase 3: Submission & Publication | [step-by-step guide](https://cjvanlissa.github.io/worcs/articles/workflow.html#phase-3-submission-and-publication) | - |

If you're new to R Markdown, here's a handy [cheatsheet](https://www.rstudio.com/wp-content/uploads/2015/02/rmarkdown-cheatsheet.pdf)!

### Notes for cautious researchers

Some researchers might want to share their work only once the paper is accepted for publication. In this case, we recommend creating a "Private" GitHub repository in Step 1, and completing Steps 13-17 upon acceptance by the journal.

## Additional Resources

- This [paper in *Data Science*](https://doi.org/10.3233/DS-210031) introduces the WORCS workflow, explains the underlying tools, and illustrates how the `worcs` package can be used to create a new project that follows the workflow. You can cite WORCS, both the package and paper, using the citation below.

> Van Lissa, C. J., Brandmaier, A. M., Brinkman, L., Lamprecht, A.,
> Peikert, A., , Struiksma, M. E., & Vreede, B. (in press). WORCS: A
> Workflow for Open Reproducible Code in Science. Data Science, 2021.
> Data Science, vol. 4, no. 1, pp. 29-49. DOI: [10.3233/DS-210031](https://doi.org/10.3233/DS-210031).

- This [presentation](https://bvreede.github.io/worcshop/slides/overview_lecture.html) from an earlier workshop introduces WORCS and the concepts + tools its based on.

- Caspar van Lissa has recorded the following videos [introducing WORCS](https://www.youtube.com/watch?v=uKd6HoK_iS0) and [showing WORCS in action](https://www.youtube.com/watch?v=uzjpN_yFeUU). 

- The `worcs` [GitHub repo](https://github.com/cjvanlissa/worcs) & [package documentation](https://cjvanlissa.github.io/worcs/index.html)  

**Sample WORCS projects**  
For a list of sample `worcs` projects created by the `worcs` authors and other users, see the [`README.md` file on the WORCS GitHub page](https://github.com/cjvanlissa/worcs). This list is regularly updated.

- R Markdown [cheatsheet](https://www.rstudio.com/wp-content/uploads/2015/02/rmarkdown-cheatsheet.pdf)

## Acknowledgements

This workshop was developed by [Research Data Management Support](https://www.uu.nl/en/research/research-data-management) at Utrecht University, in collaboration with [Caspar van Lissa](https://github.com/cjvanlissa). The workshop documentation was written by [Neha Moopen](https://github.com/nehamoopen) and [Bianca Kramer](https://github.com/bmkramer), based on an [earlier workshop](https://bvreede.github.io/worcshop/) by [Barbara Vreede](https://github.com/bvreede).

**Image attribution**  
The [Git Logo](https://git-scm.com/) by Jason Long is licensed under the Creative Commons Attribution 3.0 Unported License. The [OSF logo](https://osf.io/) is licensed under CC0 1.0 Universal. Icons in the workflow graph are obtained from [Flaticon](https://www.flaticon.com); see [detailed attribution](https://github.com/cjvanlissa/worcs/blob/master/paper/workflow_graph/Attribution_for_images.txt).
