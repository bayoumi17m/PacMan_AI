# Ghostbusters

</br>
<p align="center">
<img src="/tracking/imgs/busters.png" alt="GB" width="400px"/>
</p>
</br>

The blocks of color indicate where the each ghost could possibly be, given the
noisy distance readings provided to Pacman. The noisy distances at the bottom
of the display are always non-negative, and always within 7 of the true
distance. The probability of a distance reading decreases exponentially
with its difference from the true distance.

## Goal
Our goal for this project is to implement inference to track the ghost. Bayes'
Nets provide us with powerful tools for making the most of the information
we have. Throughout the rest of this project, I will implement algorithms for
performing both exact and approximate inference using Bayes' Nets.

## Parts of Project to be Done:

**Exact Inference**
- [x] Exact Inference Observation
- [x] Exact Inference with Time Elapse
- [x] Exact Inference Full Test

**Particle Filter Inference**
- [x] Approximate Inference Observation
- [x] Approximate Inference with Time Elapse

**Joint Particle Filter (Marginal) Inference**
- [x] Joint Particle Filter Observation
- [x] Joint Particle Filter with Elapse Time

## Problems
It seems that there is a problem with the running of MarginalInference which may
be due to a lack of computing resources since it does take a large amount of
memory.
