> under construction


#Contents#
* automatic table of contents goes here
{:toc}


## Idea

An object in an [[(∞,1)-topos]] $\mathbf{H}$ over an [[(∞,1)-site]] $C$ may be regarded as an [[∞-groupoid]] modeled on $C$. A cosimplicial commutative algebra, i.e an object in $\mathbf{L} := (Alg_k^{\Delta})^{op}$, may be regarded as a [[Lie-∞-algebroid]].

If $\mathbf{H}$ is equipped with an [[adjoint (∞,1)-functor|adjunction]]

$$
  \mathbf{H} \stackrel{\overset{\mathcal{O}}{\to}}{\overset{Spec}{\leftarrow}}
  \mathbf{L}
$$

the [[(∞,1)-functor]] $\mathcal{O}$ acts like $\infty$-Lie differentiation. Combined with the canonical adjunction

$$
  \mathbf{H} \stackrel{\overset{LConst}{\leftarrow}}{\overset{\Gamma}{\to}}
  \infty Grpd
$$

this induces a notion of Lie theory on bare $\infty$-groupoids. For suitable choices of $\mathbf{H}$ and $\mathcal{O}$, this turns out to be essentially [[rational homotopy theory]].

## Definition

Let $\mathbf{H}$ be an [[(∞,1)-category of (∞,1)-sheaves|(∞,1)-sheaf]] [[(∞,1)-topos]].

Let $k$ be a [[field]] of characteristic 0 and $\mathbf{L} := (Alg_k^{\Delta})^{op}$ the [[(∞,1)-category]] of [[cosimplicial object|cosimplicial]] unital _commutative_ algebras over $k$, with weak equivalences given by [[quasi-isomorphism]]s under the [[monoidal Dold-Kan correspondence]] $Alg_k^\Delta \simeq dgAlg^+$.

Or more generally, let $\mathbf{L} = ((Alg_k^{\Delta^{op}})^\Delta)^{op}$ be the category of cosimplicial simplicial algebra, which under monoidal Dold-Kan identifies with unbounded [[dg-algebra]]s.

We may think of $\mathbf{L}$ as the category of (derived) [[L-∞-algebroid]]s, as described there.

Say that a **global function algebra**  or **Chevalley-Eilenberg algebra** structure on $\mathbf{H}$ is an [[adjoint (∞,1)-functor|(∞,1)-adjunction]]

$$
  (\mathcal{O} \dashv Spec) \;\; :\;\;
  \mathbf{H} \stackrel{\overset{\mathcal{O}}{\to}}{\overset{Spec}{\leftarrow}}
  \mathbf{L}
  \,.
$$

Recall also the terminal [[geometric morphism]] of [[(∞,1)-topos]]es

$$
  (LConst \dashv \Gamma) \;\; : \;\;
  \mathbf{H}
  \stackrel{\overset{LConst}{\leftarrow}}{\overset{\Gamma}{\to}}
  \infty Grpd
  \,,
$$

where $\Gamma : \mathbf{H} \to$ [[∞Grpd]]  is the [[global section]]s functor and for $X \in \infty Grpd$ we have that $LConst_X$ is the [[constant ∞-stack]] of [[locally constant ∞-stack]]s on $X$.

We then have the composite functors

$$
  \Omega^\bullet(-)
  :
  \infty Grpd \stackrel{LConst}{\to} \mathbf{H} \stackrel{\mathcal{O}}{\to}
  \mathbf{L}
$$

and

$$
  |-|
  :
  \mathbf{L} \stackrel{Spec}{\to} \mathbf{H} \stackrel{\Gamma}{\to}
  \infty Grpd
$$

and the rationalization 

$$
  X \mapsto |\Omega^\bullet(X)|
  \,.
$$

## Examples

### On formal duals of algebras

Let $C = (Alg_k)^{op}$ with the [[fpqc-topology]] and $\mathbf{H} = Sh_{(\infty,1)}(C) = (sPSh(C)_{loc})^\circ$. Write $k \in sPSh(C)_{loc}$ for the line object. 

