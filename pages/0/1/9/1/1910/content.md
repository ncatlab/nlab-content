
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--



\tableofcontents


## Idea 

The *Waldhausen $S_\bullet$-construction* is a procedure that produces [[algebraic K-theory]] (as an [[infinite loop space]] or [[connective spectrum]]) from a [[category]] or [[(infinity,1)-category|$(\infty,1)$-category]] equipped with a *Waldhausen structure*.

The construction can take as input any of the following kinds of data:

* [[Waldhausen category]]

* [[Waldhausen (infinity,1)-category|Waldhausen $(\infty,1)$-category]]

* [[stable (infinity,1)-category|stable $(\infty,1)$-category]]

* [[stable derivator]]


## Definition 

### For Waldhausen categories

Recall from the definition at *[[K-theory]]* that the K-theory [[spectrum]] $K(C)$ of an [[(∞,1)-category]] $C$ is the [[diagonal of a bisimplicial set|diagonal simplicial set]] on the [[bisimplicial set]] $Core\big(Func(\Delta^\bullet,C)\big)$ of [[sequences]] of [[morphisms]] in $C$ and [[equivalence in an (infinity,1)-category|equivalences]] between these (the [[core]] of the [[Segal space]] induced by $C$).

The *Waldhausen S-construction* mimics precisely this: for $C'$ a [[Waldhausen category]], define for $n \in \mathbb{N}$ the [[simplicial set]] $S_n C'$ to be the [[nerve]] of the category whose

* objects are sequences $0 \hookrightarrow A_{0,1} \hookrightarrow \cdots \hookrightarrow A_{0,n}$ of Waldhausen cofibrations;

  * together with choices of quotients $A_{i j} = A_{0, j}/ A_{0,i}$, i.e.  cofibration sequences $A_{0,i} \to A_{0,j} \to A_{i j}$

* morphisms are collections of morphisms $\{A_{i,j} \to B_{i,j}\}$ that commute with all diagrams in sight. 

Then one finds that the [[nerve and realization|realization]] of the [[bisimplicial set]] $S_\bullet C'$ with respect to one variable is itself naturally a [[topologically enriched category|topological]] [[Waldhausen category]]. Therefore the above construction can be repeated to yield a sequence of topological categories $S^{(n)}_\bullet C'$. The corresponding sequence of thick [[geometric realization|topological realization]]s is a [[spectrum]]

$$
  \mathbf{K}(C)_n 
    = 
  \left\vert S^{(n)}_\bullet C' \right\vert
$$

this is the **S-construction** of the  **Waldhausen K-theory spectrum** of $C'$.

(... roughly at least, need to polish this, see link below meanwhile...)


## Related

* [[algebraic K-theory]]

* [[Quillen Q-construction]]

* [[K-theory of a stable (infinity,1)-category|K-theory of a stable $(\infty,1)$-category]]

* [[categorified Dold-Kan correspondence]]



## References ##

### For Waldhausen categories

* {#Waldhausen85} [[Friedhelm Waldhausen]]: *Algebraic K-theory of spaces*, in: *Algebraic and Geometric Topology* (Proceedings of a conference at Rutgers, New Brunswick, N. J., 1983), Lecture Notes in Math. **1126**, Springer (1985) 318-419 &lbrack;[doi:10.1007/BFb0074449](https://doi.org/10.1007/BFb0074449), [pdf](https://www.maths.ed.ac.uk/~v1ranick/surgery/rutgers/wald.pdf), [pdf](http://www.math.uni-bielefeld.de/~fw/LNM1126_318-419.pdf)&rbrack;

The Waldhausen S-construction is recalled in:

* {#ThomasonTrobaugh90} [[R. W. Thomason]], Thomas Trobaugh; section 1 of:  _Higher algebraic K-theory of schemes and of derived categories_ in: _The Grothendieck Festschrift_, Modern Birkhäuser Classics **88** (1990) 247--435 &lbrack;[doi:10.1007/978-0-8176-4576-2_10](https://doi.org/10.1007/978-0-8176-4576-2_10), [pdf](https://webhomes.maths.ed.ac.uk/~v1ranick/papers/tt.pdf)&rbrack;


### For Waldhausen $(\infty,1)$-categories and stable $(\infty,1)$-categories

* [[Clark Barwick]]: _On the algebraic K-theory of higher categories_, Journal of Topology **9** (2016) 245--347 &lbrack;[arXiv:1204.3607](http://arxiv.org/abs/1204.3607), [doi:10.1112/jtopol/jtv042](http://doi.org/10.1112/jtopol/jtv042)&rbrack;

* [[Andrew J. Blumberg]], [[David Gepner]], [[Goncalo Tabuada]]: _A universal characterization of higher algebraic K-theory_, Geom. Topol. **17** (2013) 733--838 &lbrack;[arXiv:1001.2282](http://arxiv.org/abs/1001.2282), [doi:10.2140/gt.2013.17.733](https://doi.org/10.2140/gt.2013.17.733)&rbrack;

### Other

A combinatorial construction of symmetries with the S-construction as a special case:

* [[David Nadler]]: _Cyclic symmetries of $A_n$-quiver representations_, Advances in Mathematics **269** (2015) 346--363 &lbrack;[arxiv/1306.0070](http://arxiv.org/abs/1306.0070), [doi:10.1016/j.aim.2014.10.006](https://doi.org/10.1016/j.aim.2014.10.006)&rbrack;
  > "This short note contains a combinatorial construction of symmetries arising in [[symplectic geometry]] (partially wrapped or infinitesimal [[Fukaya categories]]), algebraic geometry (derived categories of singularities), and K-theory (Waldhausen's S-construction). Our specific motivation (in the spirit of expectations of Kontsevich, and to be taken up in general elsewhere) is a combinatorial construction of quantizations of Lagrangian skeleta (equivalent to microlocal sheaves in their many guises). We explain here the one dimensional case of ribbon graphs where the main result of this paper gives an immediate solution."

Interpretation in terms of a [[categorified Dold-Kan correspondence]]:

* {#Dyckerhoff17} [[Tobias Dyckerhoff]]: _A categorified Dold-Kan correspondence_,  Sel. Math. New Ser. **27** 14 (2021)   &lbrack;[arXiv:1710.08356](https://arxiv.org/abs/1710.08356), [doi:10.1007/s00029-021-00618-5](https://doi.org/10.1007/s00029-021-00618-5)&rbrack;


