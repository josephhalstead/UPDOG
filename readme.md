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

Coming Soon

#### Statistics

Coming Soon

## Install
```
pip install pyupdog
```
## Run

```

UPDog.py --vcf test_data/200518_A00748_0027_AHLKFCDRXX.vcf.gz \
--proband_id test_sample \
--ped test_data/200518_A00748_0027_AHLKFCDRXX.ped \
--output results/200518_A00748_0027_AHLKFCDRXX \
--min_dp 25 \
--min_gq 15 \
--min_qual 20 \
--p_value 0.001 \
--block_size 1000000 \
--min_variants_per_block 100 \
--min_blocks 2 \
--min_proportion 0.01


```
## Analyse Output

Coming Soon

## References

[1] https://en.wikipedia.org/wiki/Uniparental_disomy
[2] UPDio https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3975066/

