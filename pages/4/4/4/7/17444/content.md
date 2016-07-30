+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}

### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--

# Contents
* automatic table of contents goes here
{:toc}

[[!redirects bi-Heyting toposes]]
[[!redirects biHeyting topos]]
[[!redirects Bi-Heyting topos]]
[[!redirects Bi-Heyting Topos]]
[[!redirects bi-Heyting Topos]]
[[!redirects bi-heyting topos]]

##Idea

A **bi-Heyting topos** is a [[topos]] whose lattices of subobjects carry the structure of a [[co-Heyting algebra]] in addition to their normal [[Heyting algebra]] structure and thereby permit to model bi-intuitionistic logic.

##Definition

A [[topos]] $\mathcal{E}$ such that the lattice $sub(X)$ of subobjects is a [[co-Heyting algebra|bi-Heyting algebra]] for every object $X\in\mathcal{E}$ is called a [[bi-Heyting topos]].

## Examples

* [[Boolean toposes]] are bi-Heyting since their subobject lattices are Boolean algebras which are self-dual Heyting algebras.

* Presheaf toposes and their [[essential subtoposes]].

##Properties

+-- {: .num_prop}
###### Proposition
A Grothendieck topos is bi-Heyting when finite unions distribute over arbitrary intersections:
$$
T\cup (\bigcap_{i\in I} T_i)=\bigcap_{i\in I} (S\cup T_i)\quad .
$$
=--

**Proof.** Because this distributivity amounts to the preservation of limits by $T\vee$\_ and implies by the [[adjoint functor theorem]] the existence of a left adjoint \_$\backslash T$ which provides the [[co-Heyting algebra]] structure. $\qed$

+-- {: .num_prop}
###### Proposition
Let $\mathcal{E}$ be a Grothendieck topos with generating set $\{G_i | i\in I\}$. Then $\mathcal{E}$ is bi- Heyting precisely iff the lattice of subobjects of $G_i$ is a bi-Heyting algebra for all $G_i$.
=--

cf. [Borceux-Bourn-Johnstone](#BBJ04) p.350.

+-- {: .num_prop #surjective_essential}
###### Proposition
Let $f:\mathcal{E}\to\mathcal{F}$ be a surjective [[essential geometric morphism]] between Grothendieck toposes. If $\mathcal{E}$ is bi-Heyting so is $\mathcal{F}$.
=--

cf. [Borceux-Bourn-Johnstone](#BBJ04) p.351.

+-- {: .num_prop}
###### Proposition
Let $\mathcal{C}$ be a small category. Then $Set^{\mathcal{C}^{op}}$ is bi-Heyting.
=--

**Proof.**  Let $|\mathcal{C}|$ be the discrete category on the objects of $\mathcal{C}$. The inclusion $i:|\mathcal{C}|\hookrightarrow \mathcal{C}$ induces a surjective essential geometric morphism $Set^{|\mathcal{C}|^{op}}\to Set^{\mathcal{C}^{op}}$ and the first of these is Booelan hence bi-Heyting. By prop. \ref{surjective_essential} follows the claim. $\qed$


##Remark

* In bi-Heyting toposes the co-Heyting algebra operations are generally not preserved by [[inverse image functor|inverse image functors]], so that the co-Heyting logical operators like [[co-Heyting negation]] or [[co-Heyting boundary]] are subject to _[[de re and de dicto]]_ effects. 

##Related entries

* [[co-Heyting algebra]]
* [[co-Heyting negation]]
* [[co-Heyting boundary]]
* [[bitopological space]]
* [[semi-abelian category]]
* [[mereology]]

##References

Bi-Heyting toposes are explicitly defined in

* {#BBJ04} [[Francis Borceux]], [[Dominique Bourn]], [[Peter Johnstone]], _Initial Normal Covers in Bi-Heyting Toposes_ , Arch. Math. **42** (2006) pp.335-356. ([pdf](http://mat.ub.edu/EMIS/journals/AM/06-4/johnston.pdf))

But their logical possibilities were exploited well before this e.g. in the work of Lawvere, Reyes and collaborators:

* {#Law86} [[William Lawvere]], _Introduction_ , pp.1-16 in Lawvere, Schanuel (eds.), _Categories in Continuum Physics_ , Springer LNM **1174** 1986.

* {#Law91a} [[William Lawvere]], _Intrinsic Co-Heyting Boundaries and the Leibniz Rule in Certain Toposes_ , pp.279-281 in A. Carboni, M. Pedicchio, G. Rosolini (eds.) , _[[Como|Category Theory - Proceedings of the International Conference held in Como 1990]]_ , LNM **1488** Springer Heidelberg 1991.

* {#Reyes}[[Gonzalo E. Reyes]], Houman Zolfaghari,  _Bi-Heyting Algebras, Toposes and Modalities_ , J. Phi. Logic **25** (1996) pp.25-43.




