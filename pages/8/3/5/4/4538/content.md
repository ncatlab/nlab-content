
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Cohomology
+-- {: .hide}
[[!include cohomology - contents]]
=--
#### Homological algebra
+-- {: .hide}
[[!include homological algebra - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

The _universal coefficient theorem_ states how [[ordinary homology]]/[[ordinary cohomology]] determines [[homology]]/[[cohomology]] with arbitrary [[coefficients]].

For $C_\bullet$ a [[chain complex]] (of [[abelian groups]]) and $F$ a [[field]] (the _coefficient field_), the [[homology group]] $H_p(C,F)$ and the [[cohomology group]] $H^p(C,F)$ are indeed related by [[dualization]]: $ H^p(C,F) \simeq Hom_F(H_p(C,F), F)$.
If the coefficients are not a [[field]] but an arbitrary [[abelian group]], then this relationship receives a correction by an [[Ext]]-group. This is discussed below in _[For ordinary cohomology](#InCohomology)_.

Dually, again if $F$ is a field then there is an isomorphism $H_n(C) \otimes F \simeq H_n(C \otimes F)$ and for more general $F$ this is corrected by a [[Tor]]-group. This is discussed below in _[For ordinary homology](#InHomology)_.

More generally, under suitable conditions there are universal coefficient theorems that relate [[generalized (Eilenberg-Steenrod) cohomology]] to the dual of [[generalized homology]]. This is discussed below in _[For generalized cohomology](#ForGeneralizedCohomology)_.

There is also a version of the theorem for Kasparov's [[KK-theory]], see the [references](#ReferencesForKK).


## Statement

### For ordinary cohomology
 {#InCohomology}


Let $C_\bullet$ be a [[chain complex]] of  [[free abelian groups]]. Let $A$ be an arbitrary [[abelian group]]. 

Write 

* $C^\bullet \coloneqq Hom_{Ab}(C_\bullet, A)$ for the dual [[cochain complex]] with respect to $A$;

* $H_n(C)$ for the [[chain homology]] of $C_\bullet$

* $H^n(C,A)$ for the [[cochain cohomology]] of $C^\bullet$ hence for the cochain cohomology of $C_\bullet$ with [[coefficients]] in $A$.

+-- {: .num_remark }
###### Remark

There is a canonical morphism of [[abelian groups]]

$$
  \int_{(-)}(-) : H^n(C,A) \to Hom_{Ab}(H_n(C,\mathbb{Z}), A)
$$

given by sending a [[cocycle]] to [[evaluation]] of that cocycle on a [[chain]]:

$$
  [\omega] \mapsto 
   \left( [\sigma] \mapsto \int_{\sigma} \omega \coloneqq \omega(\sigma) \right)
$$

=--

+-- {: .num_theorem #OrdinaryStatementInCohomology}
###### Theorem
**(universal coefficient theorem in ordinary cohomology)**

The morphism $h$ is surjective and its [[kernel]] is the [[Ext group]] $Ext^1(H_{n-1}(C, \mathbb{Z}), A)$. In other words, there is 
a [[short exact sequence]]

$$
  0 \to 
   Ext^1(H_{n-1}(C), A)
   \to 
   H^n(C, A) 
   \to 
   Hom_{Ab}(H_n(C), A)
   \to 
   0
$$

hence 

$$
  0 \to 
   Ext^1(H_{n-1}(C), A)
   \to 
   H^n(Hom_{Ab}(C_\bullet,A)) 
   \to 
   Hom_{Ab}(H_n(C), A)
   \to 
   0
$$

Moreover, this sequence [[split exact sequence|splits]] (non-canonically).

=--

We reproduce the direct proof given for instance in ([Boardman](#Boardman)).

+-- {: .num_lemma #LemmaForUCTInOrdinaryCohomology}
###### Lemma

Given a homomorphism $A_1 \stackrel{f}{\to} A_2 \stackrel{g}{\to} A_3$ of [[abelian groups]] together with a [[retract]] $s : A_3 \to A_2$ of $g$, there is a [[short exact sequence]] of [[cokernels]]

$$
  0 \to coker f \stackrel{g'}{\to} coker(g \circ f) \to coker(g) \to 0
  \,.
$$ 

=--

+-- {: .proof}
###### Proof 

Since we work in [[Ab]], all the [[cokernels]] appearing here (as discussed there) may be expressed as [[quotients]], e.g $coker(f) \simeq A_2/im(f)$.

The sequence of inclusions $im(g \circ f) \hookrightarrow im(g) \hookrightarrow A_3$ induces the canonical [[short exact sequence]]

$$
  0
   \to
  \frac{im(g)}{im(g \circ f)}
    \to
  \frac{A_3}{im(g \circ f)}
    \to
  \frac{A_3}{im(g)}
   \to
  0
$$

and we claim that this is already isomorphic to the one stated in the lemma. This is manifestly true for the two terms on the right. For the term on the left observe that $g$ induces a morphism $g' : A_2 / im(f) \to A_3 / im(g \circ f)$. By the existence of the retract $s$ this has itself a retract. Moreover it factors as

$$
  g' : A_1/im(f) \to im(g)/im(g \circ f) \hookrightarrow A_3/ im(g \circ f)
  \,.
$$

Therefore the first morphism here on the left has to be an isomorphism, too.


=--

+-- {: .proof}
###### Proof (of theorem \ref{OrdinaryStatementInCohomology})

Write 

$$
  0 \to B_n \to Z_n \to H_n \to 0
$$

for the [[short exact sequence]] of [[boundaries]], [[cycles]], and [[homology groups]] of $C_\bullet$ in degree $n$. Since $C_n$ is assumed to be a [[free abelian group]] and since $B_n$ and $Z_n$ are [[subgroups]], it follows that these are also free abelian, by the abelian [[Nielsen-Schreier theorem]]. Therefore this sequence exhibits a [[projective resolution]] of the group $H_n$. It follows that the [[Ext]]-group $Ext^1(H_n,A)$ is characterized by the short exact sequence

\[
  \label{ExtES}
  Hom(Z_n, A) \to Hom(B_n,A) \to Ext^1(H_n,A) \to 0
  \,.
\]

Notice also that the short exact sequence

\[
  \label{ChainCycleBoundarySES}
  0 \to Z_n \to C_n \stackrel{\partial}{\to} B_{n-1} \to 0
\]

is [[split exact sequence|split]] because, as before, $B_{n-1}$ is free abelian. Using these two exact sequences on the left and right of the short exact sequence

$$
  0 \to Z_n/B_n \to C_n/B_n \to C_n/Z_n \to 0
$$

shows that this is equivalent to

\[
  \label{HomologyBoundariesSES}
  0 \to H_n \to C_n/B_n \stackrel{\partial}{\to} B_{n-1}
  \,.
\]

Again this splits as $B_{n-1}$ is free abelian. 

In addition to these exact sequence consider the decomposition

$$
  \partial
  : 
  C_n
  \to
  C_n/B_n
  \to 
  C_n/Z_n
  \stackrel{\simeq}{\to}
  B_{n-1}
  \hookrightarrow
  Z_{n-1}
  \hookrightarrow
  C_{n-1}
$$

and apply $Hom(-,A)$ to obtain the diagram

$$
  \array{
    && && 0
    \\
    && && \uparrow
    \\
    && && Hom(H_n,A)
    \\
    && && \uparrow
    \\
    Hom(B_n,A) &\leftarrow& Hom(C_n,A)
    &\stackrel{i}{\leftarrow}&
    Hom(C_n/B_n,A)
    &\leftarrow&
    0
    &&   
    0
    \\
    && && \uparrow^{\mathrlap{Hom(\bar \partial,A)}}
    && && \uparrow
    \\
    0 &\leftarrow& Ext^1(H_n,A) &\leftarrow& Hom(B_{n-1},A)
    && \leftarrow &&
    Hom(Z_{n-1},A)
    \\
    && && \uparrow && \nwarrow && \uparrow
    \\
    && && 0 && && Hom(C_{n-1},A)
  }
$$

Here the right vertical sequence is exact, because (eq:ChainCycleBoundarySES) splits, and the left vertical sequence is exact because (eq:HomologyBoundariesSES) splits.  The upper horizontal sequence is exact because the [[hom functor]] takes [[cokernels]] to [[kernels]] and finally the lower horizontal sequence is the exact sequence (eq:ExtES).

Since therefore $i$ and $Hom(\bar \partial,A)$ are monomorphisms, it follows that the degree $n$-[[cocycles]] are

$$
  Z^{n-1} \coloneqq ker( Hom(C_{n-1},A) \to Hom(C_n,a) )
  \simeq
  ker( Hom(C_{n-1},A) \to Hom(B_{n-1}, A) )
  \,.
$$

Using this for $n-1$ replaced by $n$ shows by the upper horizontal exact sequence that

$$
  Z^n = Hom( C_n/B_n, A)
  \,.
$$

Similarly the [[coboundaries]] are seen to be

$$
  B^n \coloneqq im Hom(\partial,A) \simeq
  im ( Hom(Z_{n-1}, A) \to Hom(C_n/B_n), A )
  \,.
$$

Together this gives the cochain cohomology as

$$
  H^n(C,A) \coloneqq Z^n / B^n 
  \simeq
  coker ( Hom(Z_n, A) \to Hom( C_n/B_n, A ) )
  \,.
$$

Now the universal coefficient theorem follows by 
going into lemma \ref{LemmaForUCTInOrdinaryCohomology} 
with the identifications
$A_1 = Hom(Z_{n-1}, A)$, $A_2 = Hom(B_{n-1}, A)$, $A_3 = Hom(C_n/B_n,A)$.


=--

### For ordinary homology
 {#InHomology}


Let $C_\bullet \in Ch_\bullet(Ab)$ be a [[chain complex]] of [[free abelian groups]], and let $A \in $ [[Ab]] be any abelian group. Write $C_\bullet \otimes A$ etc. for the degreewise [[tensor product of abelian groups]].

More generally, let $R$ be a [[ring]] which is a [[principal ideal domain]] (in the above $R = \mathbb{Z}$ is the ring of [[integers]]), let $C_\bullet \in Ch_\bullet(R Mod)$ be a chain complex of [[free modules]] over $R$, let $A \in R Mod$ be any $R$-[[module]] and write $C_k \otimes_R A$ for the [[tensor product of modules]] over $R$.

+-- {: .num_theorem #TheoremInOrdinaryHomology}
###### Theorem

For each $n \in \mathbb{N}$ there is a [[short exact sequence]]

$$
  0 
   \to 
  H_n(C_\bullet) \otimes_R A
   \to   
  H_n(C_\bullet \otimes_R A)
   \to 
  Tor_1^{R Mod}(H_{n-1}(C_\bullet), A)
   \to 
  0
  \,
$$

where on the right we have the first [[Tor]]-module of the [[chain homology]] $H_{n-1}(C_\bullet)$ with $A$. 

=--

+-- {: .num_remark }
###### Remark

A fairly direct generalization of this statement and its proof is the [[Künneth theorem]] in ordinary homology, see at _[K&#252;nneth theorem - In ordinary homology](http://ncatlab.org/nlab/show/K%C3%BCnneth+theorem#InOrdinaryHomology)_.

=--

We spell out a proof along the lines for instance given in ([Hatcher, 3.A](#Hatcher)) or ([Chen, section 3](#Chen)).

+-- {: .num_lemma #LongSequenceForHomologyWithCoefficients}
###### Lemma

For $C_\bullet$ a [[chain complex]] of [[free abelian groups]] and $A \in$ [[Ab]] any [[abelian group]], there is a [[long exact sequence]] of the form

$$
  \cdots \to B_n \otimes A \stackrel{i_n \otimes A}{\to} Z_n \otimes A \to H_n(C_\bullet \otimes A) \to B_{n-1} \otimes A \stackrel{i_{n-1}\otimes A}{\to} Z_{n-1} \otimes A \to \cdots
  \,,
$$

where $B_n$ are the [[boundaries]] and $Z_n$ the [[cycles]] of $C_\bullet$ in degree $n$ and where $i_n \colon B_n \hookrightarrow Z_n$ is the canonical inclusion.

=--

+-- {: .proof}
###### Proof

Since, by the [[Dedekind-Nielsen-Schreier theorem]], every [[subgroup]] of a [[free abelian group]] is itself free abelian, such as the subgroup of [[cycles]] $Z_n \hookrightarrow C_n$, it follows that for each $n \in \mathbb{N}$ we have a [[split exact sequence|splitting]] of the [[short exact sequence]] $0 \to Z_n \to C_n \to B_{n-1}$ and hence (as discussed at _[[split exact sequence]]_) a [[direct sum]] decomposition

$$
  C_n \simeq  Z_n \oplus B_{n-1}
  \,.
$$

Here the second direct summand on the right identifies under the differential $\partial^C$ with the [[boundaries]] in one degree lower, since by construction $\partial^C$ is injective on $C_n/Z_n$.


Accordingly, if we regard the graded abelian groups $B_\bullet$ and $Z_\bullet$ as chain complexes with vanishing [[differential]], then we have a sequence of [[chain maps]]

$$
  0 \to Z_\bullet \hookrightarrow C_\bullet \to B_{\bullet-1} \to 0
$$

which is degreewise a [[short exact sequence]], hence is a short exact sequence of chain complexes. Now since the [[tensor product of abelian groups]] distributes over [[direct sum]], the image of this sequence under $(-)\otimes A$

$$
  0 \to Z_\bullet \otimes A \hookrightarrow C_\bullet \otimes A \to B_{\bullet-1} \otimes A \to 0
$$

is still a short exact sequence. The induced [[homology long exact sequence]], as discussed there, is the long exact sequence to be shown.

=--


+-- {: .proof}
###### Proof 
**of theorem \ref{TheoremInOrdinaryHomology}**

By lemma \ref{LongSequenceForHomologyWithCoefficients} we have [[short exact sequences]]

$$
  0 
    \to 
  coker(i_n \otimes A) 
    \to 
  H_n(C_\bullet \otimes A)
    \to 
  ker(i_n \otimes A)
    \to
  0
$$

Since the [[tensor product of abelian groups]] is a [[right exact functor]] it preserves [[cokernels]] and hence 

$$
  coker(i_n \otimes A) \simeq coker(i_n) \otimes A = H_n(C) \otimes A
  \,.
$$

The dual statement were true if $(-)\otimes A$ were also a [[left exact functor]]. In general it is not, and the failure is measure by the [[Tor]]-group: 

Notice that by assumption and by the [[Dedekind-Nielsen-Schreier theorem]] the defining [[short exact sequence]]

$$
  0 \to B_n \stackrel{i_n}{\to} Z_n \to H_n(C_\bullet) \to  0 
$$

exhibits $[\cdots \to 0 \to B_n \to Z_n] \stackrel{\simeq_{qi}}{\to} H_n(C)$ as a [[projective resolution]] of $H_n(C_\bullet)$. Therefore by definition of [[Tor]] the group $Tor_1(H_n(C_\bullet), A)$ is the chain homology in degree 1 of

$$
  [\cdots \to 0 \to B_n \otimes G \stackrel{i_n \otimes A}{\to} Z_n \otimes A]
  \,,
$$

which is

$$
  Tor_1(H_n(C_\bullet), A)
  \simeq
  ker(i_n \otimes A)
  \,.
$$

=--




+-- {: .num_section #sectiona }
=--


### For generalised cohomology theories 
 {#ForGeneralizedCohomology}

The situation for [[generalised cohomology theories]] is much more complicated than that for ordinary cohomology due to the fact that it is harder (or impossible!) to use the tools of [[chain complexes]]. Nonetheless, it is possible to say something. The general case was studied by Adams in [Ada69](#Ada69) (for use in the [[Adams spectral sequence]], see there for more) and the initial version of the rest of this section is heavily based on that treatment.  This was also considered in the slightly later work, [Ada74, Chapter 13](#Ada74). Adams' opening paragraph in [Ada69](#Ada69) is worth quoting in its entirety as motivation for this study.

> It is an established practice to take old theorems about ordinary homology, and generalise them so as to obtain theorems about generalised homology theories. For example, this works very well for duality theorems about manifolds. We may ask the following question. Take all those theorems about ordinary homology which are standard results in every day use. Which are the ones which still lack a fully satisfactory generalisation to generalised homology theories? I want to devote this lecture to such problems.

> *J. F. Adams*{: style="text-align: right"}

The lecture concentrates on the Universal Coefficient Theorem and, as a by-product, the [[Künneth theorem]]. 

Let $E^*$ and $F^*$ be two [[generalized cohomology theories]] and $E_*$ and $F_*$ two [[generalized homology theories]], such that $E$ is [[multiplicative cohomology theory|multiplicative]] and $F$ is a [[module]] over $E$.
Then the general problems that a Universal Coefficient Theorem should apply to are the following:

1. <p></p>
   +-- {: .num_enuma #enumiAa }
   =--
   Given $E_{*}(X)$, calculate $F_{*}(X)$.

2. <p></p>
   +-- {: .num_enuma #enumiAb }
   =--
   Given $E_{*}(X)$, calculate $F^{*}(X)$.

3. <p></p>
   +-- {: .num_enuma #enumiAc }
   =--
   Given $E^{*}(X)$, calculate $F_{*}(X)$.

4. <p></p>
   +-- {: .num_enuma #enumiAd }
   =--
   Given $E^{*}(X)$, calculate $F^{*}(X)$.

In [Ada69](#Ada69), Adams works in a very general setting. On this page, we shall work in a more restricted situation (as spelled out in Note 2 in Adams' lectures). We assume that $E^{*}(-)$ is the [[generalised cohomology theory]] associated to a [[commutative ring spectrum]], $E$. The cohomology theory $F^{*}(-)$ is assumed to come from a left [[module-spectrum]] over $E$, which we shall denote by $F$. We do not assume that $F$ is itself a ring spectrum. Following Adams, we shall also assume that all our cohomology and homology theories are [[reduced cohomology|reduced]].

There are two statements that one would like to hold. These are not themselves theorems, rather the theorem would say ''Under certain conditions, these statements hold''. The statements are the following.

+-- {: .num_uct #ucta .thremark }
###### UCT1

There is a [[spectral sequence]]
$$
\Tor_{p,*}^{E_{*}} (E_{*}(X), F_{*}) \xRightarrow[p]{}    F_{*}(X)
$$
with edge homomorphism
$$
E_{*}(X) \otimes _{E_{*}} F_{*} \to F_{*}(X).
$$
=--

+-- {: .num_uct #uctb .thremark }
###### UCT2

There is a [[spectral sequence]]
$$
\Ext_{E_{*}}^{p,*} (E_{*}(X), F^{*}) \xRightarrow[p]{}    F^{*}(X)
$$
with edge homomorphism
$$
F^{*}(X) \to \Hom_{E_{*}} (E_{*}(X), F^{*}).
$$
=--

For finite [[CW-complexes]] then we can derive two further statements from the above by [[S-duality]]. We use the notation $D X$ for the [[Spanier-Whitehead dual]] of $X$.

For a finite CW-complex $X$, we can apply [UCT1](#ucta) and [UCT2](#uctb) to $D X$ in place of $X$ and then use the various isomorphisms relating the cohomologies of $X$ and $D X$ to reformulate them in terms of $X$. We thus get the following statements.

+-- {: .num_uct #uctc .thremark }
###### UCT3

For $X$ a finite CW-complex, there is a spectral sequence
$$
\Tor_{p,*}^{E^{*}}(E^{*}(X), F^{*}) \xRightarrow[p]{}    F^{*}(X)
$$
with edge homomorphism
$$
E^{*}(X) \otimes _{E^{*}} F^{*} \to F^{*}(X).
$$
=--

+-- {: .num_uct #uctd .thremark }
###### UCT4
For $X$ a finite CW-complex, there is a spectral sequence
$$
\Ext^{p,*}_{E^{*}} (E^{*}(X), F_{*}) \xRightarrow[p]{}    F_{*}(X)
$$
with edge homomorphism
$$
F_{*}(X) \to \Hom^{*}_{E^{*}}(E^{*}(X), F_{*}).
$$
=--

(This is a generalization of the [[Kronecker pairing]], see also e.g. [Schwede 12, prop. 6.20](#Schwede12)).

A particularly important special case of these statements is when we have a [[topological space]], say $Y$, and a [[cohomology theory]], $E^{*}(-)$. Then we define a new homology theory $F_{*}(-)$ by $F_{*}(X) = E_{*}(X \wedge Y)$ and a new cohomology theory $G^{*}(-)$ by $G^{*}(X) = E^{*}(X \wedge Y)$. These are representable, the homology theory by $Y \wedge E$ and the cohomology theory by the function spectrum $F(Y,E)$. Putting these into the statements of the universal coefficient theorem, we obtain similar statements for the [[Künneth theorem]].

+-- {: .num_kt #kta .thremark }
###### KT1
There is a spectral sequence
$$
\Tor_{p,*}^{E_{*}} (E_{*}(X), E_{*}(Y)) \xRightarrow[p]{}    E_{*}(X \wedge Y)
$$
with edge homomorphism
$$
E_{*}(X) \otimes _{E_{*}} E_{*}(Y) \to E_{*}(X \wedge Y).
$$
=--

+-- {: .num_kt #ktb .thremark }
###### KT2
There is a spectral sequence
$$
\Ext_{E_{*}}^{p,*}(E_{*}(X), E^{*}(Y)) \xRightarrow[p]{}    E^{*}(X \wedge Y)
$$
with edge homomorphism
$$
E^{*}(X \wedge Y) \to \Hom_{E_{*}}^{*} (E_{*}(X), E^{*}(Y)).
$$
=--

+-- {: .num_kt #ktc .thremark }
###### KT3
For $X$ a finite CW-complex, there is a spectral sequence
$$
\Tor_{p,*}^{E^{*}} (E^{*}(X), E^{*}(Y)) \xRightarrow[p]{}    E^{*}(X \wedge Y)
$$
with edge homomorphism
$$
E^{*}(X) \otimes _{E^{*}} E^{*}(Y) \to E^{*}(X \wedge Y).
$$
=--

+-- {: .num_kt #ktd .thremark }
###### KT4
For $X$ a finite CW-complex, there is a spectral sequence
$$
\Ext^{p,*}_{E^{*}} (E^{*}(X), E_{*}(Y)) \xRightarrow[p]{}    E_{*}(X \wedge Y)
$$
with edge homomorphism
$$
E_{*}(X \wedge Y) \to \Hom_{E^{*}}^{*} (E^{*}(X), E_{*}(Y)).
$$
=--

The key question is, thus: when do these statements hold? Adams gives some answers in [Ada69](#Ada69).

* If $F_{*}$ is [[flat module|flat]] over $E_{*}$ then [UCT1](#ucta) holds, whence [KT1](#kta) holds if either $E_{*}(X)$ or $E_{*}(Y)$ is flat.

* If $E = S$, the [[sphere spectrum]], then all the results are true.

* If $E$ is a strict [[ring spectrum]] then [KT1](#kta) holds, if also $F$ is a strict [[module spectrum]] over $E$ then [UCT1](#ucta) holds.

* [[Atiyah]] gives a method in [Ati62](#Ati62) for [KT3](#ktc) with $E =$ [[KU]] being complex [[K-theory]] and $X$, $Y$ finite complexes.

#### A Special Case ####

In both [Ada69](#Ada69) and [Ada74](#Ada74), there is a particular focus on the universal coefficient theorem coming from its applications to the [[Adams spectral sequence]].  With that aim in mind, he studies the universal coefficient theorems with considerably strong assumptions.  These assumptions are designed to allow Atiyah's method (from [Ati62](#Ati62)) to work.

+-- {: .num_theorem #assume}
###### Assumption ######
(Condition 13.3 in [Ada74](#Ada74), see also Assumption 20 in [Ada69](#Ada69)).

   The spectrum $E$ is the [[direct limit]] of finite spectra $E_\alpha$ for which $E_*(D E_\alpha)$ is [[projective object|projective]] over $E_*$ and

   $$ 
   F^*(D E_\alpha) \to \Hom^*_{E_*}(E_*(D E_\alpha), F_*)
   $$

   is an isomorphism for all [[module-spectra]] $F$ over $E$.  Here, $D E_\alpha$ is the [[S-dual]] of $E_\alpha$.
=--

The main difference between the two treatments is that in [Ada69](#Ada69), the condition involving $F$ is stated for a *single* module-spectrum, not for *all* module-spectra, and there are alternatives for homology ($F_*(-)$) and cohomology ($F^*(-)$).

In the comments following Assumption 20 in [Ada69](#Ada69), Adams remarks that this is implied by a stronger condition (Proposition 17) on $E$ which makes no reference to $F$.  As $E$ is a ring spectrum, this reduces to:

1. The spectral sequence $H^*(E_\alpha; E^*) \Rightarrow E^*(E_\alpha)$ is trivial, and
2. For each $p$, $H^p(E_\alpha; E^*)$ is projective as an $E^*$-module.

With this assumption, Adams shows the following result:

+-- {: .num_theorem #uctholds}
###### Theorem ######
Let $E$ be a ring spectrum satisfying [the assumption above](#assume).  Let $F$ be a module-spectrum over $E$.  Then \ref{uctb} holds, and the spectral sequence is convergent.
=--

What "convergent" means here is spelled out in [Ada74, Theorem 8.2](#Ada74).

+-- {: .num_cor #uctproj}
###### Corollary ######
Let $E$ be a ring spectrum satisfying [the assumption above](#assume).  Suppose that $E_*(X)$ is projective over $E_*$.  Then the spectral sequence from \ref{uctb} collapses at the $E^2$ term.  That is,
$$
F^*(X) \to \Hom^*_{E_*}(E_*(X),F_*)
$$
is an isomorphism.
=--

In [Ada74](#Ada74), Adams lists several cohomology theories (for $E^*(-)$) where the assumption holds.  These are: $S$, $H\mathbb{Z}_p$, $MO$, $MU$, $MSp$, $K$, $KO$.

#### Freeness and Flatness ####

In [BJW95](#BJW95) and [Boa95](#Boa95) there are various versions of the universal coefficient theorems and K&#252;nneth theorems which are stated and proved (or indications given on how to prove) under assumptions of either [[free module|freeness]] or [[flat module|flatness]].

Here, we shall gather together all the statements made.  In all the following, $E^*(-)$ is a multiplicative generalised cohomology theory with representing ring spectrum $E$.  We use $E_*(-)$ for the associated homology theory.  Following [Boa95](#Boa95) and [BJW95](#BJW95), cohomology and homology are *not* reduced in this section.

+-- {: .num_theorem #homkun}
###### Theorem ([Boa95, 4.2](#Boa95)) ######
Assume that $E_*(X)$ or $E_*(Y)$ is a free or flat $E^*$-module.  Then the pairing:
$$
\times \colon E_*(X) \otimes E_*(Y) \to E_*(X \times Y),
$$
induces the K&#252;nneth isomorphism $E_*(X \times Y) \cong E_*(X) \otimes E_*(Y)$ in homology.
=--

The next result relates homology and cohomology.

+-- {: .num_theorem #strdual}
###### Theorem ([Boa95, 4.14](#Boa95)) ######
Assume that $E_*(X)$ is a free $E^*$-module.  Then $X$ has strong duality, i.e. the duality map $d \colon E^*(X) \to D E_*(X)$ is a homeomorphism between the profinite topology on $E^*(X)$ and the dual-finite topology on $D E_*(X)$.  In particular, $E^*(X)$ is complete Hausdorff.
=--

Combining these two gives the K&#252;nneth theorem for cohomology.

+-- {: .num_theorem #cokun}
###### Theorem ([Boa95, 4.19](#Boa95)) ######
Assume that $E_*(X)$ and $E_*(Y)$ are free $E^*$-modules.  Then we have the K&#252;nneth homeomorphism $E^*(X \times Y) \cong E^*(X) \widehat{\otimes} E^*(Y)$ in cohomology.
=--

There are similar results for spectra.  Boardman, Johnson, and Wilson write reduced homology and cohomology as $E_*(X,o)$ and $E^*(X,o)$, even when $X$ is a spectrum (and so the reduced theories are all that there are).

+-- {: .num_theorem #homkunsp}
###### Theorem ([Boa95, 9.20](#Boa95)) ######
Assume that $E_*(X,o)$ or $E_*(Y,o)$ is a free or flat $E^*$-module.  Then the pairing $\times \colon E_*(X,o) \otimes E_*(Y,o) \to E_*(X \wedge Y,o)$ is an isomorphism in homology.
=--

+-- {: .num_theorem #strdusp}
###### Theorem ([Boa95, 9.25](#Boa95)) ######
Assume that $E_*(X,o)$ is a free $E^*$-module.  Then $X$ has strong duality, i.e. $d \colon E^*(X,o) \to D E_*(X,o)$ is a homeomorphism between the profinite topology on $E^*(X,o)$ and the dual-finite topology on $D E_*(X,o)$.  In particular, $E^*(X,o)$ is complete Hausdorff.
=--

+-- {: .num_theorem #cokunsp}
###### Theorem ([Boa95, 9.31](#Boa95)) ######
Assume that $E_*(X,o)$ and $E_*(Y,o)$ are free $E^*$-modules.  Then the pairing
$$
\times \colon E^*(X,o) \widehat{\otimes} E^*(Y,o) \to E^*(X \wedge Y,o)
$$
induces the cohomology K&#252;nneth homeomorphism.
=--

## Examples

### For singular cohomology 
 {#InTopology}

For $X$ a [[topological space]], write $Sing X$ for its [[singular simplicial complex]] and 

$$
  C_\bullet(X) 
    \coloneqq
  N \mathbb{Z}[Sing X]
$$ 

for the [[normalized chain complex]] of the [[simplicial abelian group]] obtained by forming degreewise the [[free abelian group]].

The _[[singular homology]]_ $H_\bullet(X)$ of $X$ is the [[chain homology]] of $C_\bullet(X)$, and for $A$ some [[coefficient]] [[abelian group]], the [[singular cohomology]] $H^\bullet(X,A)$ is the [[cochain cohomology]], of $C_\bullet(X)$ with coefficients in $A$.

Comparison with the ordinary universal coefficient theorem \ref{OrdinaryStatementInCohomology} shows that:

+-- {: .num_theorem #OrdinaryStatementInTopology}
###### Theorem
**(universal coefficient theorem in topology)**

For $X$ a [[topological space]], $A$ an [[abelian group]] and $n \geq 1 \in \mathbb{N}$, the [[singular homology]] and [[singular cohomology]] of $X$ fit into a [[split exact sequence|split]] [[short exact sequence]] of the form

$$
  0 \to Ext^1(H_{n-1}(X)) \to H^n(X,A) \to Hom_{Ab}(H_n(X), A) \to 0
  \,.
$$

=--


## Related concepts

* [[Künneth theorem]]

* [[bootstrap category]]

## References

### For ordinary (co)homology

An exposition of the universal coefficient theorem for ordinary cohomology and homology is in section 3.1 of

* {#Hatcher} [[Allen Hatcher]], _Algebraic topology_ ([pdf](http://www.math.cornell.edu/~hatcher/AT/AT.pdf)); also [section 3.A](http://www.math.cornell.edu/~hatcher/AT/ATch3.4.pdf).
 


The note

* Adam Clay, _The universal coefficient theorems and K&#252;nneth formulas_ ([pdf](http://www.math.ubc.ca/~aclay/Algtopology.pdf))

surveys and spells out statement and proof of the theorem. A detailed proof of the theorem in cohomology is also in 

* {#Boardman} [[Michael Boardman]], _The universal coefficient theorem_ ([pdf](http://www.math.jhu.edu/~jmb/note/uctcoh.pdf))
 

and a detailed proof of the statement in homology is in section 3 of

* {#Chen} Chen, _Universal coefficient theorem for homology_ ([pdf](http://www.math.uchicago.edu/~may/VIGRE/VIGRE2009/REUPapers/ChenJ.pdf))
 


### For generalized (co)homology
 {#ForGeneralizedCoHomology}

The universal coefficient theorem in [[symmetric smash product of spectra|symmetric monoidal]] [[model categories of spectra]] is discussed in

* [[Anthony Elmendorf]], [[Igor Kriz]], [[Peter May]], section 8 of _[[Modern foundations for stable homotopy theory]]_ ([pdf](http://hopf.math.purdue.edu/Elmendorf-Kriz-May/modern_foundations.pdf))


Universal coefficient theorems for [[generalized homology]] are discussed in 

* [[Friedrich Bauer]], _Remarks on universal coefficient theorems for generalized homology theories_ Quaestiones Mathematicae
Volume 9, Issue 1 & 4, 1986, Pages 29 - 54 

More on the universal coefficient theorem in generalized homology is in:

* {: #Ada69 }  **Ada69** [[John Adams|J. F. Adams]]. Lectures on generalised cohomology. pages 1--138, Berlin, 1969. Springer.

* {: #Ada74 } **Ada74** [[John Adams|J. F. Adams]],  (1974). [[Stable homotopy and generalised homology]]. Chicago, Ill.: University of Chicago Press.

* {: #Ati62 }  **Ati62** [[Michael Atiyah|M. F. Atiyah]]. Vector bundles and the K&#252;nneth formula. Topology, 1:245--248, 1962.

* {: #Boa95} **Boa95** [[J. M. Boardman]],  (1995). Stable operations in generalized cohomology. (pp. 585&ndash;686). Amsterdam: North-Holland.

* {: BJW95} **BJW95** [[J. M. Boardman]], and Johnson, David Copeland and Wilson, W. Stephen. (1995). Unstable operations in generalized cohomology. (pp. 687&ndash;828). Amsterdam: North-Holland.

See also

* {#Schwede12} [[Stefan Schwede]], prop. 6.20 of _[[Symmetric spectra]]_, 2012 ([pdf](http://www.math.uni-bonn.de/~schwede/SymSpec-v3.pdf))

Further discussion along these lines includes

* [[Andrew Baker]], Andrey Lazarev, _On the Adams Spectral Sequence for $R$-modules_, Algebr. Geom. Topol. 1 (2001) 173-199 ([arXiv.0105079](http://arxiv.org/abs/math/0105079))

### For KK-theory
 {#ReferencesForKK}

Discussion for [[KK-theory]] is in 

* [[Jonathan Rosenberg]], Claude Schochet, _The K&#252;nneth theorem and the universal coefficient theorem for Kasparov's generalized K-functor_,  Duke Math. J. Volume 55, Number 2 (1987), 431-474. ([EUCLID](http://projecteuclid.org/euclid.dmj/1077306030))

[[!redirects universal coefficient theorem]]
[[!redirects universal coefficient theorems]]