+-- {: .un_prop }
###### Proposition

The functors $\mathcal{O} := Hom_{sPsh(C)}(-,k) : sPSh(C) \to (Alg_k^{\Delta})^{op}$ and $Spec : A \mapsto (Alg_k^\Delta)^{op}(\mathcal{O}(-),A)$ form an [[sSet]]-[[enriched category theory|enriched]] [[Quillen adjunction]]

$$
  (\mathcal{O} \dashv Spec) : sPSh(C)_{loc} \stackrel{\leftarrow}{\to}
  (Alg_k^\Delta)^{op}
  \,.
$$

=--

This appears as [To, prop. 2.2.2](http://arxiv.org/PS_cache/math/pdf/0012/0012219v6.pdf#page=44).

+-- {: .proof}
###### Proof

It is easily seen that we have a Quillen adjunction with respect to the global model structure on $sPSh(C)_{glob}$. Since $sPSh(C)_{loc}$ arises by [[Bousfield localization of model categories|left Bousfield localization]] at [[hypercover]]s, it suffices to show that $Spec$ sends fibrant object of $(Alg_k^\Delta)^{op}$ to simplicial presheaves that satisfy [[descent]] at hypercovers. But for this it suffices to observe that for $Y \to U$ a [[hypercover]], the $k$-cohomology of $Y$ is isomorphic to that of $U$, so that $\mathcal{O}(Y) \leftarrow \mathcal{O}(X)$ is a [[quasi-isomorphism]]: we need to check that

$$
  sPSh(Y, Spec A) \to sPSh(X,Spec A) 
$$

is an equivalence, which this is adjunct to

$$
  (Alg^\Delta)^{op}(\mathcal{O}(Y), A) \to (Alg^\Delta)^{op}(\mathcal{O}(X),A)
  \,.
$$

Since every object in $(Alg^{\Delta})^{op}$ is cofibrant and since $A$ is furthermore fibrant, this is the hom of a weak equivalence between cofibrant objects into a fibrant object and [[derived hom space|hence]] a weak equivalence.
 
=--

+-- {: .un_remark }
###### Remark

This proof works very generally whenever hypercovers $Y \to U$ over representables induce isomorphisms in $R$-cohomology as seen by the line object $R$.

=--

### On formal duals of simplicial algebra

Let now $C = $ [[simplicial algebra]]s ${}^{op}$. Then...

... essentially as above, see [Ben-Zvi/Nadler](http://arxiv.org/abs/1002.3636)

### On formal duals of smooth algebra

Let now $C = $ [[smooth loci]]. Then...

...(essentially as above, see [[schreiber:Chevalley-Eilenberg algebra]]).

## References


The [[Quillen adjunction]]

$$
  (\mathcal{O} \dashv Spec) : 
  sPSh((Alg_kop))_{loc} \stackrel{\leftarrow}{\to}
  (Alg_k^{\Delta})^{op}
$$

was considered in

* [[Bertrand Toen]], _Affine stacks (Champs affines)_ ([arXiv:math/0012219](http://arxiv.org/abs/math/0012219)) .

Its generalization to 

$$
  Sh_{(\infty,1)}((dgAlg_k^-)^{op})
  \stackrel{\leftarrow}{\to}
  (dgAlg_k)^{op}
$$

with $(dgAlg_k)^{op}$ the [[(∞,1)-site]] of non-positively graded cochain [[dg-algebra]]s is discussed in 

* [[David Ben-Zvi]], [[David Nadler]], _Loop Spaces and Connections_ ([arXiv:math/1002.3636](http://arxiv.org/abs/1002.3636))

Comments on the generalization from plain algebras to [[smooth algebra]]s are at

* [[Urs Schreiber]], _[[schreiber:Chevalley-Eilenberg algebra]]_

[[!redirects rational homotopy theory in an (∞,1)-topos]]