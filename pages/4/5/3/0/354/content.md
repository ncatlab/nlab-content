#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The notion of a Kan complex is an abstraction of the structure found in the [[singular simplicial complex]] of a topological space. 

A Kan complex is a [[geometric definition of higher category|geometric model]] of an $\infty$-[[infinity-groupoid|groupoid]] based on the [[geometric shapes for higher structures|shape]] modeled by the [[simplex category]].

A Kan complex is a collection of $k$-[[simplex]]-shaped [[k-morphism]]s for all $k \in \mathbb{N}$, such that for all composable $k$-morphisms a composite does exist (not necessarily uniquely) and  such that all $k$-morphisms are invertible under this composition.

In a Kan complex there are no _specified_ composites. But one may _choose_ out for all composable $k$-morphisms a composite and thus arrive at an [[algebraic definition of higher category|algebraic model]] for $\infty$-groupoids: [[algebraic Kan complex]]es.

## Definition

A _Kan complex_ is a [[simplicial set]] $S$ that satisfies the _Kan condition_, 

* which says that all [[horn|horns]] of the simplicial set have _fillers_,

* which means equivalently that the unique morphism $S \to pt$ from $S$ to the [[point]] is a [[Kan fibration]], 

* which means equivalently that for all diagrams

  $$
  \array{
    \Lambda^i[n] &\to& S
    \\
    \downarrow && \downarrow
    \\
    \Delta[n] &\to& pt
  }
  \;\;\;
  \leftrightarrow
  \;\;\;
  \array{
    \Lambda^i[n] &\to& S
    \\
    \downarrow && 
    \\
    \Delta[n] 
  }
  $$
  there exists a diagonal morphism
  $$
  \array{
    \Lambda^i[n] &\to& S
    \\
    \downarrow &\nearrow& \downarrow
    \\
    \Delta[n] &\to& pt
  }
  \;\;\;
  \leftrightarrow
  \;\;\;
  \array{
    \Lambda^i[n] &\to& S
    \\
    \downarrow &\nearrow& 
    \\
    \Delta[n] 
  }
  \,.
  $$

* This in turn means equivalently that the map from $n$-simplices to $(n,i)$-horns is an [[epimorphism]]
$$
  [\Delta[n], S]\, \twoheadrightarrow \,[\Lambda^i[n],S]
  \,.
$$

  In this last form the Kan condition is useful 
  for defining [[internalization|internal]] Kan 
  complexes: for instance a _smooth Kan complex_ can 
  be defined as a simplicial object in [[Diff]] 
  such that the morphisms
  $
    [\Delta[n], S] \to [\Lambda^i[n],S]
  $
  are _surjective submersions_.



## Remarks


* Kan complexes are among the most convenient and popular models for [[∞-groupoids]]. The horn filling condition from this point of view is read as guaranteeing that

  * for all collection of $(n-1)$ composable $n$-cells (a horn $\Lambda^k[n]$) there exists an $n$-cell -- their _composite_ -- and an $(n-1)$-cell connecting the original $(n-1)$ $n$-cells with their composite. Depending on $k$, this interpretation in terms of composition implies that one thinks of all cells as being reversible. Therefore this models an [[∞-groupoid]].

  For illustrations of the horn-filler conditions see [[Kan fibration]].


* Whatever other definition of [[∞-groupoid]] one considers, it is expected to map to a Kan complex under the [[nerve]].

* A slight weakening of the Kan condition, the _weak Kan condition_ leads to the definition of [[quasi-category]].

* Kan complexes are the fibrant objects in the [[model structure on simplicial sets|model structures on simplicial sets]] for which fibrations are [[Kan fibration|Kan fibrations]].

  In this context, a weak equivalence between Kan complexes is a morphism of simplicial sets that induces an [[isomorphism]] on the [[simplicial homotopy groups]] of the two Kan complexes.

## Examples

