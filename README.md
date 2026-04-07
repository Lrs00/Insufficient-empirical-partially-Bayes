# Insufficient empirical partially Bayes

This project studies empirical partially Bayes methods based on alternative summary statistics, with a focus on robust inference under small sample sizes and heterogeneous variances. In addition to the usual mean + SD pairing, the project explores median- and trimmed-based summaries, and learns the corresponding marginal likelihoods and conditional tail distributions needed for testing.

## Main idea

For each summary-statistic pairing, the project learns:

1. the marginal / likelihood distribution of the scale summary under a fixed sample size, and  
2. the conditional distribution of the location statistic given the scale summary.

These learned distributions are then used in simulation studies to compare methods in terms of power and false discovery rate.

## Files

- `learn 1.1`  
  Learns the likelihood / marginal distribution of the median absolute deviation about the median (MAD\_med).

- `learn 1.2`  
  Learns the conditional distribution associated with MAD\_med.

- `learn 1.3` and `learn 1.3.1`  
  Learn the likelihood / marginal distribution of the trimmed standard deviation.

- `learn 1.4` and `learn 1.4.1`  
  Learn the conditional distribution associated with the trimmed standard deviation.

- `simulation_final13`  
  Provides one example simulation study under a well-specified setting, where the prior on the variances is inverse-gamma.
  
- `sanity check4.15`  
  Sanity check for MAD\_mean-based p-values: analytic versus simulated results.
  
- `sanity check7.1,7.2,7.3`  
  Sanity check for global null.
## Current focus

The current simulations compare several summary-statistic pairings, including:

- mean + SD
- mean + MAD about the mean
- median + MAD about the median
- trimmed mean + trimmed SD

The overall goal is to understand when robust summaries may improve inference relative to the existing empirical partially Bayes approach.
