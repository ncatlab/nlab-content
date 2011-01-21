
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohesive $\infty$-Toposes
+--{: .hide}
[[!include cohesive infinity-toposes - contents]]
=--
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Definition

+-- {: .un_def}
###### Definition

Let [[CartSp]]${}_{synthdiff}$ be the [[full subcategory]] of the category of [[smooth loci]] on those objects of the form $\mathbb{R}^n \times D$ for $n \in \mathbb{N$ and $D$ an [[infinitesimal space]]: the formal dual of a Weil algebra.

Equip this category with the [[coverage]] where a family of morphisms in is [[covering]] precisely if it is of the form $\{U_i \times D \stackrel{(f_i, Id_D)}{\to} U \times D\}$ for $\{f_i : U_i \to U\}$ a covering in [[CartSp]]$()_{smooth}$ (a [[good open cover]]).

=--

This appears as ([Kock, (5.1)]{#Kock}). 

+-- {: .un_remark}
###### Remark

The [[sheaf topos]] over [[CartSp]]${}_{synthdiff}$ is [[equivalence of categories|equivalent]] to the [[Cahiers topos]].

=--

+-- {: .un_def}
###### Definition

We say the [[(∞,1)-topos]] of **synthetic differential $\infty$-groupoids** is the [[(∞,1)-category of (∞,1)-sheaves]]

$$
  SynthDiff \infty Grpd := Sh_{(\infty,1)}(CartSp_{synthdiff})
$$

on $CartSp_{synthdiff}$. 

=--

Since $ThCartSp$ is an [[∞-cohesive site]], this is a [[cohesive (∞,1)-topos]]. We may think of its (concrete) objects as being [[∞-groupoid]]s equipped with [[smooth structure]] in the fashion of [[Models for Smooth Infinitesimal Analysis|standard models]] of [[synthetic differential geometry]].

Therefore we call an object in $SynthDiff \infty Grpd$ a **synthetic differential $\infty$-groupoid**.

By restriction along the morphism of sites [[CartSp]]${}_{smooth}\to$[[CartSp]]${}_{synthdiff}$ every synthetic differential $\infty$-groupoid has an underlying [[smooth ∞-groupoid]].


## Properites


### Cohesiveness over $\infty Grpd$

+-- {: .un_prop}
###### Proposition

$SynthDiff \infty Grpd$ is a [[cohesive (∞,1)-topos]].

=--

+-- {: .proof}
###### Proof

Because [[CartSp]]${}_{synthdiff}$ is an [[∞-cohesive site]]. See there for details.

=--


### Cohesiveness over  $Smooth \infty Grpd$

+-- {: .un_def}
###### Definition

Write $i : CartSp_{smooth} \hookrightarrow CartSp_{synthdiff}$

for the canonical [[full subcategory|embedding]].

=--

+-- {: .un_prop}
###### Proposition

The [[(∞,1)-geometric morphism]] induced by the [[morphism of sites]] $i$ exhibits $SynthDiff \infty Grpd$ as a [[cohesive (∞,1)-topos]] over [[Smooth∞Grpd]]

$$
 (\Pi_{inf} \dashv Disc_{inf} \dashv \Gamma_{inf} \dashv coDisc_{inf})
  SynthDiff \infty Grpd
   \stackrel{\overset{i_!}{\to}}{\stackrel{\overset{i^*}{\leftarrow}}{\stackrel{\overset{i_*}{\to}}{\underset{i^!}{\leftarrow}}}}
  Smooth \infty Grpd
  \,.
$$

=--



+-- {: .proof}
###### Proof

Observe that $i$ has a [[right adjoint]] $p : CartSp_{synthdiff} \to CartSp_{smooth}$ given by the projection $p : U \times D\mapsto U $. This exhibits $CartSp_{smooth}$ as a [[coreflective subcategoy]]

$$
  (i \dashv p ) : CartSp_{synthdiff} 
   \stackrel{\overset{i}{\leftarrow}}{\underset{p}{\to}}
  CartSp_{smooth}
  \,.
$$


As before, we present the $(\infty,1)$-toposes in question by the <a href="http://ncatlab.org/nlab/show/model+structure+on+simplicial+presheaves#LocalizationAtCoverage">Left Bousfield localization at the coverage</a> $[C^{op}, sSet]_{proj,cov}$ of the global projective [[nLab:model structure on simplicial presheaves]].

We start by _defining_ 

$$
  LConst_{inf} := (-) \circ p : [C^{op}, sSet] \to [C_{th}^{op}, sSet]
$$ 

as given by precomposition with $p : C_{th} \to C$. To see that this is correct, we check that its [[nLab:right adjoint]] is indeed the functor 

$$
  \Gamma_{inf} = (-)\circ i : [C^{op}_{th}, sSet] \to [C^{op}, sSet]
$$

given by precomposition with $i$, i.e. indeed the [[nLab:direct image]] induced by the morphism of sites given by $i$.

To check this, use that this right adjoint is given by the right [[nLab:Kan extension]] $Ran_p$ along $p$

$$
  Ran_p F : U \mapsto 
  {\lim_{\leftarrow}}_{(p(V_{th}) \to U) \in (p\downarrow U)} F(V_{th})
  \,,
$$

where the [[nLab:limit]] is taken over the [[nLab:comma category]].

Now we observe that by the fact that $(i \dashv p)$ is a [[nLab:reflective subcategory|coreflective embedding]] the inclusion functor

$$
  inc : C/U = (Id_C \downarrow U) \to (p \downarrow U)
$$

of the [[nLab:overcategory]] into the [[nLab:comma category]] given by

$$
  inc : (W \to U) \mapsto ( p(i(W)) \stackrel{\simeq}{\to} W \to U)
$$

is a [[nLab:final functor]]: for all $p(V_{th}) \to U$ in $p\downarrow U$ the [[nLab:comma category]] $(p(V_{th} \to U)) \downarrow inc$ is evidently non-emty (it contains the object given by the counit $p(V_{th}) \stackrel{\simeq}{\to} p i p (V_{th})  $ ) and connected: for any two objects 

$$
  \array{
     p(i(W_1)) &\leftarrow& p(V_{th}) &\to& p(i(W_2))
     \\
     &\searrow& \downarrow & \swarrow
     \\
     && U
  }
$$

a connecting zig-zag can be taken to be

$$
  \array{
     && p i p (V_{th})
     \\
     & \swarrow &\uparrow^{\mathrlap{\simeq}}& \searrow
     \\
     p(i(W_1)) &\leftarrow& p(V_{th}) &\to& p(i(W_2))
     \\
     &\searrow& \downarrow & \swarrow
     \\
     && U
  }
  \,.
$$

By the basic characteristic of [[nLab:final functor]]s, it follows that the [[nLab:limit]] over $(p \downarrow U)$ that constructs the right Kan extension $Ran_p F$ at $U \in C$ is equivalently computed by its restriction along $inc$ as

$$
  (Ran_p F)(U)
  \simeq
  {\lim_{\leftarrow}}_{(W \to U) \in C/U} F(W)
  \,.
$$

But this is the formula for right Kan extension along the identity, so we have

$$
  (Ran_p F)(U) = F(U)
$$

(this is [[nLab:Yoneda reduction]]). So $Ran_p = (-) \circ i$ is simply given by restricting along $i$, which is the [[nLab:direct image]] operation inuced by the morphism of sites $i : C \to C_{th}$.

So far we have established 

$$
  (LConst_{inf} \dashv \Gamma_{inf})
  =
  ((-) \circ p \dashv (-) \circ i)
  :
  [C_{th}^{op}, sSet]
  \stackrel{\leftarrow}{\to}
  [C^{op}, sSet]
  \,.
$$


The functor $\Gamma_{inf}$ trivially preserves fibrations and acyclic fibrations of $[C_{th}^{op}, sSet]_{proj}$, hence $LConst_{inf}$ preserves cofibrations and acyclic cofibrations of $[C^{op}, sSet]_{proj}$. Since moreover $C \hookrightarrow C_{th}$ preserves covering families, $\Gamma_{inf}$ sends fibrant objects in $[C_{th}^{op}, sSet]_{proj,cov}$ to fibrant objects in $[C^{op}, sSet]_{proj,cov}$. Once again with [[nLab:Quillen adjunction|HTT, corollary A.3.7.2]] this implies that we have a [[nLab:Quillen adjunction]]

$$
  (LConst_{inf} \dashv \Gamma_{inf})
  :
  [C_{th}^{op}, sSet]_{proj,cov} 
    \stackrel{\overset{LConst_{inf}}{\leftarrow}}{\underset{\Gamma_{inf}}{\to}}
  [C^{op}, sSet]_{proj,cov} 
    \,.
$$

Now consider the [[nLab:left adjoint]] of $LConst_{inf}$ given by left [[nLab:Kan extension]] along $p$

$$
  \Pi_{inf} = Lan_p : [C_{th}^{op}, sSet] \to [C^{op}, sSet]
  \,.
$$

which we write in [[nLab:coend]] notation as

$$
  Lan_p A : U \mapsto 
  \int^{V_{th} \in C_{th}}
   Hom_{C}(U, p(V_{th})) \cdot A(V_{th})
  \,.
$$

With the [[nLab:co-Yoneda lemma]] we see that $\Pi_{inf}$ takes all the representable presheaves from $C_{th}$ to their underlying objects in $C$: it contracts away all the infinitesimal extensions of representable present in a simplicial presheaf on $C_{th}$ (just as the finite path $\infty$-groupoid functor $\Pi$ contracted away entirely the representables inside a simplicial presheaf).


It is clear that $LConst_{inf}$ preserves fibrations and global acyclic fibrations in $[C^{op}, sSet]_{proj}$, so $\Pi_{inf}$ preserves cofibations in $[C_{th}^{op}, sSet]_{proj}$ and therefore in $[C_{th}^{op}, sSet]_{proj, cov}$.

By the assumption that also $p$ preserves covering families, it follows that
$LConst_{inf}$ also sends fibrant objects of $[C^{op}, sSet]_{proj,cov}$ to fibrant objects in $[C_{th}^{op}, sSet]_{proj,cov}$. So one more time with [[nLab:Quillen adjunction|HTT, corollary A.3.7.2]] it follows that we also have a [[nLab:Quillen adjunction]]

$$
  (\Pi_{inf} \dashv LConst_{inf})
  : 
  [C_{th}^{op}, sSet]_{proj,cov}
  \stackrel{\overset{\Pi_{inf}}{\to}}{\underset{LConst_{inf}}{\leftarrow}}
  [C^{op}, sSet]_{proj,cov}
  \,.
$$


=--


+-- {: .un_remark}
###### Remark

From the above proof and since in $sPSh(C)$ [[nLab:commutativity of limits and colimits|colimits commute with products]], we have that for $j(U \times \mathbb{L}W)$ a representable presheaf in $sPSh(CartSp_{th})$ that

$$
  \Pi_{inf}(j(U \times \mathbb{L}W))
  = j(U) \times (colim_{CartSp_{th}} j(\mathbb{L}W))
  = j(U)
  \,,
$$

using again that the colimit over a representable functor is the point. This means that on a Dugger-cofibrant replacement in $sPSh(CartSp_{th})$ of some object $X$ as a degreewise coproduct of representables

$$
  X \stackrel{\simeq}{\leftarrow}
  \hat X 
  :=
  \int^{[n]}
  \Delta[n]
  \cdot
  \coprod_{i_n} U_{i_n} \times \mathbb{L}W_{i_n}
$$

the functor $\Pi_{inf}$ acts by discarding all the infinitesimal thickenings:

$$
  \Pi_{inf} \hat X
  Red(\hat X)
  :=
  \int^{[n]}
  \Delta[n]
  \cdot
  \coprod_{i_n} U_{i_n} 
  \,.
$$

In particular this is hence the action of the $\infty$-categorical left [[nLab:derived functor|derived]] functor of $\Pi_{inf}$

* $\Pi$ contracts all contractible local parts of $X$ to the point;

* $\Pi_{inf}$ contracts all _infinitesimal_ local parts of $X$ to the point.

=--



(...)


## Structures

We discuss what some of the general abstract <a href="http://ncatlab.org/nlab/show/cohesive+(infinity%2C1)-topos#Structures">Structures in a cohesvive (∞,1)-topos</a> look like in the model $SynthDiff \infty Grpd$.

### Concrete objects {#StrucConcreteObjects}

(...)

### Geometry and structure sheaves {#StrucGeometry}

(...)

### Cohesive $\infty$-groups {#StrucInfinGroups}

(...)

### Cohomology and principal $\infty$-bundles {#StrucCohomology}

(...)

### Concordance {#StrucConcordance}

(...)

### Geometric homotopy and Galois theory {#StrucGeometricHomotopy}

(...)

### van Kampen theorem {#StrucVanKampen}

(...)

### Paths and geometric Postnikov towers {#StrucPaths}

(...)


### Universal coverings and geometric Whitehead towers {#StrucWhitehead}

(...)


### Flat $\infty$-connections and local systems {#StrucFlat}

(...)

### de Rham cohomology {#StrucDeRham}

(...)


### $\infty$-Lie algebras {#StrucLieAlg}

(...)


### Maurer-Cartan forms and curvature characteristic forms {#StrucCurvatureForms}

(...)

### Differential cohomology {#StrucDifferentialCohomology}

(...)


### Chern-Weil homomorphism and $\infty$-connections {#StrucChernWeil}

(...)

### Higher holonomy and Chern-Simons functional {#StrucChernSimons}

(...)


## References

Section 3.4 of 

* [[Urs Schreiber]], _[[schreiber:differential cohomology in a cohesive topos]]_

The site [[CartSp]]${}_{synthdiff}$ is discussed in section 5 of

* [[Anders Kock]], _Convenient vector spaces embed into the Cahiers topos_ ([numdam](http://www.numdam.org/item?id=CTGDC_1986__27_1_3_0)).


[[!redirects synthetic differential ∞-groupoid]]

[[!redirects SynthDiff∞Grpd]]