### Kan complexes from nerves of $n$-groupoids 

+-- {: .un_prop}
###### Proposition

The [[nerve]] $N(C)$ of a [[small category]] 
is a Kan complex if and only if $C$ is a [[groupoid]].

=--

The existence of [[nLab:inverse|inverse]] morphisms in $D$ corresponds to the fact that in the [[Kan complex]] $N(D)$ the "outer" [[horns]]

$$
  \array{
    && d_0
    \\
    & && \searrow^{f}
    \\
    d_1 &&\stackrel{Id_{d_1}}{\to} && d_1
  }
  \;\;\; 
  \;\;\; 
  and
  \;\;\; 
  \;\;\; 
  \array{
    && d_1
    \\
    & {}^f\nearrow &&     
    \\
    d_0 &&\stackrel{Id_{d_0}}{\to} && d_0
  }
$$

have fillers 

$$
  \array{
    && d_0
    \\
    & {}^{f^{-1}}\nearrow&& \searrow^{f}
    \\
    d_1 &&\stackrel{Id_{d_1}}{\to} && d_1
  }
  \;\;\; 
  \;\;\; 
  and
  \;\;\; 
  \;\;\; 
  \array{
    && d_1
    \\
    & {}^f\nearrow && \searrow^{f^{-1}}
    \\
    d_0 &&\stackrel{Id_{d_0}}{\to} && d_0
  }
$$

(even unique fillers, due to the properties of the [[nerve]] of an ordinary category).

This is one way to see and motivate that a simplicial set that is a [[Kan complex]] but which does not necessarily have unique fillers makes models an [[∞-groupoid]].

Accordingly

+-- {: .un_prop}
###### Proposition

The [[nerve]] $N(C)$ of a [[strict ∞-category]] 
is a Kan complex if and only if $C$ is a [[strict ∞-groupoid]].

=--


### Singular simplicial complexes / fundamental $\infty$-groupoids

For $X$ a [[topological space]], its _singular simplicial complex_ is the [[simplicial set]] $\Pi(X)$ (often denoted  $S(X)$) whose set of $n$-simplices is the [[hom-set]]

$$
  \Pi(X)_n := Top(\Delta^n_{Top}, X)
$$

in [[Top]] of continuous maps from the standard topological $n$-simplex $\Delta^n_{Top}$ into $X$.

Using the fact that the $\Delta^n_{Top}$ arrange themselves into a [[simplicial object|cosimplicial space]]

$$
  \Delta_{Top} : \Delta \to Top
$$

in the obvious way, the $(\Pi(X)_n)$ become a [[simplicial set]] in the corresponding obvious way. For instance the face maps are induced by restricting maps to $X$ along the face inclusions $\delta^i : \Delta^{n-1} \hookrightarrow \Delta^n$.

That $\Pi(X)$ is indeed a Kan complex is intuitively clear. Technically it follows from the fact that the inclusions ${{\Lambda^n}_{Top}}_k \hookrightarrow \Delta^n_{Top}$ of topological horns into topological simplices are 
[[retracts]], in that there are continuous maps $\Delta^n_{Top} \to {{\Lambda^n}_{Top}}_k$ given by "squashing" a topological $n$-simplex onto parts of its boundary, such that
$$
  ({{\Lambda^n}_{Top}}_k \to \Delta^n_{Top} \to
  {{\Lambda^n}_{Top}}_k)
  =
  Id
  \,.
$$
Therefore the map
$[\Delta^n, \Pi(X)] \to [\Lambda^n_k,\Pi(X)]$ is an epimorphism, since it is equal to 
to $Top(\Delta^n, X) \to Top(\Lambda^n_k, X)$ which has a right inverse $Top(\Lambda^n_k, X) \to Top(\Delta^n, X)$.


The [[∞-groupoid]] represented by the Kan complex $\Pi(X)$ is called the [[fundamental ∞-groupoid]] of $X$.

