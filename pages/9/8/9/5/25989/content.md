## Basic construction via gluing

If $S$ is a scheme and $\mathcal{G}$ is a sheaf of commutative $\mathcal{O}_S$-algebras which are [[quasicoherent sheaf|quasicoherent]] as sheaves of $\mathcal{O}_S$-modules. For any affine $U\subset S$, the [[spectrum of a ring|spectrum]] of $\mathcal{G}(U)$ is a $U$-scheme.
By gluing these spectra over all affine $U$, 
one obtains an $S$-scheme $Spec(\mathcal{G})$, the __relative spectrum__ of $\mathcal{G}$ over $S$ (also called the global spectrum of $\mathcal{G}$).

An $S$-scheme which can be obtained as a relative spectrum over $S$ is said to be a __relative affine scheme__. 

## Application to vector bundles and generalizations

If $V$ is a vector space, then the symmetric algebra $Sym(V^*)$ can be interpreted as the algebra of regular functions on $V$ considered as an (affine) space. Vector bundles in algebraic geometry are usually viewed as locally free sheaves of $\mathcal{O}$-modules. However, one can construct their total spaces, using the [[symmetric algebra]] over the structure sheaf, obtaining a sheaf of algebras and then use the relative spectrum. 

In more detail, let $S$ be an [[algebraic scheme]] and $\mathcal{F}$ a [[quasicoherent sheaf]] of $\mathcal{O}_S$-modules. 
Then the correspondence $\mathcal{G}:V \mapsto Sym_{\mathcal{O}_S(V)}(\mathcal{F}(V))$ for affine $V$ extends to a sheaf of $\mathcal{O}_S$-algebras, hence one can apply the relative spectrum to obtain an $S$-scheme
$Spec(Sym_{\mathcal{O}_S}\mathcal{F})$ which should be viewed as the total space of the "bundle" $\mathcal{F}$ .

## Literature

* Stacks project 27.3 [Relative spectrum via glueing](https://stacks.math.columbia.edu/tag/01LL), 27.4 [Relative spectrum as a functor](https://stacks.math.columbia.edu/tag/01LQ)

category: algebraic geometry

[[!redirects relative affine scheme]]