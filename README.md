All computations for this paper were performed in Excel

Appendix 4 (below and appended withing the paper) describes how to calculate 
the midpoint estimate and  the total margin of error (TME) under varying knowledge of
candidate preferences among nonrespondents.

We have also uploaded to this repository an Excel file that calculates the TME 
as depicted in Figure 1.
﻿
 
Appendix 4: Flowchart for Computation of TME
 
STEP 1: Determine P(z = 0)
STEP 2: Determine what is known about P(y = 1|z = 0), such as
·         Section 2.1: No knowledge.
·         Section 3.1: Predetermined bound. P(y = 1|z = 0) lies in an interval [λ0, λ1].
·         Section 3.2: Predetermined distance. δ0 ≤ P(y = 1|z = 0) − P(y = 1|z = 1) ≤ δ1.
STEP 3: Compute the midpoint of the identification interval estimate
·         Section 2.1: m∙P(z = 1) + ½P(z = 0)
·         Section 3.1: m∙P(z = 1) + ½(λ0 + λ1)P(z = 0)
·         Section 3.2: m + ½(δ0 + δ1)P(z = 0)
STEP 4: Compute the TME
·         Section 2.1: ½[P(z = 1)2/N + P(z = 0)2]½
·         Section 3.1: ½[P(z = 1)2/N + P(z = 0)2∙(λ1 − λ0)2]½
·         Section 3.2: ½[1/N + P(z = 0)2∙(δ1 − δ0)2]½











### Step 4

Author(s) submit a link to their GitHub repository as part of the [JASA
Reproducibility review process](https://jasa-acs.github.io/repro-guide/),
required upon submission of an invited revision.

### Step 5

JASA Associate Editors for Reproducibility will review the materials in
the GitHub repository of the authors and submit a
reproducibility review as part of the standard JASA review process.
Authors have the opportunity to respond to the review by making changes
and pushing their changes to their personal GitHub repository.

### Step 6

Once the manuscript is accepted, the materials in the author(s) personal
GitHub repository will be copied to the [JASA repository](https://github.com/jasa-acs).

## Reproducibility materials file structure

This template provides a suggested file structure for a JASA submission, but authors are free
to modify this structure.

The suggested components are as follows. Directories in the submission may have subdirectories to
further organize the materials.

1.  A `README.md` file - This file gives a short description of the
    paper and an overview of how to carry out the analyses presented in their manuscript.
2.  A `manuscript` directory - This directory will generally hold the source files
    (often LaTeX or Rmd) for the manuscript and any files directly related to the
    generation of the manuscript, including figure files.
3.  A `data` directory - This directory will generally hold the real data files 
    (or facsimile versions of them in place of confidential data) and simulated data files.
    See `data/README.md` for more details. 
4.  A `code` directory - This directory will generally hold 
    source code files that contain the core code to implement the method and various utility/auxiliary functions.
5.  An `output` directory - This directory will generally hold objects derived
    from computations, including results of simulations or real data analyses. See `output/README.md` for more details.

## Guidance on the use of reproducible environments

Submissions may include the use of reproducible environments capturing
state of a machine generating manuscript artifacts and even the
manuscript itself. Here we discuss two types of reproducible
environments and their use. Both virtual and package environments may be
put in the `code` directory.

### Package environments

Package environments capture the set of packages used by a programming
language needed to generate output. The R programming language has
`renv`, `switchr` and others to accomplish this, Python has `venv`,
`conda` and others, and Julia has native support (through the `Pkg`
package). When submitting these types of environments, the following are
suggested.

1.  Clearly indicate (in the overall `README.md`) the language(s) used (including version) 
    and the package environment tool used (e.g., `renv`, `conda`).
2.  Use a single package environment for all reproducible content.
3.  Prefer packages from package archives (CRAN, Bioconductor,
    RForge.net for example).
4.  If you use packages from a code repository (GitHub, GitLab, etc.)
    then use a release version if possible, or indicate the commit used. You could also consider
    forking the repository and providing a release.

### Virtual environments

Virtual environments such as Docker and Singlarity capture
the entire computing environment in which computations were performed.
In general, they are a more robust solution, capable of taking a
“snapshot” of a machine, including any system-level utilities and
external libraries needed to perform your computations. They have the
advantage that reproducing materials means running the virtual
environment, rather than recreating the programming language environment.
If using a virtual environment, we ask that 
you provide a definition file (e.g., a Dockerfile) or (perhaps better)
a link to an image in a standard online registry, such as DockerHub.

## References

Gentleman, Robert, and Duncan Temple Lang. “[Statistical Analyses and
Reproducible
Research](http://biostats.bepress.com/cgi/viewcontent.cgi?article=1001&context=bioconductor).”
(2004).

Gentleman, Robert. “[Reproducible research: a bioinformatics case
study](https://www.degruyter.com/document/doi/10.2202/1544-6115.1034/html).”
Statistical applications in genetics and molecular biology 4.1 (2005).

Marwick, Ben, and Bryan, Jennifer, and Attali, Dean, and Hollister,
Jeffrey W. [rrrpkg Github Page](https://github.com/ropensci/rrrpkg).
