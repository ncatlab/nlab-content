
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--

#Contents#
* automatic table of contents goes here
{:toc}

## Idea 

Model structures on chain complexes are [[model category]] structures on [[categories of chain complexes]] whose weak equivalences are [[quasi-isomorphism]]s. 

Via these model structures, all of the standard techniques in [[homological algebra]], such as injective and projective resolutions, are special cases of constructions in [[homotopy theory]], such as cofibrant and fibrant [[resolution]]s.

The existence of these model structures depends subtly on whether the chain complexes in question are bounded or not. 

### In non-negative degree

Chain complexes in non-negative degree in an [[abelian category]] $A$ are special in that they may be identified via the [[Dold?Kan correspondence]] as [[simplicial object]]s in $A$.

$$
  Ch_+(A) \simeq A^{\Delta^{op}}
  \,.
$$

At least if $A$ is the category of [[abelian groups]], so that $A^{\Delta^{op}}$ is the category of abelian [[simplicial group]]s it inherits naturally a model category structure from the [[model structure on simplicial sets]], which [[presentable (∞,1)-category|presents]] the [[(∞,1)-category]] of [[∞-groupoid]]s.

The model structure on chain complexes transports this presentation  of the special $\infty$-groupoids given by abelian simplicial groups along the Dold-Kan correspondence to chain complexes.

Analogous statements apply to the category of unbounded chain complexes and the canonical [[stable (infinity,1)-category]] [[Spec]] of [[spectrum|spectra]]. 

### For unbounded chain complexes

