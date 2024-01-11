+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

What may be called *nonabelian differential cohomology* -- in combination of *[[nonabelian cohomology]]* and *[[differential cohomology]]* -- is a notion of [[connections on infinity-bundles|connections on higher bundles]] with [[higher group|higher]] [[gauge group]] being a possibly non-[[abelian infinity-group|abelian]] [[n-group]].

Early motivation was the observation ([SSS12](#SatiSchreiberStasheff12)) that with the [[Green-Schwarz mechanism]] imposed, the [[B-field]] in [[heterotic string theory]] combines with the ordinary non-abelian [[gauge field]] into a non-abelian higher connection (a [[twisted differential string structure]]), and analogously so after lifting the situation to the [[C-field]] in [[Hořava-Witten theory]] ([FSS15](#FSS15)).

Later, the desire to more accurately model more of the expected subtle topological properties of the [[C-field]] (such as the [[shifted C-field flux quantization]] combined with [[Page charge]]-quantization) led to the hypothesis ("[[schreiber:Hypothesis H]]") that it ought to be [[flux quantization|flux quantized]] in unstable [[differential Cohomotopy|differential]] 4-[[Cohomotopy]], hence with [[homotopy type]] of its higher gauge group being the [[loop group|loop]] [[infinity-group|$\infty$-group]] of the 4-sphere. This [[schreiber:Hypothesis H]] turns out to subtly reproduce the [[Green-Schwarz mechanism]] in its lift to [[Hořava-Witten theory]] ([FSS22](#FSS22)) and also that on [[M5-branes]] ([SS20](#SS20), [FSS21](string+structure#FSS21)).

Generally, one may understand [[differential cohomology|differential]] [[nonabelian cohomology]] as modelling [[flux quantization|flux quantized]] [[higher gauge theory|higher gauge fields]] ([SS23](#SS23)). 

For example, also the "Hypothesis K" of [[D-brane charge quantization in topological K-theory]] is, at face value, a [[flux quantization]] (of the [[RR-field]] combined with the [[B-field]]) in a non-abelian differential cohomology (see the overview [here](/schreiber/show/Introduction+to+Hypothesis+H#OverviewLogicOfFluxQuantization)) which however may be and commonly is regarded as *twisted abelian* namely as [[twisted differential K-theory]], by regarding the [[B-field]] as a "[[background field]]" and considering the [[RR-field]] in its dependence.

## Related concepts

* [[nonabelian cohomology]]

* [[differential cohomology]]

* [[higher gauge theory]]

## References

### Via higher Cartan connections from (adjusted) Weil algebras

Early explorative notes:

* [[Urs Schreiber]], _On nonabelian differential cohomology_, March 17, 2008, [Slides](https://www.math.uni-hamburg.de/home/schreiber/diffcohslides.pdf).

The local structure of [[L-infinity algebra valued differential forms|$L_\infty$-algebra valued differential forms]], via [[dg-algebra]] [[homomorphisms]] out of ("[[adjusted Weil algebra|adjusted]]") [[Weil algebras]] in the [[de Rham complex]] of the base manifold:

* [[Hisham Sati]], [[Urs Schreiber]], [[Jim Stasheff]], example 5 in section 6.5.1, p. 54 of _[[schreiber:L-infinity algebra connections|$L_\infty$ algebra connections and applications to String- and Chern-Simons n-transport]]_, in: *Quantum Field Theory*, Birkh&#228;user (2009) 303-424 \[<a href="http://arxiv.org/abs/0801.3480">doi:0801.3480</a>, [doi:10.1007/978-3-7643-8736-5_17](https://doi.org/10.1007/978-3-7643-8736-5_17)\]

The [[Lie integration]] of this local structure to globally possibly nontrivial actual [[connections on infinity-bundles|connections on higher bundles]]:

* [[Domenico Fiorenza]], [[Urs Schreiber]], [[Jim Stasheff]], _Čech cocycles for differential characteristic classes_, Advances in Theoretical and Mathematical Physics 16:1 (2012), 149–250, [arXiv:1011.4735](http://arxiv.org/abs/1011.4735), [doi:10.1007/BF02104916](https://doi.org/10.1007/BF02104916).

For the application of this construction to modelling the [[Green-Schwarz mechanism]] see [below](#HigherGaugeTheoryOfTheGreenSchwarzMechanismReferences).


### Via the nonabelian character map

A more axiomatic formulation of [[differential cohomology|differential]] [[non-abelian cohomology]] (not yet proven to subsume the above construction) in non-abelian generalization of the original [Hopkins-Singer construction](differential}cohomology#HopSin) of abelian (namely [[Whitehead-generalized cohomology]]) [[differential cohomology]], now using a nonabelian generalization of the [[Chern-Dold character map]]:

* [[Domenico Fiorenza]], [[Urs Schreiber]], [[Hisham Sati]], Def. 9.3 ([p. 161](/schreiber/files/NonabelianCharacterWS231212.pdf#page=171)) in: *[[schreiber:The Character Map in Non-Abelian Cohomology]]*, World Scientific (2023) &lbrack;[doi:10.1142/13422](https://doi.org/10.1142/13422)&rbrack;

On how this generally serves to reflect [[flux quantization]] in [[higher gauge theories]]:

* {#SS23} [[Hisham Sati]], [[Urs Schreiber]], *[[schreiber:Flux Quantization on Phase Space]]* &lbrack;[arXiv:2312.12517](https://arxiv.org/abs/2312.12517)&rbrack;

reviewed in:

* [[Hisham Sati]], [[Urs Schreiber]], *[[schreiber:Introduction to Hypothesis H]]* ([here](/schreiber/show/Introduction+to+Hypothesis+H#OverviewFluxQuantizationViaNonabDiffCohomology))


### Differential cohomotopy for the 11d SuGra C-field

The example of unstable (and as such non-abelian) [[differential Cohomotopy]] (in the context of modeling the [[supergravity C-field]] via [[schreiber:Hypothesis H]]):

* [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], §4 in: *[[schreiber:The WZW term of the M5-brane and differential cohomotopy]]*, J. Math. Phys. **56** 102301 (2015) &lbrack;[arXiv:1506.07557](https://arxiv.org/abs/1506.07557), [doi:10.1063/1.4932618](https://doi.org/10.1063/1.4932618)&rbrack;

* [[Daniel Grady]], [[Hisham Sati]], Def. 3.2 in: *Differential cohomotopy versus differential cohomology for M-theory and differential lifts of Postnikov towers*, Journal of Geometry and Physics **165** (2021) 104203 &lbrack;[arXiv:2001.07640](https://arxiv.org/abs/2001.07640), [doi:10.1016/j.geomphys.2021.104203](https://doi.org/10.1016/j.geomphys.2021.104203)&rbrack;

* {#FSS20} [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], Ex. 9.3 in: _[[schreiber:The Character Map in Twisted Non-Abelian Cohomology|The Character Map in Nonabelian Cohomology --- Twisted, Differential, Generalized]]_, World Scientific (2023) &lbrack;[arXiv:2009.11909](https://arxiv.org/abs/2009.11909), [doi:10.1142/13422](https://doi.org/10.1142/13422)&rbrack;


[[!include higher gauge theory of the Green-Schwarz mechanism -- references]]


[[!redirects non-abelian differential cohomology]]
[[!redirects differential nonabelian cohomology]]
[[!redirects differential non-abelian cohomology]]
