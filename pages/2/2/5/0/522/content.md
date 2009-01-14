Let $C$ be a [[closed monoidal category]] with [[interval object]] $I$. Then for any [[pointed object]] $pt \stackrel{pt_B}{\to}B$ in $C$ the _generalized universal $B$-bundle_ is (if it exists) the morphism

$$
  p : \mathbf{E}_{pt} B \to B
$$

which is the total composite vertical morphism of the pullback diagram

$$
  \array{
    \mathbf{E}_{\mathrm{pt}}B
    &\to&
    pt
    \\
    \downarrow && \downarrow^{pt_B}
    \\
    [I,B]
    &\stackrel{d_1}{\to}&
    B
    \\
    \downarrow^{d_0}
    \\
    B
  }
  \,.
$$

The fiber of the generalized universal bundle is the _loop monoid_ $\Omega_{pt} B$:

the sequence

$$
  \Omega_{pt}B \stackrel{i}{\to} \mathbf{E}_{pt} B \stackrel{p}{\to} B
$$

is exact in that $i$ is the kernel of $p$ in the sense of kernels of morphisms of [[pointed object]]s (see there).

#Examples#

In (higher) categorical contexts, take the interval object to the the interval category $I := \{a \to b\}$. Then

* For $C =$ [[Cat]], $B := \mathbf{B}G$ a one-object groupoid corresponding to a group $G$ with the unique point, $\mathbf{E}_{pt} \mathbf{B}G = \mathbf{E}G = G//G$ is the [[action groupoid]] of $G$ acting on itself. The sequence of groupoids is
$$
  G \to G//G \to \mathbf{B}G
  \,.
$$
This is the universal $G$-bundle in its groupoid incarnation. It is a theorem by Segal from the 1960s that indeed this maps, under [[geometric realization]] to the familiar universal $G$-bundle in $Top$. This is recalled in the following reference.

* For $C = 2Cat$, strict 2-categories , $B := \mathbf{B}G$ a strict one-object 2-groupoid corresponding to a strict [[2-group]] $G$ with the unique point, $\mathbf{E}_{pt} \mathbf{B}G = \mathbf{E}G$ was described under the name $INN(G)$ in

* Urs Schreiber, David Roberts, _The inner automorphism 3-group of a strict 2-group_, Journal of Homotopy and Related Structures, Vol. 3(2008), No. 1, pp. 193-244
([arXiv](http://arxiv.org/abs/0708.1741v2))

This was shown to be _action bigroupoid_ of $G$ acting on itself in

* Igor Bakovi&;ccaron;, _Bigroupoid 2-torsors _ PhD thesis, Munich (2008) ([pdf](http://edoc.ub.uni-muenchen.de/9209/)).

One can show that this $\mathbf{E} G$ indeed classifies principal $G$-2-bundles, as indicated in the last section of the above reference.

* One can take $B$ to be something very different from the familiar classifying groupoids. Taking it to be $n$Cat yields the [[subobject classifier]]s of higher [[topos|toposes]]:

  * $\mathbf{E}_{pt} (-1)Cat \to (-1)Cat$ is $\{\top\} \to \{\top, \bottom\}$, the [[subobject classifier]] in [[Set]];

  * $\mathbf{E}_{pt} 0Cat \to 0Cat$ is $Set_* \to Set$, the forgetful functor from [[pointed set]]s, which is the  2-[[subobject classifier]] in [[Cat]];

  * $\mathbf{E}_{pt} Cat \to Cat$ is $Cat_* \to Cat$.

These cases for $n= 0$ and $n=1$ have been considered in the context of universal category bundles in 

* Kathryn Hess, _[[HessLackBundCat.pdf:file]]_ .

The discussion there becomes more manifestly one of bundles if one regards all morphisms $C \to Set$ appearing there as being the right legs of [[anafunctor]]s. 

Notes on the general picture here are for instance at [[schreiber:Nonabelian homotopical cohomology and fiber bundles]].
