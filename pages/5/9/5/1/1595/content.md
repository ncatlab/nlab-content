+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Statement

The **Freudenthal suspension theorem** ([Freudenthal 37](#Freudenthal37)) is the following theorem about [[homotopy groups]] of [[n-spheres]]:

The [[suspension]] homomorphism $\sigma :\pi_{n+k}(S^n)\to \pi_{n+k+l}(S^{n+l})$ is an [[isomorphism]] for $n\gt k+1$. 

In this statement, one can replace $S^n$ with any $(n-1)$-[[connected space]] $Y$ while replacing $S^{n+l}$ with the corresponding suspension $\Sigma^{l} Y$.

The Freudenthal suspension theorem is a special case of the [[Blakers-Massey theorem]].


The Freudenthal suspension theorem motivated introducing the [[stable homotopy groups of spheres]] $\pi_k(S):=\pi_{n+k}(S^n)$, more generally the [[stable homotopy groups]] $\pi_k^S(Y) = \pi_{n+k}(\Sigma^n Y)$, both independent of $n$ where $n\gt k+1$, and still more generally the [[Spanier-Whitehead category]], then the [[stable homotopy category]] and eventually the [[stable (infinity,1)-category of spectra]].


## Related concepts

* [[suspension isomorphism]]

## References

Due to 

* {#Freudenthal37} [[Hans Freudenthal]],  _&#220;ber die Klassen der Sph&#228;renabbildungen_, Compositio Math., 5:299-314, 1937.

A standard textbook account is in

* [[Alan Hatcher]], _[Algebraic Topology](http://www.math.cornell.edu/~hatcher/AT/ATpage.html)_, chapter 4 ([pdf](http://www.math.cornell.edu/~hatcher/AT/ATch4.pdf))

A nice expanded version of the statements there is in

* Tengren Zhang, _Freudenthal suspension theorem_  ([pdf](http://www.math.uchicago.edu/~may/VIGRE/VIGRE2009/REUPapers/ZhangTengren.pdf))


A formalization in [[homotopy type theory]] in [[Agda]] is in 

* [[Peter Lumsdaine]], [[Dan Licata]], _[Freudenthal.agda](https://github.com/dlicata335/hott-agda/blob/master/homotopy/Freudenthal.agda)_

Discussion in [[equivariant homotopy theory]] includes

* {#GreenleesMay} [[John Greenlees]], [[Peter May]], p. 7,8 of _Equivariant stable homotopy theory_ ([pdf](http://www.math.uchicago.edu/~may/PAPERS/Newthird.pdf))




