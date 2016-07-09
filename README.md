# RiVIERA (beta)
<u>Ri</u>sk <u>V</u>ariant <u>I</u>nference using <u>E</u>pigenomic <u>R</u>eference <u>A</u>nnotation

## Description
RiVIERA (beta) is a novel Bayesian framework to jointly model the likelihood of GWAS p-values via beta density function across multiple related disorders using large-scale reference epigenomic annotations. Briefly, the inputs to RiVIERA are: (1) GWAS associations p-values: one or more sets of p-values from multiple GWAS; (2) epigenomic reference annotations: binary or continuous annotations (or ``genome browser tracks") for each SNP that reflect their epigenomic context (i.e., histone marks, DNase I hypersensitivity, transcription factor binding, etc) in various tissues or cell lines. The goal of RiVIERA is to infer for each SNP in disease their posterior probability of disease association (PPA) using epigenomic values and to detect functional enrichments from the annotations, taking into account the underlying multi-trait epigenomic covariance.

#### Input
1. GWAS summary association statistics in one or more traits (p-values)
2. Functional annotation matrix (binary or continuous) for each SNP

#### Important features
1. Efficient full Bayesian inference of causal SNP and causal annotations allows incorporation of large number of annotations
2. Can model epigenomic covariance of multiple related traits (model complexity is linear to the number of traits)

## Installation
RiVIERA (beta) requires Rcpp and RcppArmadillo, which can be easily installed within R via 'install.packages' function.

Download, build and install:

`$ git clone https://github.mit.edu/liyue/rivieraBeta`

`$ R CMD build rivieraBeta`

`$ R CMD INSTALL RiVIERAbeta_0.9.1.tar.gz`

## Documentation
Function manuals are described in R documents:

`> library(RiVIERAbeta)`

`> ?RiVIERAbeta`

User manual with examples is written in sweave and invoked by vignette:

`> vignette(RiVIERAbeta)`

