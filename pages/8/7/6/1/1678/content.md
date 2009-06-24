A lax natural transformation is a transformation (i.e.
$0$-cell indexed collection of $1$-cells, like a [[natural transformation]]) that commutes up to a
coherent $2$-cell.


## Definitions ##

Given [[bicategories]] $C,D$ and (possibly [[lax functor|lax]]) $2$-[[2-functor|functors]]
$F,G:C\to D$, a _lax natural transformation_ $\alpha:F\Rightarrow G$
is given by

* for each $A\in C$ a $1$-cell $\alpha_A:F(A)\to G(A)$ in $D$,
as usual

* for each $f:A\to B$ in $C$ a 2-cell $\alpha_f: G(f) \circ
\alpha_A \Rightarrow \alpha_B \circ F(f)$

such that

* for each $A,B$, the $\alpha_f$ are the components of a
(strict) [[natural transformation]] $\alpha_{A,B}:
(\alpha_A)^* \circ G_{A,B} \dot{\to} (\alpha_B)_* \circ
F_{A,B}$

* the assignment $f\mapsto \alpha_f$ behaves sensibly with
respect to identities and composition (see the
references for details).

The word 'natural' is often dropped for brevity.

$\alpha$ is a _pseudo-natural_ transformation if each
$\alpha_f$ is [[isomorphism|invertible]], a _strict_ one if each is
an [[identity morphism|identity]].  An _oplax_ transformation is as above, only
with all 2-cells reversed.  As usual, nothing significant
changes if the definitions of _lax_ and _oplax_ are
swapped; it is a matter of convention.  (For example, we are following Leinster below, but the [[Elephant]] uses the reverse convention.)

+-- {: .query}
How consistent are different authors in this convention?  Should we include a warning ---or for that matter, a reassurance?  ---Toby

[[Finn Lawler|Finn]]:  I don't know myself, but back in [May](http://ncatlab.org/nlab/show/2009+May+changes) (see end of page) Jonas Frey said 'Johnstone in the elephant and Gurski in his PhD-thesis for example use an other orientation than Leinster and Borceux in their books'.  The one above is Leinster's.  I haven't seen any of the other references.

_Toby_:  OK, I just checked the Elephant, and it is reverse.

_Todd_: My own impression is that Leinster and Borceux are in the minority here, and that a bigger warning may be warranted. I think for instance that Johnstone is on the side of most Australians, who after all have done the most work in this area.

My own convention is that of Street: the arrow orientations in a product of [[parity complex]]es is to follow the usual sign conventions for chain complexes. For example, if I write $\alpha \otimes f$ instead of $\alpha_f$, and $\partial^-$ for 'source' and $\partial^+$ for 'target', and interpreting '+' as union, then for $\varepsilon \in \{-1, 1\}$ we would have 

$$\partial^{\varepsilon}(\alpha \otimes f) = \partial^{\varepsilon}(\alpha) \otimes f + \alpha \otimes (-1)^{dim(\alpha)} \partial^\varepsilon f$$ 

so accordingly, since $dim(\alpha) = 1$, the set of source cells of $\alpha \otimes f$ would be $\{F \otimes f, \alpha \otimes G\}$, if you follow my drift. Street's rule of thumb then is that 'lax' would follow this "normal" order, and 'colax' the opposite. 
=--

The [[category]] $Lax(F,G)$ consists of lax transformations from $F$ to $G$ and [[modification]]s between them.


## The Yoneda Lemma ##

Given a bicategory $C$, a lax functor $F:C\to Cat$ and a $0$-cell $A\in C$, there
are [[adjoint functor]]s

$$ I : Lax(y A,F) \stackrel{\to}{\leftarrow} F(A) : J $$

such that $J \dashv I$.  Here $y A:C \to Cat$ is the image of $A$ under the
bicategorical [[Yoneda embedding]].

+-- {: .proof}
###### Proof (sketch)

For $a\in F(A)$, let $J(a):y A\Rightarrow F$ be the lax transformation defined by $J(a)_B(f) = (F f)(a)$.  The components

$$  J(a)_g : F(g) \circ J(a)_X \dot{\to} J(a)_Y \circ g_* $$

for $g:X\to Y$ in $C$ are given by $F$'s comparison map $(F_{g,-})_a$.  The coherence conditions follow from those on $F$ wrt the associator and left unitor of $C$.  For $x:a\to b$ in $F(A)$, $J(x)$ is a modification because $F_{g,f}$ is a natural transformation (i.e. 2-cell in $Cat$).

Let $I(\alpha) = \alpha_A(1_A)$ as usual.  For $m:\alpha\ddot{\to}\beta$ a modification, $I(m)=(m_A)(1_A)$.

The unit $\eta: F A \dot{\to} I J$ at $a\in F A$ is the component $(F_A)_a$ of $F$'s comparison map, which is natural in $a$ by definition.  The counit $\epsilon_\alpha$ is obtained via the usual 1-chasing, and is given in components by

\[ (\epsilon_\alpha)_B(f) = \alpha_B(r_f) \circ (\alpha_f)(1_A) \]

where $r$ is the right unitor of $C$.  Some diagram-chasing confirms that this is indeed natural in everything, and so $\epsilon: J I \dot{\to} Lax(y A,F)$.

The triangle identities may be proved by expanding the definitions above and using the coherence conditions on lax functors and transformations and coherence of $C$.

See Gray for the case [[strict 2-categories]] and strict 2-functors.
=--

+-- {: .query}
[[Finn Lawler|Finn]]:  I don't know how natural this is in $F$ and $A$, but I'll try to figure it out.

Also, if you reverse the definitions of lax and oplax transformations, then you should do the same for functors, and I think in that case $I\dashv J$.
=--


## References ##

* Gray, [[Gray-adjointness-for-2-categories|Adjointness For
2-Categories]]

* Leinster, _Basic bicategories_,
[arXiv](http://arxiv.org/abs/math/9810017).

Note that both of these use somewhat outdated terminology.