This example is the universal one: up to [[model structure on simplicial sets|weak equivalence of Kan complexes]] every Kan complex is the fundamental $\infty$-groupoid of a (compactly generated, weakly Hausdorff) [[topological space]].

This is the statement of the [[homotopy hypothesis]] (which is a theorem for $\infty$-groupoids modeled as Kan complexes.

## How to think of Kan complexes as $\infty$-groupoids {#AsGrpds}

We expand here a bit on how a Kan complex may naturally be thought of as an [[∞-groupoid]]: a [[higher category theory|higher category]] in which all [[k-morphism]]s for all $k \in \mathbb{N}$ are invertible.

For this interpretation, one thinks of a $k$-dimensional cell $\phi \in C_K$ of a Kan complex $C$ as a [[k-morphism]] whose 

* _source_ is the $(k-1)$-morphism given by the pasting diagram of the $(k-1)$-cells that are the faces $d_{k} \phi, \; d_{k-2} \phi, d_{k-4} \phi \cdots$  of $\phi$;

* _target_ is the $(k-1)$-morphism given by the pasting diagram of the $(k-1)$-cells that are the faces $d_{k-1} \phi, \; d_{k-3} \phi, d_{k-5} \phi \cdots$  of $\phi$

where $d_i : C_k \to C_{k-1}$ are the [[simplicial identities|face maps]] of the [[simplicial set]] $C$.

This is easy to see in low dimensions: 

* a 1-cell $\phi \in C_1$ in the [[simplicial set]] $C$ has a single source 0-cell $x := d_1 \phi$ and a single target 0-cell $y := d_0 \phi$ and hence may be pictured as a [[morphism]]

  $$
    x \stackrel{\phi}{\to} y
    \,.
  $$

* a 2-cell $\phi \in C_2$ in the [[simplicial set]] $C$ has two incoming 1-cells $d_2 \phi, d_0 \phi \in C_1$ and one outgoing 1-cell $d_1 \phi \in C_1$, and if we think of the two incoming 1-cells as representing the composite of the corresponding 1-morphisms, we may picture te 2-cell $\phi$ here as a globular 2-morphism

  $$
    \array{
      && x_1
      \\
      & {}^{\mathllap{d_2 \phi}}\nearrow &\Downarrow^\phi& \searrow^{\mathrlap{d_1 \phi}}
      \\
      x_0 &&\underset{d_1 \phi}{\to}&& x_2
    }
    \,.
  $$

More in detail, one may think of the incoming two adjacent $1$-cells here as _not_ being the composite of these two morphism, but just as a [[composable pair]], and should think of the existence of the 2-morphism $\phi$ here as being a **compositor** in a [[bicategory]] that shows how the composable pair is composed to the morphism $d_1 \phi$.

So if an $\infty$-groupoid is thought of as a [[geometric shapes for higher structures|globular]] [[Batanin ∞-category| ∞-category]] in which all [[k-morphism]]s are invertible, then the corresponding Kan complex is the [[nerve]] or rather the [[∞-nerve]] of this [[∞-category]].

Notably if $C$ is to be regarded as (the nerve of) an ordinary [[groupoid]], every composable pair of morphisms has a unique composite, and hence there should be a _unique_ 2-cell

  $$
    \array{
      && x_1
      \\
      & {}^{f}\nearrow &\Downarrow& \searrow^{g}
      \\
      x_0 &&\underset{h = g \circ f}{\to}&& x_2
    }
  $$

that is the unique **identity 2-morphism**

$$
  g \circ f \stackrel{=}{\Rightarrow} h
  \,.
$$

More generally, in a [[2-groupoid]] there may be non-identity 2-morphisms, and hence for any 1-morphism $k _ x_0 \to x_2$ 2-isomorphic to $h$, there may be many 2-morphisms $g \circ f \Rightarrow k$, hence many 2-cells

$$
  \array{
    && x_1
    \\
    & {}^{f}\nearrow &\Downarrow^{\simeq}& \searrow^{g}
    \\
    x_0 &&\underset{k }{\to}&& x_2
  }
  \,.
$$

All we can say for sure is that _at least_ one such 2-cell exists, and that the 2-cells themselves may be composed in some way. This is precisely what the horn-filler conditions in a Kan complex encode.

To see this for the composition of 2-morphisms, we need to move further up in dimension. The task of analyzing the combinatorics of k-simplices and their boundaries in the above fashion quickly goes beyond what can be handled in a naive fashion. Luckily, this combinatorial problem has been completely solved by [[Ross Street]] in his work on [[oriental]]s.

The $k$-[[oriental]] $O(k)$ is precisely the prescription for how exactly to think of  a $k$-[[simplex]] as being a [[k-morphism]] in an [[omega-category]]. The first few look like this:

$$
\array{\arrayopts{\rowalign{center}}
O(\Delta^0) = & \{ 0\} \\
O(\Delta^1) = & \left\{ 0 \to 1\right\} \\
O(\Delta^2) = & \left\{
\array{\begin{svg}
[[!include oriental > Delta2]]
\end{svg}}
\right\}\\
O(\Delta^3) = & \left\{
\array{\begin{svg}
[[!include oriental > Delta3]]
\end{svg}}\right\}\\
O(\Delta^4) = & \left\{
\array{\begin{svg}
[[!include oriental > Delta4]]
\end{svg}}
\right\}
}
$$

In fact, the [[omega-nerve]] $N(K)$ of an [[omega-category]] $K$ is the [[simplicial set]] whose collection of $k$-cells $N(K)_k := Hom(O(k),K)$ is precisely the collection of images of the $k$th oriental $O(k)$ in $K$.

This is fully formally the prescription of how to think of a Kan complex as an $\infty$-groupoid: the Kan complex $C$ is the [[omega-nerve]] of an [[omega-category]] in which all morphism are invertible:

* the $k$-cells in  $C_k$ are precisely the collection of $k$-morphisms ihn the omega-category of shape the $k$th [[oriental]] $O(k)$;

* the [[horn]]-filler conditions satisfied by these cells is precisely a reflection of the fact that

  1. there exists a notion of composition of adjacent k-morphisms in the [[omega-category]];

  1. under this composition all $k$-morphisms have an inverse.

We have already seen in low dimension how the existence of composites in an $\omega$-category is reflected in the fact that in a Kan-complex certain 22-simplices exist, and how the non-uniqueness of these 2-simplices reflects the existence of nontrivial 2-morphisms.

To see in a similar fashion that the Kan condition ensures the existence of _inverses_ consider an _outer horn_ in $C$, a diagram of 1-cells of the form

$$
  \array{
    && x_1
    \\
    & {}^{\mathllap{f}}\nearrow
    \\
    x_0 &&\underset{h}{\to}&& x_2
  }
  \,.
$$

In general given such a diagram in a [[category]], there is no guarantee that the corresponding triangle as above will exist in its [[nerve]]. But if the category is a [[groupoid]], then it is guaranteed that the missing 1-face can be chose to be the [[inverse]] of $f$ composed with the morphism $h$, and there is at least one 2-morphism

$$
  \array{
    && x_1
    \\
    & {}^{\mathllap{f}}\nearrow
    &\Downarrow^{\simeq}& \searrow^{\mathrlap{h \circ f^{-1}}}
    \\
    x_0 &&\underset{h}{\to}&& x_2
  }
  \,.
$$

A similar analysis for higher dimensional cells shows that the fact that a Kan complex has all horn fillers encodes precisely the fact that it is the [[omega-nerve]] of an [[omega-category]] in which _all_ [[k-morphism]]s for all $k$ are composable if adjacent and have a weak inverse.



[[!redirects Kan complexes]]

