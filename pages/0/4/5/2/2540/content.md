<div class="rightHandSide toc">
[[!include synthetic differential geometry - contents]]
</div>



#Contents#
* automatic table of contents goes here
{:toc}

#Idea#

Objects $X$ in a [[smooth topos]] $(\mathcal{T}, R)$ 
modelling the axioms of [[synthetic differential geometry]]
have a notion of elements $x,y \in X$ that are [[infinitesimal space|infinitesimally close]] in $X$.

Two elements that are infinitesimally close, denoted $x \sim_1 y$, are called **infinitesimal neighbour**s.

The collection of all elements $x \sim_{(1)} y$ in a [[space]] $X$ with this property forms the space denoted $X_{(1)}$ or $X^{\Delta^1_{inf}}$:  
often called the (first order) _infinitesimal neighbourhood of the diagonal_ in $X$,
where the diagonal meant is the embedding $Id \times Id : X \to X \times X$ of $X$ into the cartesian [[product]] with itself.

**Warning**
Notice that, as usual in a [[topos]], "elements" here always and crucially means
"[[generalized element]]s". For instance 
the notation $x \in X$ denotes a morphism $U \stackrel{x}{\to} X$
for some [[object]] $U$. _Ordinary_ elements in the sense of morphisms from the
[[terminal object]] ${*} \stackrel{x}{\to} X$ typically do not have infinitesimal neighbours.
But they also do not play a single-out role.


# Definition #

As with all concepts in [[synthetic differential geometry]], there is  an abstract definition that depends only on the axioms of a [[smooth topos]]
$(\mathcal{T}, R)$ and then there are the concrete realizations of this abstract definition
in concretely chosen models $(\mathcal{T}, R)$.

In the literature one of the most wide-spread definitions of first order neighbourhoods is actually one that is formulated in a specific model only, namely
to the kind of model studied in [[algebraic geometry]], given by a [[category of sheaves]] on a [[site]] of formal duals of commutative rings. While the construction principle there is quite generic in that 
it works similarly for a wide range of other models, 
for instance when replacing [[ring]]s by [[smooth algebra]]s
and hence [[affine scheme]]s by [[smooth loci]], it is worthwhile to make
the [[category theory|abstract nonsense]] behind it explicit.

In 

