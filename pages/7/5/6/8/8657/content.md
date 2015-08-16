
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--

# The adjoint triangle theorem
* automatic table of contents
{: toc}


## Statement ##

+-- {: .num_theorem #ATT}
###### Theorem
Suppose that $U:B\to C$ is a [[functor]] which has a [[left adjoint]] $F:C\to B$ with the property that the diagram
$$ F U F U \;\underoverset{\epsilon F U}{F U \epsilon}{\rightrightarrows}\; F U \xrightarrow{\epsilon} 1_B $$
is a [[coequalizer]].  Suppose that $A$ is a category with coequalizers of reflexive pairs; then a functor $R:A\to B$ has a left adjoint if and only if the composite $U R$ does.
=--
+-- {: .proof}
###### Proof
The direction "only if" is obvious since adjunctions compose.  For "if", let $F'$ be a left adjoint of $U R$, and define $L:B\to A$ to be the pointwise coequalizer of
$$ F' U F U \xrightarrow{F' U \epsilon} F' U $$
and
$$
  F' U F U \xrightarrow{F' U \theta U}
  F' U R F' U \xrightarrow{\epsilon' F' U}
  F' U
$$
where $\theta:F \to R F'$ is the [[mate]] of the equality $U R = U R$ under the adjunctions $F\dashv U$ and $F'\dashv U R$.  One then verifies that this works.
=--

+-- {: .num_remark #Monadic}
###### Remark
The hypotheses on $U$ are satisfied whenever it is [[monadic functor|monadic]].
=--

+-- {: .num_remark #RegMono}
###### Remark
In fact, it suffices to assume that each counit $\epsilon : F U b \to b$ is a [[regular epimorphism]], rather than it is the coequalizer of a specific given pair of maps.  See [(Street-Verity), Lemma 2.1](#StreetVerity).
=--

## Applications

The [[adjoint lifting theorem]] is a corollary.

## References ##

* [[Michael Barr]], [[Charles Wells]], _Toposes, Triples and Theories_ , Springer Heidelberg 1985. (Reprinted as [TAC reprint no.12](http://www.tac.mta.ca/tac/reprints/articles/12/tr12abs.html) (2005); section 3.7, pp.131ff) 

* [[Eduardo Dubuc]], _Adjoint triangles_, pp.69-81 in LNM **61** Springer Heidelberg 1968.

* [[John Power]], _A unified approach to the lifting of adjoints_ , Cah. Top. G&#233;om. Diff. Cat. **XXIX** no.1 (1988) pp.67-77. ([numdam](http://www.numdam.org/item?id=CTGDC_1988_29_1_67_0))

* [[Ross Street]], [[Dominic Verity]], _The comprehensive factorization and torsors_ , TAC **23** no.3 (2010) pp.42-75. ([abstract](http://www.tac.mta.ca/tac/volumes/23/3/23-03abs.html))
{#StreetVerity}

[[!redirects adjoint triangle]]
[[!redirects adjoint triangles]]
