# analytic-combinatorics

A Clojure library designed to solve problems in Analytic Combanitorics.

## Experiments

- Program I.1 Determine the choice of four coins that maximizes the number of ways to change a dollar.
- Program I.2 Write programs that estimate the rate of growth of the Cayley numbers and the partition numbers (Hn/Hn−1 and Pn/Pn−1).
- Program II.1 Write a program to simulate the Ehrenfest mode (see Note II.11) and use it to plot the distribution of the number of balls in urn A after 103, 104 and 105 steps when starting with 103 balls in urn A and none in urn B.
- Program III.1 Write a program that generates 1000 random permutations of size N for N = 103, 104, ... (going as far as you can) and plots the distribution of the number of cycles, validating that the mean is concentrated at HN.
- Program IV.1 Compute the percentage of permutations having no singelton or doubleton cycles and compare with the asymptotic estimate from analytic combinatorics, for N = 10 and N = 20 .
- Program IV.2 Plot the derivative of the supernecklace GF (see Note IV.28) in the style of the plots in Lecture 4. Click here for access to the Java code in the lecture.
- Program V.1 In the style of the plots in the Lecture 6, plot the GFs for the set of bitstrings having no occurrence of the pattern 0000000001. Do the same for 0101010101. (See Web Exercise V.1 and Program IV.2).
- Program VI.1 In the style of the plots in Lecture 6, do r- and θ-plots of 1/Γ(z) in the unit square  of size 10 centered at the origin (see Program IV.2)
- Program VII.1 Do r- and θ-plots of the GF for bracketings (see Web Exercise VII.1).

## Exercises

### Week 1

- Alice, Bob, and coding bounds. Alice wants to communicate n bits of information to Bob over a channel (a wire, an optic fibre) that transmits 0,1-bits but is such that any occurrence of 11 terminates the transmission. Thus, she can only send on the channel an encoded version of her message (where the code is of some length ℓ≥n) that does not contain the pattern 11.
- Fast determination of the Cayley-Polya numbers. Logarithmic differentiation of H(z) provides for the Hn a recurrence by which one computes Hn in time polynomial in n. (Note: a similar technique applies to the partition numbers Pn.)

### Week 2

#### Problem 1

- Consider a system of two chambers A and B (also classically called "urns"). There are N distinguishable balls, and, initially, chamber A contains them all. At any instant 12,32,…, one ball is allowed to change from one chamber to the other. Let E[ℓ]n be the number of possible evolutions that lead to chamber A containing ℓ balls at instant n and E[ℓ](z) the corresponding EGF.
- Then: E[ℓ](z)=(Nℓ)(coshz)ℓ(sinhz)N−ℓ,E[N](z)=(coshz)N≡2−N(ez+e−z)N.
- [Hint: the EGF E[N] enumerates mappings where each pre-image has an even cardinality.] In particular, the probability that urn A is again full at time 2n is:
- (1/2^N*N^2n) * ∑(k=0..N),((N_K)(N-2k)^2n)
- This famous model was introduced by Paul and Tatiana Ehrenfest in1907, as a simplified model of heat transfer. It helped resolve the apparent contradiction between irreversibility in thermodynamics (the case N→∞) and recurrence of systems undergoing ergodic transformations (the case N<∞).

#### Problem 2

- Combinatorics of trigonometrics. Interpret tanz1−z, tantanz, and tan(ez−1) as EGFs of combinatorial classes.

#### Problem 3

- Leaves and node-degree profile in Cayley trees. For Cayley trees, the bivariate EGF with u marking the number of leaves is the solution to
- T(z,u)=uz+z(eT(z,u)−1)
- By Lagrange inversion, the distribution is expressible in terms of Stirling partition numbers.) The mean number of leaves in a random Cayley tree is asymptotic to ne−1. More generally, the mean number of nodes of outdegree k in a random Cayley tree of size~n is asymptotic to:
- n * e^-1 * (1/k!)
- Degrees are thus approximately described by a Poisson law of rate 1.

#### Problem 4

- After Bhaskara Acharya (circa 1150 AD). Consider all the numbers formed in decimal with digit 1 used once, with digit 2 used twice, ..., with digit 9 used nine times. Such numbers all have 45 digits. Compute their sum $S$ and discover, much to your amazement that $S$ equals 45875559600006153219084769286399999999999999954124440399993846780915230713600000. This number has a long run of nines (and further nines are hidden!). Is there a simple explanation? This exercise is inspired by the Indian mathematician Bhaskara Acharya who discovered multinomial coefficients near 1150 AD.

### Week 3

- A "supernecklace" of the 3rd type is a labelled cycle of cycles (see page 125). Draw all the supernecklaces of the 3rd type of size n for n = 1, 2, 3, and 4. Then develop an asymptotic estimate of the number of supernecklaces of size n by showing that
- [z^n] ln(1/(1 - ln(1/1-z))) ~ (1/n)(1-e^-1)^-n

### Week 4

#### Problem 1

- Give an asymptotic expression for the number of strings that do not contain the pattern 0000000001. Do the same for 0101010101.

#### Problem 2

- Give asymptotic expressions for the number of objects of size N and the number of parts in a random object of size N for the following classes: compositions of 1s, 2s, and 3s, triple surjections, and alignments with no singleton cycles.

### Week 5

#### Problem 1

- Use the standard function scale to directly derive an asymptotic expression for the number of strings in this following CFG: S = E + U×Z×S + D×Z×S, U = Z + U×U×Z, D = Z + D×D×Z.

#### Problem 2

- Give an asymptotic expression for the number of rooted ordered trees for which every node has 0, 2, or 3 children. How many bits are necessary to represent such a tree?

#### Problem 3

- Use the tree-like schema to develop an asymptotic expression for the number of bracketings with $N$ leaves (see Example I.15 on page 69 and Note VII.19 on page 474)

### Week 6


### License

Copyright © 2014 FIXME

Distributed under the Eclipse Public License either version 1.0 or (at
your option) any later version.
