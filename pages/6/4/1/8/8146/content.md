
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Diagram chasing lemmas
+-- {: .hide}
[[!include diagram chasing lemmas - contents]]
=--
#### Homological algebra
+-- {: .hide}
[[!include homological algebra - contents]]
=--
=--
=--
#Contents#
* table of contents
{:toc}

## Idea

The _$3 \times 3$-lemma_ or _nine lemma_ is one of the basic [[diagram chasing lemmas]] in [[homological algebra]].

## Statement

+-- {: .num_lemma}
###### Lemma

Let 

$$
  0 \to A_\bullet \to B_\bullet \to C_\bullet \to 0
$$

be a [[short exact sequence]] of [[chain complexes]]. Then 
if two of the three complexes $A_\bullet, B_\bullet, C_\bullet$
are [[long exact sequence|exact]], so is the remaining third.

=--

+-- {: .num_lemma}
###### Lemma

Let 

$$
  \array{   
     && 0 && 0 && 0 &&
     \\
     && \downarrow && \downarrow && \downarrow && 
     \\
     0 &\to& A' &\to& B' &\to& C' &\to& 0
     \\
     && \downarrow && \downarrow && \downarrow && 
     \\
     0 &\to& A &\to& B &\to& C &\to& 0
     \\
     && \downarrow && \downarrow && \downarrow && 
     \\
     0 &\to& A'' &\to& B'' &\to& C'' &\to& 0
     \\
     && \downarrow && \downarrow && \downarrow && 
     \\
     && 0 && 0 && 0 &&
  }
$$

be a [[commuting diagram]] in some [[abelian category]] such that each of the three columns is an [[exact sequence]].  Then

1. If the two bottom rows are exact, then so is the top.

1. If the top two rows are exact, then so is the bottom.

1. If the top and bottom rows are exact _and_ $A \to C$ is the [[zero morphism]], then also the middle row is exact.

=--

A proof by way of the [[salamander lemma]] is spelled out in detail at _[Salamander lemma - Implications - 3x3 lemma](http://ncatlab.org/nlab/show/salamander+lemma#3x3Lemmas)_.

## Related concepts

* [[salamander lemma]]

* [[snake lemma]], [[5-lemma]]

* [[horseshoe lemma]]

## References

### In abelian categories

An early appearance of the $3 \times 3$-lemma is as lemma (5.5) in 


* D. A. Buchsbaum, _Exact categories and duality_, Transactions of the American Mathematical Society Vol. 80, No. 1 (1955), pp. 1-34 ([JSTOR](http://www.jstor.org/stable/1993003))

In 

* [[Charles Weibel]], _[[An introduction to homological algebra]]_

it appears as exercise 1.3.2.

The sharp $3 \times 3$-lemma appears as lemma 2 in 

* Temple Fay, [[Keith Hardie]], [[Peter Hilton]], _The two-square lemma_, Publicacions Matem&#224;tiques, Vol 33 (1989) ([pdf](http://dmle.cindoc.csic.es/pdf/PUBLICACIONSMATEMATIQUES_1989_33_01_10.pdf))

Also lemma 3.2-3.4 of

* [[Saunders MacLane]], _Homology_, Grundlehren der math. Wissenshaften vol 114, Springer (1995)

### In non-abelian categories

Discussion of generalization to non-abelian categories is in 

* Marino Gran, Diana Rodelo, _Goursat categories and the $3 \times 3$-lemma_, Applied Categorical Structures, Vol. 20, No 3, 2012, 229-238. ([journal](http://www.google.com/url?q=http%3A%2F%2Flink.springer.com%2Farticle%2F10.1007%252Fs10485-010-9236-x&sa=D&sntz=1&usg=AFQjCNG1kEggBxeeDfQlkWOa4ShUo8vwLA), [pdf slides](http://ct2010.disi.unige.it/slides/Rodelo_CT2010.pdf))

* Marino Gran, Zurab Janelidze and Diana Rodelo, _$3 \times 3$ lemma for star-exact sequences_, Homology, Homotopy and Applications, Vol. 14 (2012), No. 2, pp.1-22. ([journal](http://www.intlpress.com/HHA/v14/n2/a1/))

* [[Dominique Bourn]], _$3 \times 3$-lemma and protomodularity_, Journal of Algebra, Volume 236, Number 2, 15 February 2001 , pp. 778-795(18)

* [[Dominique Bourn]], _The denormalized $3 \times 3$ lemma_, Journal of Pure and Applied Algebra, Volume 177, Issue 2, 24 January 2003, Pages 113-129, doi:[10.1016/S0022-4049(02)00143-3](https://doi.org/10.1016/S0022-4049%2802%2900143-3)


[[!redirects nine lemma]]
[[!redirects 9 lemma]]
[[!redirects 3x3-lemma]]

[[!redirects sharp 3x3 lemma]]

