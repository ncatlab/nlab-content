
#Contents#
* automatic table of contents goes here
{:toc}

## Idea ##

The general procedure in [[K-theory]] is to assign a **K-theory spectrum** $\mathbf{K}(C)$ to a [[stable (∞,1)-category]] $C$. 

In practice these stable $(\infty,1)$-categories are usually [[presentable (infinity,1)-category|presented]] by [[homotopical category|homotopical categories]] called [[Waldhausen category|Waldhausen categories]].

The _Waldhausen S-construction_ on a Waldhausen category $C'$ produces a [[simplicial set]] equivalent to the K-theory spectrum (see below) of the [[simplicial localization]] $C$ of $C'$: it is a concrete algorithm for computing K-theory spectra.

## Definition ##

Recall from the definition at [[K-theory]] that the K-theory spectrum $K(C)$ of the [[(∞,1)-category]] $C$ is the diagonal simplicial set on the bisimplicial set $Core(Func(\Delta^n,C))$ of sequences of morphisms in $C$ and equivalences between these.

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


## References ##


The Waldhausen S-construction is recalled for instance in section 1 of 

* Paul D. Mitchener, _Symmetric Waldhausen K-theory spectra of topological categories_ ([pdf](http://bib.mathematics.dk/unzip.php?filename=DMF-2001-05-001-v1.pdf.gz))