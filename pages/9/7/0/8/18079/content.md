# Toposes are extensive

* table of contents
{: toc}

## Statement

Every [[elementary topos]] is a finitary [[extensive category]].  In fact, more is true: if an elementary topos has [[coproducts]] indexed by any [[arity class]] $\kappa$, then it is $\kappa$-extensive.  In particular, a cocomplete elementary topos is infinitary extensive.

## Proofs

There are several possible proofs.  In all cases, stability of coproducts under pullback is automatic since a topos is locally cartesian closed, so it suffices to consider [[disjoint coproduct|disjointness]].

### From finitary to infinitary

As shown at [[extensive category]], if we assume [[classical logic]] then $\coprod_{j\in J} A_j \cong A_1 \sqcup A_2 \sqcup \coprod_{j\neq 1,2} A_j$, so that in a finitary-extensive category, any existing coproducts are stable and disjoint.  Thus, in this case it suffices to deal with finite coproducts.  However, in topos theory we are often interested in toposes "over an arbitrary base", in which case the ambient logic is [[constructive logic]] and so this argument does not apply.

Nevertheless, we mention a couple of proofs that apparently apply only to the finitary case in addition to the fully general version.

### Via pushouts of monos

A proof applying to finite coproducts is given in [Johnstone, A2.4.4](#Johnstone): since $0\to X$ and $0\to Y$ are monic, it suffices to show that the pushout of a mono is a mono and also a pullback.

To see this, let $f:A\rightarrowtail B$ be monic and $g:A\to C$ any morphism, and let $h:B\to P C$ be the name of $(f,g):A\to B\times C$, i.e. $(f,g)$ is the pullback $\in_C \rightarrowtail P C \times C$ along $(h,1)$.  In other words, $(k,l):X\to B\times C$ factors through $(f,g)$ iff $(h k,l)$ factors through $\in_C$ (i.e. $l(x) \in h k(x)$ for all $x:X$ in the [[internal logic]]).  This is in particular the case if $h k = \{\} \circ l$ (i.e. $h k(x) = \{l(x)\}$ for all $x:X$ in the internal logic), which implies that the square
$$\array{A & \xrightarrow{g} & C \\ ^f\downarrow && \downarrow^{\{\}} \\ B & \xrightarrow{h} & P C }$$
is a pullback.

Now given a pushout
$$\array{A & \xrightarrow{g} & C \\ ^f\downarrow && \downarrow^{d} \\ B & \xrightarrow{c} & D }$$
with $f$ monic, with $h$ as above we have an induced $m:D \to P C$ by the universal property of the pushout, with $m d = \{\}$ and $m c = h$.  Since $\{\}$ is monic, $d$ must also be monic, and since the previous square is a pullback, so must this one be.

### Via quasi-disjointness

A different proof applying to finite coproducts can be obtained by combining A1.5.14 and A1.6.2 of [Johnstone](#Johnstone).  Define $R$ and $S$ to make the following squares pullbacks:
$$\array{ R & \xrightarrow{r} & A & \xleftarrow{s} & S\\
  ^{r'}\downarrow && \downarrow^i && \downarrow\\
  A & \xrightarrow{i} & A+B & \xleftarrow{j} & B}$$
Specifically, $(r,r')$ is the [[kernel pair]] of $i$.  In particular, there is an induced diagonal $\triangle : A \to R$ such that $r \triangle = 1_A$.  On the other hand, since pullback preserves colimits, $(r,s)$ is a coproduct diagram.  Thus, the pair of morphisms $1_R:R\to R$ and $\triangle \circ s : S\to R$ factor (uniquely) through some $h:A\to R$, so that in particular $h r = 1_R$.  Thus, $r:R\to A$ has both a left and a right inverse, so it is an isomorphism, and hence $i$ is monic.  Dually, $j$ is monic.

Now we claim that any two morphisms $f,g:S\to X$ with domain $S$ are equal.  For the pair of morphisms $R \xrightarrow{r} A \to A+X$ and $S \xrightarrow{f} X \to A+X$ factor uniquely through $A$ (which, recall, is the coproduct $R+S$).  But since $r$ is an isomorphism, this factorization must be the left coprojection $A\to A+X$.  Therefore, the composite $S \xrightarrow{f} X \to A+X$ is equal to the composite $S \xrightarrow{s} A \to A+X$, and similarly so is the composite $S \xrightarrow{g} X \to A+X$.  Since $X\to A+X$ is monic by the previous paragraph, $f= g$.

Finally, since $0$ is a strict initial object, $0\to S$ is monic.  And of course $1_S : S\to S$ is also monic, and these two monomorphisms are classified by two maps $f,g:S\to \Omega$ into the subobject classifier.  By the previous paragraph, $f= g$, hence $S\cong 0$ and is initial.

### Via logical functors

Finally, we give a proof that applies constructively to arbitrary coproducts.  This proof is due to Moens and/or Jibladze or both (I'm not quite sure) and can be found (in fibered-topos language) in [Streicher, Appendix A](#Streicher).

Suppose $\mathcal{E}$ a topos with $J$-indexed coproducts for all $J$ belonging to some [[arity class]] $\kappa$.  Then $\Delta : \mathcal{E} \to \mathcal{E}^J$ is a [[logical functor]] with a left adjoint $\coprod_J$, so (by A2.3.8 of [Johnstone](#Johnstone), see also [[logical functor]]) to show that $\coprod_J$ induces equivalences $\mathcal{E}^J/\{A_j\} \to \mathcal{E}/\coprod_j A_j$ (which is one characterization of $\kappa$-extensivity) it suffices for $\coprod_J$ to be faithful.  As with any adjunction, to show the left adjoint to be faithful it suffices to show that the unit $\eta : Id \to \Delta \coprod_J$ is monic, which means in this case that the injections $A_j \to \coprod_j A_j$ are all monic.

Now since $\kappa$ is an arity class, $J\times J$ also belongs to it, and hence so do the fibers of the diagonal $J\to J\times J$.  Thus, $\mathcal{E}$ has coproducts indexed by the [[subsingletons]] determined by the equalities $(j=k)$ for any $j,k\in J$.  Moreover, for any $j$ we can write $A_j = \coprod_{k\in J} \coprod_{(j=k)} A_{k}$, and under this identification the injection $A_j \to \coprod_{k\in J} A_{k}$ is obtained by applying the functor $\coprod_J$ to the evident family of maps $\coprod_{(j=k)} A_{k}\to A_k$.  But since $\coprod_J$ is the left adjoint of a logical functor, it preserves monomorphisms (see A2.4.8 of [Johnstone](#Johnstone), also [[logical functor]]).  Thus, it suffices to prove that each $\coprod_{(j=k)} A_{k}\to A_k$ is monic.

Now, the functor $\coprod_{(j=k)} : \mathcal{E}^{(j=k)} \to \mathcal{E}$ has a logical right adjoint sending $B\in\mathcal{E}$ to the subsingleton-indexed family $\{B\}_{(j=k)}$, and the units of its adjunction $\{A\}_{(j=k)} \to \{ \coprod_{(j=k)} A \}_{(j=k)}$ are isomorphisms (to define an inverse, it suffices to consider the object $\coprod_{(j=k)} A$ under the assumption $j=k$, in which case this object is isomorphic to $A$).  Thus, $\coprod_{(j=k)}$ is fully faithful, and in particular faithful, and since its right adjoint is also logical, it induces an equivalence $\mathcal{E}^{(j=k)} \simeq \mathcal{E}/\coprod_{(j=k)} 1$.

However, the unit of a pullback adjunction $\mathcal{E}/I \rightleftarrows \mathcal{E}$ is $A\to A\times I$, and if this is an isomorphism then in particular $I\cong I\times I$ and thus $I$ is subterminal.  Moreover, in this case the counits of the adjunction are the projections $A\times I \to A$, which are pullbacks of the mono $I\to 1$ and therefore also monic.  Finally, in our case where $I = \coprod_{(j=k)} 1$, the counit associated to $A_k$ is precisely the map $\coprod_{(j=k)} A_{k} \to A_k$ that we wanted to prove to be monic.

## References

* {#Johnstone} [[Peter Johnstone]], [[Sketches of an Elephant]]

* {#Streicher} [[Thomas Streicher]], *Fibered categories a la Jean Benabou*, [citeseer](http://citeseerx.ist.psu.edu/viewdoc/citations;jsessionid=76DB3E2F57E81C74E05109B8F7E11E44?doi=10.1.1.678.919)
