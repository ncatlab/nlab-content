
#Contents#
* table of contents
{:toc}

## Idea ##

The Waldhausen $S_\bullet$-construction is a procedure that produces [[algebraic K-theory]] (as an [[infinite loop space]] or [[connective spectrum]]) from a category or [[(infinity,1)-category]] equipped with a [[Waldhausen structure]].

The construction can take as input any of the following:

* [[Waldhausen category]]
* [[Waldhausen (infinity,1)-category]]
* [[stable (infinity,1)-category]]
* [[stable derivator]]
* ...

## Definition ##

### For Waldhausen categories

Recall from the definition at [[K-theory]] that the K-theory spectrum $K(C)$ of the [[(∞,1)-category]] $C$ is the diagonal simplicial set on the [[bisimplicial set]] $Core(Func(\Delta^n,C))$ of sequences of morphisms in $C$ and equivalences between these (the [[core]] of the [[Segal space]] induced by $C$).

The Waldhausen S-construction mimics precisely this: for $C'$ a [[Waldhausen category]] for every integer $n$ define a simplicial set $S_n C'$ to be the [[nerve]] of the category whose

* objects are sequences $0 \hookrightarrow A_{0,1} \hookrightarrow \cdots \hookrightarrow A_{0,n}$ of Waldhausen cofibrations;


  * together with choices of quotients $A_{i j} = A_{0, j}/ A_{0,i}$, i.e.  cofibration sequences $A_{0,i} \to A_{0,j} \to A_{i j}$

* morphisms are collections of morphisms $\{A_{i,j} \to B_{i,j}\}$ that commute with all diagrams in sight. 

Then one finds that the [[nerve and realization|realization]] of the bisimplicial set $S_\bullet C'$ with respect to one variable is itself naturally a topological [[Waldhausen category]]. Therefore the above construction can be repeated to yield a sequence of topological categories $S^{(n)}_\bullet C'$. The corresponding sequence of thick [[geometric realization|topological realization]]s is a [[spectrum]]

$$
  \mathbf{K}(C)_n = |S^{(n)}_\bullet C'|
$$

this is the **S-construction** of the  **Waldhausen [[K-theory]] spectrum** of $C'$.

(... roughly at least, need to polish this, see link below meanwhile...)

## Related

* [[algebraic K-theory]]
* [[Quillen Q-construction]]
* [[K-theory of a stable (infinity,1)-category]]
* [[K-theory of a Waldhausen (infinity,1)-category]]

* [[categorified Dold-Kan correspondence]]

## References ##

### For Waldhausen categories

* {#Waldhausen85} [[F. Waldhausen]], _Algebraic K-theory of spaces_, Alg. and Geo. Top., Springer Lect. Notes Math. 1126 (1985), 318-419, [pdf](http://www.maths.ed.ac.uk/~aar/surgery/rutgers/wald.pdf).

The Waldhausen S-construction is recalled for instance in section 1 of 

* {#ThomasonTrobaugh90} [[R. W. Thomason]], Thomas Trobaugh, _Higher algebraic K-theory of schemes and of derived categories_, _The Grothendieck Festschrift_, 1990, 247-435.

or in section 1 of

* Paul D. Mitchener, _Symmetric Waldhausen K-theory spectra of topological categories_ ([pdf](http://bib.mathematics.dk/unzip.php?filename=DMF-2001-05-001-v1.pdf.gz))

### For Waldhausen (infinity,1)-categories and stable (infinity,1)-categories

* [[C. Barwick]], _On the algebraic K-theory of higher categories_, [arXiv:1204.3607](http://arxiv.org/abs/1204.3607).

* [[Andrew J. Blumberg]], [[David Gepner]], [[Goncalo Tabuada]], _A universal characterization of higher algebraic K-theory_, [arXiv:1001.2282](http://arxiv.org/abs/1001.2282v4).

### Other

A combinatorial construction of symmetries due to Nadler has a relation to the S-construction in a special case:

* [[David Nadler]], _Cyclic symmetries of $A_n$-quiver representations_, [arxiv/1306.0070](http://arxiv.org/abs/1306.0070)

> This short note contains a combinatorial construction of symmetries arising in symplectic geometry (partially wrapped or infinitesimal Fukaya categories), algebraic geometry (derived categories of singularities), and K-theory (Waldhausen's S-construction). Our specific motivation (in the spirit of expectations of Kontsevich, and to be taken up in general elsewhere) is a combinatorial construction of quantizations of Lagrangian skeleta (equivalent to microlocal sheaves in their many guises). We explain here the one dimensional case of ribbon graphs where the main result of this paper gives an immediate solution. 

Interpretation in terms of a [[categorified Dold-Kan correspondence]] is discussed in

* {#Dyckerhoff17} [[Tobias Dyckerhoff]], _A categorified Dold-Kan correspondence_ ([arXiv:1710.08356](https://arxiv.org/abs/1710.08356))