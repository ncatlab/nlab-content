
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

In a [[finite]] [[group]] $G$, for every prime $p$, a maximal $p$-[[p-torsion|torsion]] subgroup of $G$ is also known as a **Sylow $p$-subgroup**.

## Facts

Let the order of $G$ be $ r p^k $, where $ r $ is coprime to $p$.

Let $H \lt G$ be a subgroup of rank $p^l$, and consider the left action of $G$ on right cosets of $H$:
$$ (g, x H )\mapsto (g x) H .$$
This action induces further an action of $G$ on $(G / H) \mathbf{C} (p^{k-l})$, the subsets of $G/H$ of size $p^{k-l}$.  The number of these, $\binom{ r p^{k-l} }{ p^{k-l} } $, is congruent to $r$, mod $p$, and hence some orbit must have size coprime to $p$, hence necessarily dividing $r$, hence some set of cosets must have stabilizer of size at least $ p^k $.  [[exercise|One checks]] that on the other hand, the stabilizer of a set of cosets is at most the size of their union for a *very good* reason, and furthermore is a subgroup of $G$.  Lastly, every orbit contains a representative that contains $H$. In consequence,

+-- {: .num_theorem #pSylowModp}
###### Theorem 
Every $p$-subgroup $H$ of $G$ is contained in a subgroup of order $p^k$, which is necessarily a maximal $p$-subgroup.  The number of maximal $p$-subgroups including $H$ is congruent to $1$ mod $p$.
=--

One also has

+--  {: .num_theorem #SylowConj}
###### Theorem
Any two Sylow $p$-subgroups of $G$ are conjugate. 

=--

See [[class equation]] for a detailed discussion of these matters. (Now updated to take into account the proof below. The discussion above refers to a more involved proof from an earlier page version, which in turn was adapted from the Wikipedia article; it may be found [here](https://nforum.ncatlab.org/discussion/6646/class-equation/), comment 4.) The following slick proof for the existence of Sylow subgroups was suggested to us by [[Benjamin Steinberg]]. 

+-- {: .proof} 
###### Proof that Sylow subgroups exist 
First observe that if a group $G$ has a $p$-Sylow subgroup $P$, then so does each of its subgroups $H$. For we let $H$ act on $G/P$ by left translation, and then note that since $G/P$ has cardinality prime to $p$, so must one of its connected components $H/Stab(a_x)$ in the $H$-set decomposition 

$$G/P \cong \sum_{orbits\; x} H/Stab(a_x)$$ 

($a_x \in G/P$ a representative of its orbit $x$), making $Stab(a_x)$ a $p$-Sylow subgroup of $H$. 

Then, if $H$ is any group, apply this observation to the embedding 

$$H \stackrel{Cayley}{\hookrightarrow} Perm({|H|}) \hookrightarrow GL_{{|H|}}(\mathbb{Z}/(p))$$ 

where we embed the permutation group via permutation matrices into the group $G$ consisting of matrices ${|H|} \times {|H|} \to \mathbb{Z}/(p)$. Letting $n$ be the cardinality of $H$, the order of $G$ is $(p^n - 1)(p^n - p)\ldots (p^n - p^{n-1})$, with maximal $p$-factor $p^{n(n-1)/2}$. This $G$ has a $p$-Sylow subgroup given by unitriangular matrices, i.e., upper-triangular matrices with all $1$'s on the diagonal, and we are done. 
=-- 

## Related pages

* [class equation](class+equation#sylow_theorems)

* [[group actions on n-spheres]]

##References

For a generalisation of Sylow theory to finite [[∞-groups]], that is, ∞-groups with finitely many non-trivial homotopy groups which are all finite, see

* [[Matan Prasma]], [[Tomer Schlank]], _Sylow theorems for ∞-groups_, ([arXiv:1602.04494](https://arxiv.org/abs/1602.04494))

[[!redirects Sylow p-subgroups]]