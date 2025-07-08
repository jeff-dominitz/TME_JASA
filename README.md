The data studied in this paper are publicly available online on the website of the New York Times at
https://www.nytimes.com/interactive/2024/07/03/us/elections/times-siena-poll-registered-voter-crosstabs.html?smid=nytcore-ios-share&referringSource=articleShare&sgrp=c-cb


The calculations in the Illustration and in its Extensions 1-4 were performed by hand. Specifics are reported in the paper.

Computations for The graphical illustration in Figure 1 were performed in Excel. See the file TME graph.xlsx in this repository.


Appendix 4 (below and appended within the paper) describes how to calculate the midpoint estimate and  the total margin of error (TME) under varying knowledge of candidate preferences among nonrespondents.
 
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