See the [references](#References) by Spaltenstein and Hinich below.

## Definitions 

(...)

### Model structures on cochain complexes in non-negative degree {#CochainNonNeg}

Let $C$ be an [[abelian category]]. 

Recall that by the dual [[Dold-Kan correspondence]] the category $C^\Delta$ of [[cosimplicial object]]s in $C$ is equivalent to the catagory $Ch^\bullet_+(C)$ of [[cochain complex]]es in non-negative degree. This means that we can transfer results discussed at [[model structure on cosimplicial objects]] to cochain complexes (see [Bousfield2003, section 4.4](http://arxiv.org/PS_cache/math/pdf/0312/0312531v1.pdf) for more).

#### General results

Let $G \in Obj(C)$ be a [[class]] of objects, such that $C$ has enough $G$-[[injective object]]s. 

Then there is a model category structure $Ch^\bullet_+(C)_G$ whose

* weak equivalences are maps $f : X \to Y$ such that for each $A \in G$ the induced map $C(Y,A) \to C(X,A)$ is a [[quasi-isomorphism]] of chain complexes of abelian groups;

* $f$ is a cofibration if it is $G$-monic in positive degree;

* $f$ is a fibration if it is degreewise a [[split epimorphism]] with $G$-injective kernel.
 
If for example we take $G$ to be the class of all objects of $C$, then this induces a model structure $Ch^\bullet_+(C)_{tot}$ whose

* weak equivalences are cochain [[homotopy equivalence]]s;

* fibrations are morphisms that are degreewise [[split epimorphism]]s;

* cofibration are morphisms that are in positive degree [[split monomorphism]]s.

As an example of that, if $C = $ [[Vect]] is a category of [[vector space]]s over some field, we have that every epi/mono splits and that every [[quasi-isomorphism]] is a homotopy equivalence. 

This is the model structure which induces the [[transferred model structure|transferred]] [[model structure on dg-algebra]]s over a field. 

#### The projective model structure {#CochainNonNegProj}

We record a detailed proof of the following statement.

+-- {: .un_prop}
###### Proposition

The catgeory $Ch^\bullet_+(Ab)$ of non-negatively graded cochain complexes of [[abelian group]]s becomes a model category with

* fibrations the degreewise surjections;

* weak equivalences the [[quasi-isomorphism]]s.

=--


+-- {: .proof}
###### Proof


As usual, write $\mathbb{Z}[n]$ for the complex concentrated on the additive group of [[integer]]s in degree $n$, and $\mathbb{Z}[n-1,n]$ for the cochain complex $(0 \to \cdots 0 \to \mathbb{Z} \stackrel{Id}{\to} \mathbb{Z} \to 0 \cdots)$ with the two copies of $\mathbb{Z}$ in degree $n-1$ and $n$.


**Lemma**

The canonical inclusions $0 \to \mathbb{Z}[n]$ and $\mathbb{Z}[n] \to \mathbb{Z}[n-1,n]$ are cofibrations, in that they  have the [[left lifting property]] against acyclic fibrations.

_Proof._  Let $p : A \stackrel{\simeq}{\to} B$ be an acylic fibration. We need to construct a lift in 

$$
  \array{
     \mathbb{Z}[n] &\stackrel{f}{\to}& A
     \\
     \downarrow &{}^{\mathllap{\sigma}}\nearrow& \downarrow^{\iota}
     \\
     \mathbb{Z}[n-1,n] &\stackrel{g}{\to}& B
  }
  \,.
$$

First consider the case $n \gt 0$. Then such a lift
is equivalently an element $\sigma \in A_{n-1}$ such that 

* $d_A \sigma = f_n(1)$

* $\iota_{n-1}(\sigma) = g_{n-1}(1)$.

Now...

(...out of time...to be continued...)



=--


## History and references {#References}

Of course the description of model categories of chain complexes as ([[presentable (infinity,1)-category|presentations]] of) special cases of (stable) $(\infty,1)$-categories is exactly opposite to the historical development of these ideas. 

While the homotopical treatment of weak equivalences of chain complexes ([[quasi-isomorphism]]s) in [[homological algebra]] is at the beginning of all studies of higher categories and a "folk theorem" ever since

* [[Andre Joyal]], Letter to Alexander Grothendieck. April 11, 1984

it seems that the injective model structure on chain complexes has been made fully explicit in print only in proposition 3.13 of

* Tibor Beke, _Sheafifiable homotopy model categories_ ([arXiv](http://arxiv.org/abs/math/0102087), [pdf](http://arxiv.org/PS_cache/math/pdf/0102/0102087v1.pdf))

(at least according to the remark below that).

The projective model structure is discussed after that in 

* [[Mark Hovey]], _Model category structures on chain complexes of sheaves_, Trans. Amer. Math. Soc. 353, 6 ([pdf](http://www.mathaware.org/tran/2001-353-06/S0002-9947-01-02721-0/S0002-9947-01-02721-0.pdf))

Variant model structures on chain complexes are discussed in

* [[Dan Christensen]], [[Mark Hovey]], _Quillen model structures for relative homological algebra_ ([pdf](http://jdc.math.uwo.ca/papers/relative.pdf))

### For unbounded chain complexes

Work specifically on model structures on unbounded complexes includes the following.

Spaltenstein wrote a famous paper 

* N. Spaltenstein, _Resoutions of unbounded complexes_, Compositio Mathematica, 65 no. 2 (1988), p. 121-154 ([numdam](http://www.numdam.org/item?id=CM_1988__65_2_121_0))

on how to do homological algebra with unbounded complexes (in both sides) where he introduced notions like K-projective and K-injective complexes. Later, 

* V. Hinich, _Homological algebra of homotopy algebras_, Comm. Algebra, vol. 25 (1997), no. 10, 3291-3323
([pdf at author's page](http://math.haifa.ac.il/hinich/WEB/mypapers/haha.pdf)) 

shown that there is a model category structure on the category of unbounded chain complexes, reproduced Spaltenstein's results from that perspective and extended them widely. See also

* J. D. Christensen, Derived categories and projective classes, 2005 ([hopf archive](http://hopf.math.purdue.edu/cgi-bin/generate?/Christensen/derived))


[[!redirects model structures on chain complexes]]

[[!redirects model structures on cochain complexes]]
