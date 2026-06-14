
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}



## Idea 

Antinatural transformations provide a way to define maps between covariant and contravariant functors in the setting of [[dagger category | dagger category theory]]. The point is that composing with a dagger (which is contravariant) makes a [[covariant functor]] contravariant and a [[contravariant functor]] covariant.


## Definition ##

\begin{definition}
Given a [[dagger category]] $(C,\dagger)$ and a [[category]] $D$ with a [[covariant functor]] $F: C \to D$ and a [[contravariant functor]] $G: C^{\mathrm{op}} \to D$, an __antinatural transformation__ $\alpha : F \Rightarrow G$ between them is a [[natural transformation]] from $F$ to $G \circ \dagger$.

Similarly, an antinatural transformation $\beta: G \Rightarrow F$ is a [[natural transformation]] from $G$ to $F \circ \dagger$.
\end{definition}

\begin{remark}
A [[contravariant functor]] from $C$ to $D$ can either be interpreted as a [[functor]] $C^{\mathrm{op}} \to D$ or as a functor $C \to D^{\mathrm{op}}$. Thus, a [[dagger category | dagger structure]] on $C$ is both a functor $\dagger: C \to C^{\mathrm{op}}$ and a functor $\dagger: C^{\mathrm{op}} \to C$, by abuse of notation. It thus makes sense to precompose both $F$ and $G$ with $\dagger$. 

Likewise, if we instead wrote $G$ in the definition above as a functor $G:C \to D^{\mathrm{op}}$, we would need $D$ to have a dagger structure to recover the analogous definition.
\end{remark}


## Related entries

* [[natural transformation]]

* [[H-star-category]]


## References

Introduced in:

* {#Baez97} [[John Baez]], _Higher-dimensional algebra II: 2-Hilbert spaces_, Adv. Math. **127** (1997) 125-189 &lbrack;[arXiv:q-alg/9609018](http://arxiv.org/abs/q-alg/9609018)&rbrack;


