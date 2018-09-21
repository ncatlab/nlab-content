
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Classical McKay correspondence

The classical McKay correspondence, named after John McKay, is a one-to-one correspondence between the [[McKay graphs]] of finite subgroups $G \subset \text{SL}_2(\mathbb{C})$ and the extended Dynkin diagrams of ADE type.

### Construction

Take $G\subset \text{SL}_2(\mathbb{C})$ finite. Then, let $\rho_0, ..., \rho_n$ denote the irreducible representations of $G$, with $\rho_0$ being the trivial representation. Then, set $\langle \rho_i \otimes \mathbb{C}^2, \rho_j \rangle = m_{i j}$. Since $\mathbb{C}^2$ is self-dual, as it admits an invariant non-degenerate skew-symmetric bilinear form, $m_{i j} = m_{j i}$. Finally, consider the vertices $v_0, ..., v_n$ with $m_{i j}$ vertices between each $v_i$ and $v_j$. Furthermore, for $m_{i j} = 1$, we do not need to write the weight of the corresponding arrow. The resulting graph is the [[McKay graph]] of $G$.


(...)

### Interpretation in K-theory

In ([GSZ](#GSZ)) the McKay correspondence is interpreted as an isomorphism on [[K-theory]], based on the observation that the [[representation ring]] of $G$ is equal to the $G$-[[equivariant K-theory]] of $\mathbb{C}^2$. This is isomorphic to the ordinary K-theory of the minimal resolution of the Kleinian singularity, $\mathbb{C}^2\sslash G$.

## Derived McKay correspondence

Due to T. Bridgeland, A. King, and M. Reid.

(...)



## Related concepts

* [[ADE classification]]

## References

Introductions and surveys include

* Graham Leuschke, _The McKay correspondence_ ([pdf](http://www.leuschke.org/uploads/McKay-total.pdf))

* Drew Armstrong, _Lectures on the McKay correspondence_, 2015 ([pdf scan of notes](http://www.math.miami.edu/~armstrong/Talks/McKay_Talca.pdf))

* [[John Baez]], _The Geometric McKay Correspondence_, ([Part I](https://golem.ph.utexas.edu/category/2017/06/the_geometric_mckay_correspond.html), [Part II](https://golem.ph.utexas.edu/category/2017/07/the_geometric_mckay_correspond_1.html))

Literature collection

* [[Miles Reid]], _[Links to papers on McKay correspondence](homepages.warwick.ac.uk/staff/Miles.Reid/McKay/)_

As anisomorphism between [[topological K-theory]] of the resolution and [[equivariant K-theory]] of the [[ADE-singularity]]:

* {#GSZ} G. Gonzalez-Sprinberg, [[Jean-Louis Verdier]], Construction g&eacute;om&eacute;trique de la correspondance de McKay, Ann. Sci. ́&Eacute;cole Norm. Sup.16 (1983) 409–449. ([numdam](http://www.numdam.org/item?id=ASENS_1983_4_16_3_409_0))

* [[Tom Bridgeland]], [[Alastair King]], [[Miles Reid]], _The McKay correspondence as an equivalence of derived categories_ ([pdf](http://www.ams.org/journals/jams/2001-14-03/S0894-0347-01-00368-X/S0894-0347-01-00368-X.pdf))

