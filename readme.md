# UniParental Disomy triO investiGator (UPDOG)

## What's UPDOG?

UniParental Disomy (UPD) is genetic phenomenon where an individual inherits two copies of a chromosome from a single parent and none from the other. UPD can take the form of heterodisomy where the child inherits non identical chromosomes from one parent, or isodisomy where the child inherits a duplicate chromosome from a parent [1].

UPDOG is a Python tool to find and plot UPD events in Next Generation Sequencing (NGS) Whole Genome Sequencing trio data. Given a VCF containing a sample and the sample's two parents the tool will produce and plot a set of metics for each chromosome. The user can then examine these plots for signs of UPD events. Alternatively, the tool produces a CSV file containing the statistically significant UPD events.


### Principle

1) Examine each chromosome in segments e.g. 1MB and calculate the proportion of mendellian errors in each segment.
2) Calculate the expected number of mendellian errors (Mean over all chromosomes).
3) For each segment in step 1 measure whether each segment has a statistically significant increase in each type of mendelian error.
4) Merge contiguous statistically significant segments together.
5) Apply hard filters to the UPD calls and report to user.

#### Mendellian Errors

Each UPD event produces signature mendellian errors in trio genotypes [2]

Paternal 

#### Statistics

## Install

## Run

## Analyse Output

## References

[1] https://en.wikipedia.org/wiki/Uniparental_disomy
[2] UPDio https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3975066/
[3] UPDtool

