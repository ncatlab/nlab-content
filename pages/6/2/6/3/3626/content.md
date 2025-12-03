
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


# Frobenius algebra
* table of contents
{: toc}

## Idea
 {#Idea}

A *Frobenius algebra* is a [[vector space]] equipped with the [[structures]] both of an [[algebra]] and of an a [[coalgebra]] in a compatible way, where the compatibility is different from (more "topological" than) that in a [[bialgebra]]/[[Hopf algebra]]:

The *Frobenius property* on an algebra/coalgebra $A$ states that all ways of using $n$ product operations and $m$ coproduct operations to map $A^{\otimes^{n+1}} \to A^{\otimes^{m+1}}$ are equal.

More generally, Frobenius algebras can be defined [[internalization|internal]] to any [[monoidal category]] (and even in any [[polycategory]]) in which case they are sometimes called *Frobenius monoids*.
(For example a Frobenius monoid in an [[endofunctor|endo]]-[[functor category]] is a *[[Frobenius monad]]*.)

After their original introduction in pure [[algebra]] in the 1930s, Frobenius algebras later attracted much attention for the role they play in [[quantum physics]], in fact for two rather different roles they play there:

* **in [[topological quantum field theory]]** Frobenius algebras encode the structure of [[2-dimensional TQFTs]]:

  Here the underlying vector space of the Frobenius algebra is identified (cf. *[[functorial field theory]]*) with the [[space of quantum states]] over a connected 1-manifold (a [[circle]] for the "[[closed string]]" states or a [[closed interval]] for the "[[open string]]" states), the product and coproduct operations are the [[correlators]] on a [[trinion]] [[cobordism]] ("[[pair of pants]]") read in either direction, and the Frobenius property reflects the [[diffeomorphisms]] between [[cobordisms]] obtained by gluing [[trinions]] along their boundary components.

  Beware that this is similar to but subtly different from the "non-compact" [[2d TQFTs]] commonly known as the "[[topological string]]" (the [[A-model]] and the [[B-model]] of [[mirror symmetry]]-fame) which are *not* described by Frobenius algebras (because here one ex-cludes the "cap" cobordism and thus the [[trace]]-operation hence the finite-dimensionality on the algebra of states) but by "[[Calabi-Yau objects]]" (for more see *[here](TCFT#Definition)* at *[[TCFT]]*.)

  On the other hand, the [[FRS-theorem]] shows that all *[[rational 2d conformal field theories]]* -- hence the compact-target-space sectors of the *physical* [[string]] (such as [[WZW models]] and [[Gepner models]]) -- *are* described by [[Frobenius monoids]] [[internalization|internal]] to [[modular tensor categories]] (MTCs): Here the ambient MTC encodes the local non-topological ("chiral") component of the [[conformal field theory]] (its spaces of [[conformal blocks]]) while the internal Frobenius monoid encodes the remaining topological "[[sewing constraints]]".

Later
  
* **in [[quantum information theory]]** (such as now in the [[ZX-calculus]]) Frobenius algebras encode aspects of the [[quantum measurement]]-process, including its associated [[wavefunction collapse]] (see [here](quantum+information+theory+via+dagger-compact+categories#MeasurementReferencesQuantumInformationTheoryViaStringDiagrams) at *[[quantum information theory via dagger-compact categories]]*).

  One way to understand how this comes about (not the original way, though) is to observe that in the [[linear type theory]] which is relevant for [[quantum information theory]] the [[reader monad]] and [[coreader comonad]] for a given [[finite set]] $W$ of [[possible worlds|possible]] measurement outcomes merge to a single [[Frobenius monad]] (the *[[quantum reader monad]]*, see there for more) which is in turn identified with the [[writer monad]]/[[cowriter comonad]] for a canonical Frobenius algebra structure on the [[linear span]] of $W$.

Curiously, these two different roles that Frobenius algebras play in [[quantum physics]] are not closely related, in fact they seem somewhat orthogonal to each other.





## Definition

There are a number of equivalent definitions of the concept of Frobenius algebra.

The original definition is an associative algebra with a suitable [[linear form]] on it.

* [As an associative algebra with linear form](#AsAssociativeAlgebraWithLinearForm).

In the context of [[2d TQFT]] what crucially matters is that this is equivalent to an associative algebra structure with a compatible coalgebra structure

* [As an associative algebra with compatible coalgebra structure](#AlgebraCoalgebra).

There are

* [Further equivalent definitions](#FurtherDefinition)


### As associative algebra with coalgebra structure
 {#AlgebraCoalgebra}

\begin{definition}\label{FrobeniusAlgebra}
A *Frobenius algebra* [[internalization|in]] a [[monoidal category]] $(\mathcal{C}, \otimes, \mathbb{1})$ (for instance [[Vect]] with the usual [[tensor product of vector spaces]]) is

1. an [[object]] $A$ 

1. [[morphisms]] 

   * ([[unit]]) $\eta \,\colon\, \mathbb{1} \to A$, 

   * ([[counit]]) $\epsilon \,\colon\, A \to \mathbb{1}$, 

   * ([[multiplication]]) $\mu \,\colon\, A \otimes A \to A$.  

   * ([[comultiplication]]) $\delta \,\colon\, A \to A \otimes A$,

such that:

1. $(A, \mu, \eta)$ is a [[monoid]] (an [[associative algebra]] when $\mathcal{C} = Vect$),

1. $(A, \delta, \epsilon)$ is a [[comonoid]] (a [[coassociative coalgebra]] when $\mathcal{C} = Vect$),

1. the **Frobenius laws** hold: $(id_A \otimes \mu) \circ (\delta \otimes id_A) = \delta \circ \mu = (\mu \otimes id_A) \circ (id_A \otimes \delta)$.

\end{definition}

In terms of [[string diagrams]], Def. \ref{FrobeniusAlgebra} says:

[[frobenius_algebra.jpg:pic]]

The first line here shows the associative law and left/right unit laws for a [[monoid]].  The second line shows the coassociative law and left/right counit laws for a [[comonoid]].  The third line shows the Frobenius laws.

In fact, although this seems rarely to be remarked, the two Frobenius laws can be replaced by the single axiom $(1 \otimes \mu) \circ (\delta \otimes 1) = (\mu \otimes 1) \circ (1 \otimes \delta)$.  Here is a proof in string diagram notation that this axiom implies $(1 \otimes \mu) \circ (\delta \otimes 1) = \delta \circ \mu$ (taken from [Pastro-Street 2008](#PastroStreet2008)):

[[frobenius_axioms_one_to_two.png:pic]]

Here the first and fifth steps use the counitality property of the comonoid structure, the second and fourth steps use the assumed axiom (once in each direction), and the third step uses coassociativity.


### As associative algebra with linear form
 {#AsAssociativeAlgebraWithLinearForm}

Frobenius algebras were originally formulated in the category [[Vect]] of [[vector spaces]] with the following equivalent definition:

+-- {: .num_defn}
###### Definition

A **Frobenius algebra** is a [[unitality|unital]], [[associative algebra]] $(A, \mu, \eta)$ equipped with a [[linear form]] $\epsilon \colon A \rightarrow k$ -- to becalled a **Frobenius form** -- such that $\epsilon \circ \mu$ is a non-degenerate [[inner product]]. I.e. the induced morphism

\[  
  u 
  \;\mapsto\; 
  \big(
    v \mapsto \epsilon \circ \mu(v \otimes u)
  \big) 
\]

is an [[isomorphism]] of $V$ with its [[dual vector space|dual space]] $V^*$. 

=--

From this definition it is easy to see that every Frobenius algebra [[internalization|in]] [[Vect]] is necessarily [[finite-dimensional vector space|finite-dimensional]].

### Further definitions
 {#FurtherDefinitions}

There are about a dozen equivalent definitions of a Frobenius algebra. [Ross Street (2004)](#Street2004) lists most of them.

## Types of Frobenius algebras

### Commutative Frobenius algebras ###

We can define 'commutative' Frobenius algebras in any [[symmetric monoidal category]].  Namely, a Frobenius algebra is **commutative** if its associated monoid is commutative --- or equivalently, if its associated comonoid is cocommutative.  

### Symmetric Frobenius algebras ###

We can define 'commutative' or 'symmetric' Frobenius algebras in any [[symmetric monoidal category]].  A Frobenius algebra $A$ is **symmetric** if 
$$\epsilon \mu \circ S_{A,A} = \epsilon \mu \, $$
where $S_{A,A} : A \otimes A \to A \otimes A$ is the symmetry, and $\epsilon\mu$ is the nondegenerate pairing induced as above from the multiplication and the counit.  Any commutative Frobenius algebra is symmetric, but not conversely: for example the algebra of $n \times n$ matrices with entries in a field, with its usual trace as $\epsilon$, is symmetric but not commutative when $n \gt 1$.  

A theorem of [Eilenberg & Nakayama (1955)](#Eilenberg1955) says that in the category [[Vect]] of [[vector spaces]] over a [[field]] $k$, an algebra $A$ can be equipped with the structure of a symmetric Frobenius algebra if (but not only if) it is **[[separable algebra|separable]]**, meaning that for any field $K$ [[field extension|extending]] $k$, $A \otimes_k K$ is a [[semisimple algebra|semisimple]] algebra over $K$.   

### Special Frobenius algebras


\begin{definition}
\label{SpecialFrobeniusAlgebras}

The term "special Frobenius algebra" is not used consistently in the literature, but the main point is to require that the product is the [[left inverse]] to the coproduct, possibly up to a non-vanishing element $\beta_A$ in the [[ground field]]:

\[
  \label{ProdLeftInverseToCoprodUpToScaling}
  prod \circ coprod \,=\, \beta_A \cdot id
\]

This condition removes the [[genus of a surface|genus]]-contribution in normal forms of "connected maps", up to rescaling, see [below](#NormalFormAndSpiderTheorem).

But then it is natural to also require the counit to be left inverse to the unit, up to (another) non-vanishing ground field element $\beta_1$:

\[
  \label{CounitLeftInverseToUnitUpTOScaling}  
  counit \circ unit \,=\, \beta_1 \cdot id
\]

which also removes the disconnected "vaccum"-contribution, up to scaling.

The two conditions (eq:ProdLeftInverseToCoprodUpToScaling) and (eq:CounitLeftInverseToUnitUpTOScaling) on a Frobenius algebra are taken to be the definition of "special Frobenius" in [Fuchs, Runkel & Schweigert 2002, Def. 3.4 (i)](#FRS-theorem+on+rational+2d+CFT#FuchsRunkelSchweigert02):

\begin{imagefromfile}
    "file_name": "FRS-SpecialFrobeniusDiagram.jpg",
    "width": 400,
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 10, 
        "left": 10
    }
\end{imagefromfile}

However, other authors take the condition for "special Frobenius" to be the single constraint that 

\[
  \label{CoprodLetfInverseToProd}
  prod \circ coprod \,=\, id
\]

(eg. [Coecke & Pavlović 2008, p. 17](quantum+information+theory+via+dagger-compact+categories#CoeckePavlović08), [Fauser 2012, Def. 3.7](https://arxiv.org/abs/1202.6380))

and may instead call (eq:ProdLeftInverseToCoprodUpToScaling) the condition to be *trivially connected*.

Beware that both of these conventions are adhered to by no small number of authors.
\end{definition}

In the category of vector spaces, any element $a$ of an associative unital algebra gives a left multiplication map 
$$ \array{ 
L_a : &A &\to& A \\
      &b &\mapsto& a b 
}
$$
which in turn gives a bilinear pairing $g: A \times A \to k$ defined by
$$ g(a,b) = tr(L_a L_b) $$
One can show that the algebra $A$ can be equipped with the structure of a special Frobenius algebra if and only if $g$
is nondegenerate, i.e., if there is an isomorphism $A \to A^*$ given by
$$ a \mapsto g(a, -)  $$
In this case, there is just one way to make $A$ into a special Frobenius algebra, namely by taking the counit to be 
$$ \epsilon(a) = tr(L_a) $$
(In any Frobenius algebra, the unit, multiplication and counit determine the comultiplication.)  

In fact, all the results of the previous paragraph generalize to Frobenius algebras in any symmetric monoidal category, since the proofs can be done using string diagrams.  

An associative unital algebra for which the bilinear pairing $g$ is nondegenerate is called **strongly separable**.  So, any strongly separable algebra becomes a special Frobenius algebra in a unique way.  For more details, see [[separable algebra]] and [Aguiar (2000)](#Aguiar2000).

To get a feeling for some of the concepts we are discussing, an example is helpful.  The group algebra $k[G]$ of a finite group $G$ is always separable but strongly separable if and only if the order of $G$ is invertible in the field $k$.  By the results mentioned, this means that $k[G]$ can always be made into a symmetric Frobenius algebra, but only into a special Frobenius algebra when $|G|$ is invertible in $k$.

To see this, we can check that the group algebra $k[G]$ becomes a symmetric Frobenius algebra if we define the counit $\epsilon: k[G] \to k$ to pick out the coefficient of $1 \in G$:
$$   \epsilon : \sum_{g \in G} a_g \, g \mapsto a_1 \,. $$
But when $|G|$ is invertible in $k$, we can check that $k[G]$ becomes a _special_ symmetric Frobenius algebra if we normalize the counit as follows:
$$  \epsilon : \sum_{g \in G} a_g \, g \mapsto \frac{a_1}{|G|} \, .$$

We should warn the reader that [Rosebrugh et al (2005)](#Rosebrugh2005) call a special Frobenius algebra 'separable'. This usage conflicts with the standard definition of a [[separable algebra]] in the category of vector spaces over a field, so we suggest avoiding it.

### &#8224;-Frobenius algebras ###

If a Frobenius algebra lives in a monoidal [[†-category]], $(\delta)^\dagger = \mu$ and $(\epsilon)^\dagger = \eta$, then it is said to be a **&#8224;-Frobenius algebra**. These crop up in the theory of 2d [[TQFTs]], and also in the foundations of [[quantum mechanics in terms of dagger-compact categories|quantum theory]]. Symmetric dagger Frobenius monoids internal to $\mathrm{FHilb}$ can be classified by [[H-star-algebra | $H^*$-algebras]].

## Examples
 {#Examples}


\begin{example}
\label{VectorSpaceWithLinearBasis}
\linebreak
For $W \,\in\,$ [[FiniteSets]], the $W$-fold [[direct sum]] 
$\mathrm{Q}W \equiv \underset{W}{\oplus} \mathbb{1}$ of the [[ground field]] $\mathbb{1}$ -- with its inherited [[direct sum]]-[[associative algebra]]-[[structure]] -- becomes a [[Frobenius algebra]] by taking the

* [[counit]] to be the canonical [[sum]]-operation;

* [[coproduct]] to be map induced by the [[diagonal]] on indices.

In components, if we choose the canonical [[linear basis]]
$$
  \mathrm{Q}W
  \;\simeq\;
  Span
  \Big(
    \big\{
      \left\vert w \right\rangle
    \big\}_{w \colon W}
  \Big)
$$
then on basis vectors these structure maps are expressed as follows (where "$\delta$" is the [[Kronecker delta]]):

\begin{tikzcd}[sep=0pt]
  \mathbb{K}
  \ar[rr, "{ \mathrm{unit} }"]
  &&
  \mathrm{Q}W
  \\
  1 &\mapsto& 
  \sum_{w} \left\vert w \right\rangle
\end{tikzcd}

\begin{tikzcd}[sep=0pt]
  \mathrm{Q}W
  \otimes 
  \mathrm{QW}
  \ar[rr, "{ \mathrm{prod} }"]
  &&
  \mathrm{Q}W
  \\
  \left\vert w, \, w' \right\rangle
  &\mapsto&
  \delta_w^{w'}
  \,
  \left\vert w \right\rangle
\end{tikzcd}

\begin{tikzcd}[sep=0pt]
  \mathrm{Q}W
  \ar[rr, "{ \mathrm{coprod} }"]
  &&
  \mathrm{Q}W
  \otimes
  \mathrm{Q}W
  \\
  \left\vert w \right\rangle
  &\;\mapsto\;&
  \left\vert w,\, w \right\rangle
\end{tikzcd}

\begin{tikzcd}[sep=0pt]
  \mathrm{Q}W
  \ar[rr, "{ \mathrm{counit} }"]
  &\;\;&
  \mathbb{K}
  \\
  \left\vert w \right\rangle
  &\mapsto&
  1
\end{tikzcd}

In these components, the Frobenius property is this equation:


\begin{tikzcd}[sep=0pt]
  \mathrm{Q}W
  \otimes
  \mathrm{Q}W
  \ar[
    rrrr, 
    "{ \mathrm{id} \,\otimes\, \mathrm{coprod} }"  
  ]
  \ar[
    dddd, 
    "{ 
      \mathrm{coprod} \,\otimes\, \mathrm{id} 
    }"{description}
   ]
  &&&&
  \mathrm{Q}W
  \otimes
  \mathrm{Q}W
  \otimes
  \mathrm{Q}W
  \ar[
    dddd, 
    "{ 
      \mathrm{prod} \,\otimes\, \mathrm{id} 
    }"{description}
  ]
  \\
  &
  \left\vert w,\, w'\right\rangle
  &\mapsto&
  \left\vert w,\, w',\, w' \right\rangle  
  \\
  &
  \rotatebox[origin=c]{-90}{$\mapsto$}
  &&
  \rotatebox[origin=c]{-90}{$\mapsto$}
  \\
  &
  \left\vert w,\, w,\, w' \right\rangle
  &\mapsto&
  \delta_{w}^{w'}
  \left\vert w,\, w' \right\rangle
  \\
  \mathrm{Q}W 
  \otimes
  \mathrm{Q}W 
  \otimes
  \mathrm{W}W
  \ar[
    rrrr, 
    "{ 
      \mathrm{id} \,\otimes\, \mathrm{prod} 
    }"{swap}
  ]
  &&&&
  \mathrm{Q}W 
  \otimes
  \mathrm{Q}W
\end{tikzcd}

Elementary as this example may be, it embdies some important principles:

For $\mathbb{K} \,=\, \mathbb{C}$ the [[complex numbers]], the corresponding [[Frobenius monad]] $\mathrm{Q}W \otimes (\text{-}) \,\colon\, \mathbb{C}Mod \to \mathbb{C}Mod$ (or rather $\mathrm{Q}W \otimes (\text{-}) \,\colon\, FinDimHilb \to FinDimHilb$) has been proposed &lbrack;[Coecke & Pavlović 2008](quantum+measurement#CoeckePavlović08)&rbrack; to reflect aspects of [[quantum measurement]] in the context of [[quantum information via dagger-compact categories]] and is used as such in the *[[zxCalculus]]* (where the Frobenius property is embodied by "spider diagrams"). Various authors discuss the Frobenius algebras $\mathrm{Q}W$ in this context, see the references [there](quantum+information+theory+via+dagger-compact+categories#MeasurementReferencesQuantumInformationTheoryViaStringDiagrams).

From another perspective on the same phenomenon (discussed at *[[quantum circuits via dependent linear types]]*): The $\mathrm{Q}W$-[[writer monad]] underlying the [[Frobenius monad]] $\mathrm{Q}W \otimes (-) \,\colon\, \mathbb{K}Mod \to \mathbb{K}Mod$ is a linear version of the [[reader monad]], as such discussed at *[[quantum reader monad]]*. Regarded as a [[monad in computer science|computational effect]] its [[Kleisli morphisms]] encode [[quantum gates]] with an "indefiniteness"-effect (in the sense of [quantum modal logic](necessity+and+possibility#ModalQuantumLogic)) whose "[handling](monad+in+computer+science#MonadModulesInIdeaSection)" is the process of [[quantum measurement]].

In particular, the [[algebra over a monad|algebras]] (hence also the corresponding [[coalgebra over a comonad|coalgebras]]) over $\mathrm{Q}W \otimes (\text{-})$ the [[dependent linear types|$W$-dependent $\mathbb{K}$-linear types]], namely the $\mathbb{K}$-[[vector bundles]] over $W$, hence the $W$-[[indexed sets]] of $\mathbb{K}$-[[vector spaces]], understood as residual [[spaces of quantum states]] after [[quantum state collapse|collapse]] following the measurement result $w \in W$.
\end{example}



## Properties 

### General


+-- {: .num_prop}
###### Proposition 
A Frobenius algebra $A$ in a [[monoidal category]] is an [[dual object|object dual]] to itself. 
=-- 

+-- {: .proof}
###### Proof 
Let $I$ be the [[monoidal unit]]. To say $A$ is dual to itself means there are maps $e: I \to A \otimes A$ and $p: A \otimes A \to I$ such that the [[triangle identities]] hold. The maps are defined by 
$$e = (I \stackrel{\eta}{\to} A \stackrel{\delta}{\to} A \otimes A), \qquad p = (A \otimes A \stackrel{\mu}{\to} A \stackrel{\epsilon}{\to} I)$$ 
and one of the [[triangle identities]] uses one of the Frobenius laws and unit and counit axioms to derive the following [[commutative diagram]]: 

$$\array{
A & \stackrel{1 \otimes \eta}{\to} & A \otimes A & \stackrel{1 \otimes \delta}{\to} & A \otimes A \otimes A \\
 & {}_1\searrow & \downarrow \mathrlap{\mu} & & \downarrow \mathrlap{\mu \otimes 1} \\
 & & A & \overset{\delta}{\to} & A \otimes A \\
 & &  & {}_{1}\searrow & \downarrow \mathrlap{\epsilon \otimes 1} \\
 & & & & A
} 
$$ 

The other [[triangle identity]] uses the other Frobenius law and unit and counit axioms.
 
=-- 

As a result, we see that in the monoidal category [[Mod|$Mod_k$]] of [[modules]] over a [[commutative ring]] $k$, Frobenius algebras $A$ considered as modules over $k$ are [[finitely generated module|finitely generated]] and [[projective module|projective]]. This is because $A \otimes_k -$, being [[adjoint functor|adjoint]] to itself, is a [[left adjoint]] and [[left adjoints preserve colimits|therefore preserves all colimits]]. That $A \otimes_k -$ preserves arbitrary small coproducts means $A$ is finitely generated over $k$, and that $A \otimes_k-$ preserves coequalizers means $A$ is projective over $k$. 

* Every Frobenius algebra $A$ is a [[quasi-Frobenius algebra]]: projective and injective left (right) modules over $A$ coincide. 

* Every Frobenius algebra $A$ is a [[pseudo-Frobenius algebra]]: $A$ is an injective cogenerator in the category of left (right) $A$-modules. 

Frobenius algebras are closely connected with [[ambidextrous adjunctions]]. For example, a **[[Frobenius monad]]** on a category $C$ is by definition a Frobenius monoid in the monoidal category of [[endofunctors]] on $C$ (with monoidal product given by endofunctor composition), and if we have a pair of [[adjunctions]] $F \dashv U$ and $U \dashv F$, then $M = U F$ carries a monad structure and a [[comonad]] structure and the Frobenius laws are satisfied, a fact most easily seen by using [[string diagrams]].  


### PROPs for Frobenius algebras

Certain kinds of Frobenius algebras have nice [[PROPs]] or [[PRO|PROs]].  The PRO for Frobenius algebras is the monoidal category of planar thick tangles, as noted by [Lauda (2006)](#Lauda2006) and illustrated here:

[[frobenius_algebra.jpg:pic]]


Lauda and Pfeiffer [Lauda (2008)](#Lauda2008) showed that the PROP for _symmetric_ Frobenius algebras is the category of 'topological open strings', since it obeys this extra axiom:

[[symmetric_frobenius_algebra_law.jpg:pic]]

The PROP for _commutative_ Frobenius algebras is [[2Cob]], as noted by many people and formally proved in [Abrams (1996)](#Abrams96).  This means that any commutative Frobenius algebra gives a 2d [[TQFT]].  See [Kock (2006)](#Kock2006) for a history of this subject and [Kock (2004)](#Kock2004) for a detailed introduction.  In 2Cob, the circle is a Frobenius algebra.  The monoid laws look like this:

[[monoid_laws.jpg:pic]]

The comonoid laws look like this:

[[comonoid_laws.jpg:pic]]

The Frobenius laws look like this:

[[frobenius_laws.jpg:pic]]

and the commutative law looks like this:

[[commutative_law.jpg:pic]]

The PROP for _special_ commutative Frobenius algebras is Cospan(FinSet), as proved by Rosebrugh, Sabadini and Walters.  This is worth comparing to the PROP for commutative [[bialgebra|bialgebras]], which is Span(FinSet).  For details, see [Rosebrugh et al (2005)](#Rosebrugh2005), and also [Lack (2004)](#Lack2004).  

A special commutative Frobenius algebra gives a 2d TQFT that is insensitive to the genus of a 2-manifold, since in terms of pictures, the 'specialness' axioms $m \circ \delta = 1$ says that

[[special_law.jpg:pic]]




### Classification of 2d TQFT
 {#RelationTo2DTQFT}

[[!include 2d TQFT -- table]]



### Normal form and "Spider theorem"
 {#NormalFormAndSpiderTheorem}

\begin{proposition}
**(normal form for 2d cobordisms)**
\linebreak
Every *[[connected topological space|connected]]* [[cobordism]] with

* $n_{in} \gt 0$ ingoing boundary components

* $n_{out} \gt 0$ outgoing boundary components

* [[genus of a surface|genus]]$\;$ $g$

is equivalent ([[diffeomorphism|diffeomorphic]]) to the [[composition]] of 

* $n_{in}-1$ [[trinions]] regarded as $S^1 \times S^1 \to S^1$

* $g$ 2-punctured [[tori]] $S^1 \to S^1$

* $n_{out}-1$ [[trinions]] regared as $S^1 \to S^1 \times S^1$,

\begin{imagefromfile}
    "file_name": "Abrams-2dCobordismNormalForm.jpg",
    "width": 600,
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 10, 
        "left": 10
    },
    "caption": "(from [Abrams 1996, Fig. 3](#Abrams96))"
\end{imagefromfile}


as shown in the following example for 

* $n_{in} = 5$

* $g = 4$

* $n_{out} = 4$


\begin{imagefromfile}
    "file_name": "2dCObordismNormalForm.jpg",
    "width": 600,
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 10, 
        "left": 10
    },
    "caption": "(from [Kock 2004, p. 64](#Kock2004))"
\end{imagefromfile}

\end{proposition}
This is discussed in [Abrams 1996, Prop. 12](#Abrams96); [Kock 2004, §1.4.16](#Kock2004).

By the [relation](#RelationTo2DTQFT) between 2d cobordism and Frobenius algebras this means equivalently that:

\begin{corollary}\label{NormalFormForFrobeniusMaps}
**(normal form for Frobenius maps)**
\linebreak
Given a Frobenius algebra

$$
  \big(
    A 
    ,\,
    unit
    ,\,
    counit
    ,\,
    prod
    ,\,
    coprod
  \big)
$$

then every linear map of the form

$$
  A^{\otimes^{n_{in}}}
  \longrightarrow
  A^{\otimes^{n_{out}}}
$$

which is 

1. entirely the composite of the algebra's structure maps, ie. of the (co)unit and the (co)product, 

1. *connected*, in that it does not decompose as a tensor product of such morphisms,

is equal to the composite, in this order, of

* $n_{in}-1$ copies of $prod$

* some number ($g$) of copies of $prod \circ coprod$

* $n_{out}-1$ copies of $coprod$.
  
\end{corollary}

\begin{corollary}\label{SpiderTheorem}
**(Spider theorem)**
\linebreak
If the Frobenius algebra in Cor. \ref{NormalFormForFrobeniusMaps} is *special* in that $prod \circ coprod = id$ (eq:CoprodLetfInverseToProd) then every linear map of the form
$$
  A^{\otimes^{n_{in}}}
  \longrightarrow
  A^{\otimes^{n_{out}}}
$$

which is 

1. entirely the composite of the algebra's structure maps, ie. of the (co)unit and the (co)product, 

1. *connected* in that it does not decompose as a tensor product of such morphisms,

is equal to the composite, in this order, of

* $n_{in}-1$ copies of $prod$

* $n_{out}-1$ copies of $coprod$.

\end{corollary}



\begin{imagefromfile}
    "file_name": "FrobNormalFormAsSpiderRule.jpg",
    "float": "right",
    "width": 500,
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 10
    },
    "caption": "From [Cocke & Duncan 2011](quantum+information+theory+via+dagger-compact+categories#CoeckeDuncan11)"
\end{imagefromfile}

The "spider theorem" (Cor. \ref{SpiderTheorem}) is called this way in [Coecke & Duncan 2008, Thm. 1](quantum+information+theory+via+dagger-compact+categories#CoeckeDuncan08) (it appears unnamed also in [Coecke & Paquette 2008, p. 6](quantum+information+theory+via+dagger-compact+categories#CoeckePaquette08)) and shares its name with the corresponding "spider diagrams" used in the [[ZX-calculus]] for [[quantum computation]] (where the Frobenius algebras that appear are those that realize the [[quantum reader monad]] as a [[Frobenius monad|Frobenius]] [[writer monad]]/[[cowriter comonad]]).



### Frobenius algebras in polycategories

In fact, Frobenius algebras can be defined in any [[polycategory]], and hence in any [[linearly distributive category]].  The essential point is that the monoidal structure used for the monoid structure could be different from the monoidal structure used for the comonoid structure, i.e. we could have $\mu:A\otimes A \to A$ but $\delta :A \to A \parr A$.  The compatibility between $\otimes$ and $\parr$ in a linearly distributive category (or between their "[[multicategory|multicategorical]]" analogues in a polycategory) is precisely what is required to write down the composites involved in the Frobenius laws.  For instance, we can have

$$ A\otimes A
\xrightarrow{1_A \otimes \delta}
A \otimes (A \parr A)
\xrightarrow{lin-distrib}
(A \otimes A) \parr A
\xrightarrow{\mu \parr 1_A}
A\parr A
$$

and one of the Frobenius laws says that this composite is equal to

$$ A \otimes A \xrightarrow{\mu} A \xrightarrow{\delta} A\parr A. $$

This is analogous to how a [[bimonoid]] can be defined in any [[duoidal category]].  In fact, it is a sort of [[microcosm principle]]; it is shown in [(Egger2010)](#Egger2010) that Frobenius monoids in the linearly distributive category [[Sup]] are precisely [[star-autonomous category|*-autonomous]] cocomplete [[posets]] (and hence, in particular, linearly distributive).

In polycategorical language we can give another [[unbiased]] definition of a  commutative Frobenius monoid: it is equipped with exactly one morphism $\overset{n}{\overbrace{(A,A,\dots,A)}} \to \overset{m}{\overbrace{(A,A,\dots,A)}}$ of each possible (two-sided) arity, such that any (symmetric) polycategorical composite of two such morphisms is equal to another such.  The monoid structure consists of the morphisms of arity $(2,1)$ and $(0,1)$, while the comonoid structure is the morphisms of arity $(1,2)$ and $(1,0)$, and the Frobenius relations say that three ways to compose these to produce a morphism of arity $(2,2)$ are equal.  (The morphism of arity $(0,0)$ is the composite $\epsilon\eta$; no axiom is required on it, because in a polycategory there is no other morphism $()\to ()$ to compare it to.)  In other words, the free symmetric polycategory containing a commutative Frobenius monoid is the [[terminal object|terminal]]  symmetric polycategory.  In this way Frobenius algebras are to polycategories in the same way that monoids are to multicategories.

## Related concepts

* [[Calabi-Yau algebra]]

* [[hypergraph category]]

* [[Frobenius pseudomonoid]]

* [[Frobenius monad]]

[[!include reader-writer (co)monads -- table]]


## References ##

Frobenius algebras were introduced by [[Brauer]] and Nesbitt and were named after [[Ferdinand Frobenius]].

See for instance

* {#Eilenberg1955} [[Samuel Eilenberg]], [[Tadasi Nakayama]], _On the dimension of modules and algebras. II. Frobenius algebras and quasi-Frobenius rings_, _Nagoya Math. J._ **9** (1955) 1-16 &lbrack;[doi:10.1017/S0027763000023229](https://doi.org/10.1017/S0027763000023229)&rbrack;

* [[Marcelo Aguiar]] (2000), _A note on strongly separable algebras_, Bolet&#237;n de la Academia Nacional de Ciencias (C&#243;rdoba, Argentina), special issue in honor of Orlando Villamayor, **65**, 51--60.  ([pdf](http://www.math.cornell.edu/~maguiar/strongly.pdf))
{#Aguiar2000}

* [[Andrew Baker]], _Frobenius algebras_ 2010 ([pdf](http://www.maths.gla.ac.uk/~ajb/dvi-ps/Frobenius-talk.pdf))

On the role of Frobenius algebras in [[2d TQFT]]:

* {#Abrams96} [[Lowell Abrams]], *Two-dimensional topological quantum field theories and Frobenius algebra*, Jour. Knot. Theory and its Ramifications **5**, 569-587 (1996) &lbrack;[doi:10.1142/S0218216596000333](https://doi.org/10.1142/S0218216596000333), [ps](http://home.gwu.edu/~labrams/docs/tqft.ps)&rbrack;

* {#BaezTWF} [[John Baez]], This Week's Finds in Mathematical Physics, [week268](http://math.ucr.edu/home/baez/week268.html) and [week299](http://math.ucr.edu/home/baez/week299.html).

* {#Kock2004} [[Joachim Kock]], *Frobenius Algebras and 2d Topological Quantum Field Theories*, Cambridge U. Press (2004) &lbrack;[doi:10.1017/CBO9780511615443](https://www.cambridge.org/core/books/frobenius-algebras-and-2d-topological-quantum-field-theories/A6438118DFADFD27175779F1FC0FF7CB), [webpage](http://mat.uab.cat/~kock/TQFT.html), [course notes pdf](http://mat.uab.es/~kock/TQFT/FS.pdf), [[Kock-FrobAlgTQFT-short.pdf:file]]&rbrack;

* {#Kock2006} [[Joachim Kock]], Remarks on the history of the Frobenius equation (2006) &lbrack;[web](http://mat.uab.es/~kock/TQFT.html#history)&rbrack;

* {#Lauda2006} [[Aaron Lauda]]: *Frobenius algebras and ambidextrous adjunctions*, Theory and Applications of Categories **16** 4 (2006) 84-122 &lbrack;[tac:16-04](http://tac.mta.ca/tac/volumes/16/4/16-04abs.html), [arXiv:math/0502550](http://arxiv.org/abs/math/0502550)&rbrack; 
  > (relating to [[ambidextrous adjunctions]] and [[Frobenius monads]])

* {#Lauda2008} [[Aaron Lauda]], [[Hendryk Pfeiffer]], Open-closed strings: two-dimensional extended TQFTs and Frobenius algebras, _Topology Appl._ **155** (2005) 623-666 &lbrack;[arXiv:0510664](http://arxiv.org/abs/math/0510664), [doi:10.1016/j.topol.2007.11.005](https://doi.org/10.1016/j.topol.2007.11.005)&rbrack;


For applications in proof theory of classical and [[linear logic]] or linguistics:

* [[Martin Hyland]],  _Abstract Interpretation of Proofs: Classical Propositional Calculus_, pp. 6-21 in Marcinkowski, Tarlecki (eds.),  _Computer Science Logic (CSL 2004)_, LNCS **3210** Springer Heidelberg 2004. ([preprint](https://www.dpmms.cam.ac.uk/~jmeh1/Research/Publications/2004/aap04.pdf))

* [[Richard Garner]], _Three investigations into linear logic_ , PhD report  Cambridge 2006. ([pdf](http://comp.mq.edu.au/~rgarner/Thesis/Smith-Knight-Essay.pdf))

* D. Kartsaklis, M. Sadrzadeh, S. Pulman,  [[Bob Coecke]], _Reasoning about meaning in natural language with compact closed categories and Frobenius algebras_ (2014). ([arXiv:1401.5980](https://arxiv.org/abs/1401.5980))

Frobenius algebras in [[linearly distributive categories]]:

* {#Egger10} [[Jeff Egger]]: *The Frobenius relations meet linear distributivity*, Theory and Applications of Categories **24**2 (2010) &lbrack;[tac:24-2](http://tac.mta.ca/tac/volumes/24/2/24-02abs.html)&rbrack;
  

See also

* [[Aurelio Carboni]]: *Matrices, relations, and group representations*, Journal of Algebra **136** 2 (1991) 497--529 &lbrack;<a href="https://doi.org/10.1016/0021-8693(91)90057-F">doi:10.1016/0021-8693(91)90057-F</a>&rbrack;

* [[Bertfried Fauser]], _Some Graphical Aspects of Frobenius Structures_,  preprint (2012).  [arXiv:1202.6380](http://arxiv.org/pdf/1202.6380v1) 

* {#Lack2004} [[Stephen Lack]] (2004), Composing PROPs, _Theory and Applications of Categories_ **13**, 147--163.  ([web](http://www.tac.mta.ca/tac/volumes/13/9/13-09abs.html))

* [[F. W. Lawvere]], _Ordinal Sums and Equational Doctrines_, pp. 141-155 in Eckmann (ed.), _Seminar on Triples and Categorical Homology Theory_, LNM **80** Springer Heidelberg 1969. ([TAC Reprint of vol. 80](http://www.tac.mta.ca/tac/reprints/articles/18/tr18.pdf)) 

* {#PastroStreet2008} Craig Pastro and [[Ross Street]], _Weak Hopf monoids in braided monoidal categories_, 2008, [arXiv:0801.4067](https://arxiv.org/abs/0801.4067)

* {#Rosebrugh2005} R. Rosebrugh, N. Sabadini and R.F.C. Walters (2005), Generic commutative separable algebras and cospans of graphs, _Theory and Applications of Categories_ **15** (Proceedings of CT2004), 164--177.  ([web](http://www.tac.mta.ca/tac/volumes/15/6/15-06abs.html))

* {#Street2004} [[Ross Street]] (2004), Frobenius monads and pseudomonoids, _J. Math. Phys._ **45**.  ([doi:10.1063/1.1788852](https://doi.org/10.1063/1.1788852))

* R. F. C. Walters, R. J. Wood, _Frobenius objects in Cartesian cicategories_, TAC **20** no. 3 (2008) 25--47. ([pdf](http://www.tac.mta.ca/tac/volumes/20/3/20-03.pdf))


category: algebra

[[!redirects Frobenius algebra]]
[[!redirects Frobenius algebras]]
[[!redirects Frobenius monoid]]
[[!redirects Frobenius monoids]]
