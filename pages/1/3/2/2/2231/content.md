## Definition

We give a definition of an inner automorphism in any [[category]], originally due to Bergman.

Suppose $C$ is a category and $G$ is an object of $C$.
An __inner automorphism__ of $G$ is a family of automorphisms $p_f\colon H\to H$, one for every morphism $f\colon G\to H$ in $C$, for which the following square commutes for every morphism $g\colon H\to K$:
\begin{xymatrix}
H \ar[r]^{p_f} \ar[d]_g & H \ar[d]^g \cr
K \ar[r]_{p_{gf}} & K \cr
\end{xymatrix}

For example, if $C$ is the category of [[groups]], then every such family $p$ can be shown to satisfy $p_f(h)=f(g) h f(g)^{-1}$ for an element $g\in G$.

Bergman computes inner automorphisms for many algebraic structures, which tend to be given by a conjugation of some sort.

## Groups

An __inner automorphism__ $\phi:G\to G$ of a group $G$ is any [[automorphism]] $\phi_g$ of the form $h\mapsto g h g^{-1}$. The inner automorphisms form a [[subgroup]] $Inn(G)$, called the __inner automorphism group__ of $G$, of the entire [[automorphism group]] $Aut(G)$; it is the [[image]] of the natural map $G\to Aut(G)$ given by $g\mapsto\phi_g$. The [[center]] of a group $G$ is precisely the [[kernel]] of this natural map. Similarly, the monoidal center due to Drinfel'd and Majid, in the case when the monoidal category is Picard, is a $2$-category-theoretic kernel (an observation due to L. Breen). 

Higher analogues of the inner automorphism group were studied by Roberts and Schreiber. 

## Related concepts

* [[automorphism]]

## References

* [[George Bergman]], _An inner automorphism is only an inner automorphism, but an inner endomorphism can be something strange_, Publicacions Matemàtiques 56 (2012), 91-126.  [DOI](https://doi.org/10.5565/publmat_56112_04).


[[!redirects inner automorphisms]]
[[!redirects inner automorphism group]]