* [[Anders Kock]], _Synthetic differential geoemtry_ ([pdf](http://home.imf.au.dk/kock/sdg99.pdf))

this is done for elements in _formal manifolds_ . In the following
we start with an entirely general definition and then look at the
special case that should be the most general situation in which 
the first order neighbourhood has the expected linear properties:
this is the case for [[microlinear space]]s.

## general definition ##

Let $(\mathcal{T},R)$ be a [[smooth topos]]. Write $D = \{x \in R | x^2 = 0 \}$ for the [[infinitesimal space|infinitesimal interval]] in $\mathcal{T}$, the [[equalizer]] 

$$
  D = \lim \left( R \stackrel{\stackrel{(-)^2}{\to}}{\stackrel{0}{\to}}
   R 
  \right)
  \,.
$$
 
For any object $X\in \mathcal{T}$ write $p_{T X} : X^D \to X$ for the [[tangent bundle]] projection induced from the unique ${*} \to D$.

Write

$$
  ev : X^D \times D \to X
$$

for the canonical evaluation map, the [[internal hom]] [[adjunct]] to $Id : X^D \to X^D$.


In full generality one would then like to make the following definition

+-- {: .un_defn}
###### Definition

For $X \in \mathcal{T}$ the infinitesimal neighbourhood of the diagonal of $X$ is the [[image]]

$$
  im\left( 
    X^D \times D \stackrel{p_{T X} p_1 \times ev}{\to}
    X \times X
  \right)
  \,.
$$

=--

The above definition means that an element $(x,y) \in X^{\Delta^1_{inf}}$ is an element $(x,y) \in X \times X$ such that _there exists_

* an infinitesimal curve $v \in X^D$

* an element $\epsilon \in D$

with $v(0) = x$ and $v(\epsilon) = y$.

Or diagrammatically, for $x,y : U \to X$ given over domain of definition $U$, such that there exists a diagram

$$
  \array{
    && X
    \\
    & {}^x\nearrow & \uparrow^{p_{T X} p_1}
    \\
    U &\stackrel{(v,\epsilon)}{\to}& X^D \times D
    \\
    & {}_{y}\searrow & \downarrow^{ev}
    \\
    && X
  }
  \,.
$$


## definition for microlinear spaces ##

Notice that the [[infinitesimal space|infinitesimal interval]] $D$, while not an $R$-[[module]] (it is not closed under addition of its elements in $R$) does have a canonical [[action]] by the [[monoid]] $(R,\cdot)$ which we denote

$$
  \cdot : D \times R \to D
  \,.
$$

Recall that an object $X$ in a [[smooth topos]] is called a [[microlinear space]] if, essentially, the [[tangent bundle]] $p_{T X} : X^D \to X$ has a fiberwise $R$-linear structure.

For $X$ microlinear, there is therefore in oparticular an action

$$
  X^D \times R \to X^D
$$

that on elements is written

$(v,t) \mapsto t \cdot v$, where in turn $t \cdot v$ is the element of $X^D$ characterized by $t \cdot v : \epsilon \mapsto v(t \cdot \epsilon)$.

This means that for $X$ microlinear there is the notion of [[tensor product]] over $R$ of the [[tangent bundle]] with the [[infinitesimal space|infinitesimal interval]] $D$:

$$
  X^D \otimes_R D :=
  \lim_\to
  \left(
    X^D \times R \times D
    \stackrel{\to}{\to}
    X^D \times D
  \right)
  \,.
$$

+-- {: .un_def}
###### Definition

For $X \in \mathcal{T}$ a [[microlinear space]] in a [[smooth topos]] $(\mathcal{T},R)$ write

$$
  X^{\Delta^1_{inf}} := X^D \otimes_R D
  \,.
$$

=--

This means that elements of $X^{\Delta^1_{inf}}$ are equivalence classes of pairs of elements $(v, \epsilon) \in X^D \times D$ where the equivalence relation is $(t\cdot v, \epsilon) \sim (v, t \cdot \epsilon)$ for all $t \in R$.




+-- {: .un_remark}
###### Remark on notation

The notatin $X^{\Delta^1_{inf}}$ is primitive notation and does not denote an [[internal hom]]. It is usefully suggestive, though, in the context of the canonical embedding

$$
  X^{\Delta^1_{inf}} \hookrightarrow X^{\Delta^1_{\mathcal{T}}}
$$

of infinitesimal neighbours regarded as infinitesimal path into all paths.

=--

Let $\Delta^1_{\mathcal{T}}$ be the [[simplex in a lined topos|standard 1-simplex in the smooth topos]] $(\mathcal{T},R)$: as an object this is just $R$. 

### properties ###

Some observations:

* $X^{\Delta^1_{inf}}$ still has a conical $(R,cdot)$-action

* Every morphism $\omega : X^{\Delta^1_{inf}} \to R$ that takes 0-vectors to 0 is $(R,\cdot)$-linear: for all $v : {*} \to X^D$ we have for all $t \in R$ that $\omega(t (v,\epsilon)) = t \omega(v,\epsilon)$.

  **Proof**

  By the nature of the tensor product we may take $R$ as acting only on the $D$-factor. Then for fixed $v \in X^D$ the map in question is

  $$
    D \simeq {*}\times D \stackrel{v \times Id}{\to} 
    X^D \times D \to R
 $$

  which by the [[Kock-Lawvere axiom]] is linear.


* There is a canonical [[monomorphism]]

  $$
    i: 
    X^{\Delta^1_{inf}} \hookrightarrow 
    X^{\Delta^1_{\mathcal{T}}}
  $$

  defined as follows:

  let $f : X^D\\times D \to X^R$ be 
  the [[internal hom]] [[adjunct]] of

  $$
    \bar f : X^D \times D \times R 
    \stackrel{Id times \cdot}{\to}
     X^D \times D
     \stackrel{ev}{\to}
     X
     \,.
  $$

  This $f$ does coequalize the two morphisms $X^D \times R \times D \stackrel{\to}{\to} X^D \times D$ and this way defines $i : X^D \otimes_R D \to X^R$.



## definition for manifolds ##

In particular every [[manifold]] is a [[microlinear space]]. We show that for $X$ a [[manifold]] the object $X^{\Delta^1_{inf}}$ from above coincides with the usual notion.

...

...

See also section I.17 in

* [[Anders Kock]], _Synthetic differential geoemtry_ ([pdf](http://home.imf.au.dk/kock/sdg99.pdf))

...

## definition for loci ##

For spaces defined as formal duals to algebras or rings, there is the standard definition:

let $X = Spec(A)$. Let $J = ker(\cdot : A \otimes A \to A)$ be the ideal of functions on $X \times X$ that vanish on the diagonal. then $X_{(1)} = Spec(A/J^2)$.

...

#Related concepts#


The collection of first order infinitesimal neighbours of a space $X$ arranges itself into the [[schreiber:infinitesimal path ∞-groupoid]] $\Pi^{inf}(X)$. Various concepts derive from this one:

of [[differential form]]s may be understood in terms of functions on $\Pi(x)^{inf}$. This is described at

* [[differential forms in synthetic differential geometry]].

A [[deRham space]] is the colimit over a $\Pi^{inf}(X)$. 


# References #

A detailed discussion of first and higher order neighbourhoods in 
algebraic models is in 

* [[Lawrence Breen]], [[William Messing]], _Combinatorial differential forms_ ([arXiv](http://arxiv.org/abs/math/0005087))
