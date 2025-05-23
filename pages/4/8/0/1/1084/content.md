
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
#### Homotopy
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--




#Contents#
* table of contents 
{:toc}

## Idea

The _mapping cone_ of a [[morphism]] $f : X \to Y$ in some [[homotopical category]] (precisely: a [[category of cofibrant objects]]) is, if it exists, a particular representative of the [[homotopy fiber|homotopy cofiber]] of $f$. 

It is also called the _homotopy [[cokernel]]_ of $f$ or the _[[weak quotient]]_ of $Y$ by the [[image]] of $X$ in $Y$ under $f$. 

The dual notion is that of [[mapping cocone]].

<img src="http://ncatlab.org/nlab/files/mappingcone.jpg" width="660" >

(graphics taken from [Muro 2010](#Muro10))


## Definition
 {#Definition}

The mapping cone construction is a means to _present_ in a [[category with weak equivalences]] the following canonical
construction in [[homotopy theory]]/[[(∞,1)-category theory]].

+-- {: .num_defn #InfinityCokernel}
###### Definition

In an [[(∞,1)-category]] $\mathcal{C}$ with [[terminal object]] and [[(∞,1)-pushout]], the [[homotopy fiber|homotopy cofiber]] of a [[morphism]] $f : X \to Y$ is the [[homotopy pushout]]

$$
  coker(f) \coloneqq Y \coprod_X {*}
$$

hence the object [[universal construction]] sitting universally in a [[diagram]] of the form

$$
  \array{
     X &\stackrel{}{\to}& {*}
     \\
     \downarrow^{\mathrlap{f}} &\swArrow_{\simeq}& \downarrow
     \\
     Y &\to& coker(f)
  }
  \,.
$$

=--

+-- {: .num_prop #HomotopyCofiberByFactorizationLemma}
###### Proposition

If the [[(∞,1)-category]] $\mathcal{C}$ is presented by (is [[equivalence of (infinity,1)-categories|equivalent]] to the [[simplicial localization]] of) a [[category of cofibrant objects]] $C$ (for instance given by the [[cofibrant objects]] in a [[model category]]) then this homotopy cofiber is presented by the ordinary [[colimit]] 

$$
  \array{
    && X &\stackrel{f}{\to}& Y
    \\
    && \downarrow^{\mathrlap{i_1}} && \downarrow^{\mathrlap{i}}
    \\
    X &\stackrel{i_0}{\to}& cyl(X)
    \\
    \downarrow && &\searrow & \downarrow
    \\
    {*} &\to& &\to& cone(f) 
  }
$$

in $C$ using any [[cylinder object]] $cyl(X)$ for $X$.

=--

This is discussed in detail at [[factorization lemma]] and at [[homotopy pullback]].

+-- {: .num_remark }
###### Remark

Intuitively this says that $cone(f)$ is the object obtained by

1. forming the cylinder over $X$;

1. gluing to one end of that the object $Y$ as specified by the map $f$.

1. shrinking the other end of the cylinder to the point.

Intuitively it is clear that this way every [[cycle]] in $Y$ that happens to be in the image of $X$ can be "continuously" translated in the cylinder-direction, keeping it constant in $Y$, to the other end of the cylinder, where it becomes the point. This means that every [[homotopy group]] of $Y$ in the image of $f$ vanishes in the mapping cone. Hence in the mapping cone **the image of $X$ under $f$ in $Y$ is removed up to homotopy**. This makes it clear how $cone(f)$ is a homotopy-version of the [[cokernel]] of $f$. And therefore the name "mapping cone".

=--



+-- {: .num_remark }
###### Remark

A morphism $\eta : cyl(X) \to Y$ out of a [[cylinder object]] is a [[left homotopy]] $\eta : g \Rightarrow h$ between its restrictions $g\coloneqq \eta(0)$ and $h \coloneqq \eta(1)$ to the cylinder boundaries

$$
  \array{
     X
     \\
     \downarrow^{\mathrlap{i_0}} & \searrow^{\mathrlap{g}}
     \\
     cyl(X) &\stackrel{\eta}{\to}& Y
     \\
     \uparrow^{\mathrlap{i_1}} & \nearrow_{\mathrlap{h}}
     \\
     X
  }
  \,.
$$

Therefore prop. \ref{HomotopyCofiberByFactorizationLemma} says that 
the mapping cone is the the [[universal property|universal]] object with a morphism $i$ from $Y$ and a [[left homotopy]] from $i \circ f$ to the [[zero morphism]]. This is of course also precisely what def. \ref{InfinityCokernel} is saying.

=--


+-- {: .num_prop }
###### Proposition

The colimit in prop. \ref{HomotopyCofiberByFactorizationLemma} may be computed in two stages by two consecutive [[pushouts]] in $C$, and in two ways by the following [[pasting diagram]]:

$$
  \array{
    && X &\stackrel{f}{\to}& Y
    \\
    && \downarrow^{i_1} && \downarrow
    \\
    X &\stackrel{i_0}{\to}& cyl(X) &\to & cyl(f)
    \\
    \downarrow && \downarrow && \downarrow
    \\
    {*} &\to& cone(X) &\to& cone(f) 
  }
  \,.
$$

Here every square is a [[pushout]], (and so by the [[pasting law]] is every rectangular pasting composite).

=--

This now is a basic fact in ordinary [[category theory]]. The pushouts appearing here go by the following names:

+-- {: .num_defn #CylindersAndCones}
###### Definition

The pushout

$$
  \array{
     X &\stackrel{i_0}{\to}& cyl(X)
     \\
     \downarrow && \downarrow
     \\
     {*} &\to& cone(X)
  }
$$

defines the **[[cone]]** $cone(X)$ over $X$ (with respect to the chosen [[cylinder object]]): the result of taking the [[cylinder object|cylinder]] over $X$ and identifying one $X$-shaped end with the [[point]].

The pushout 

$$
  \array{
    X &\stackrel{f}{\to}& Y
    \\
    \downarrow && \downarrow
    \\
    cyl(X) &\to& cyl(f)
  }
$$

defines the **[[mapping cylinder]]** $cyl(f)$ of $f$, the result of identifying one end of the cylinder over $X$ with $Y$, using $f$ as the gluing map.

The pushout 

$$
  \array{
    cyl(X) &\to& cyl(f)
    \\
    \downarrow && \downarrow
    \\
    cone(X) &\to& cone(f)
  }
$$

defines the **mapping cone** $cone(f)$ of $f$: the result of forming the cylinder over $X$ and then identifying one end with the point and the other with $Y$, via $f$.

=--

The geometric intuition behind this is best seen in the archetypical example of the [[classical model structure on topological spaces]]. See the example _[For topological spaces](#ForTopologicalSpaces)_ below. The example _[For chain complexes](InChainComplexes)_ can be understood similarly geometrically by thinking of all chain complexes as [[singular chain complex|singular chains]] on topological spaces.


## Examples

We discuss realizations of the general construction in various contexts.
Some of these examples are regarded in parts of the literature as the default examples, notably that [for topological spaces](#ForTopologicalSpaces) and that [for chain complexes](#InChainComplexes).

### Suspension 

The mapping cone of the morphism $X \to {*}$ to the [[terminal object]] is the [[suspension object]] $\Sigma X$ of an object $X$. The dual notion of the [[loop space object]] of $X$.

### For topological spaces
 {#ForTopologicalSpaces}

The notion _mapping cone_  derives its name from its geometrical 
interpretation in the category [[Top]] of [[topological spaces]].

For more details see also at _[[topological cofiber sequence]]_.


With respect to the standard [[model structure on topological spaces]] every [[CW-complex]] is a cofibrant object, and hence mapping cones on maps between CW-complexes have intrinsic meaning in [[homotopy theory]].

Write $I \coloneqq [0,1] \subset \mathbb{R} \in $ [[Top]] for the [[closed interval]] with its [[Euclidean space|Euclidean]] [[metric topology]]. This is an [[interval object]] for the standard model structure. We may therefore take the [[cylinder object]] of a topological space $X$ to be 

$$ 
  cyl(X) \coloneqq X \times I
  \,,
$$

which is literally the cylinder over $X$. 

Given a [[continuous function]] $f:X\to Y$, the 
[[topological space]] $cone(f)$ is

$$
  cone(f) =  (X \times I) \cup_{f} Y
$$

This is the [[disjoint union]] of $X \times I$ with $Y$
followed by an identification under which for each 
$x\in X$ a point $(x,1) \in X \times I$ is identified with 
the point $f(x) \in Y$ and followed by the contraction of $X\times \{0\}$ to a point. 

Of course the opposite convention is also possible: identify $(x,0)$ with $f(x)$ for all $x$ and then contract $X\times\{1\}$ to a point; the two constructions of cones are canonically homeomorphic; the first is sometimes called the "inverse mapping cone".

The [[singular chain complex]] [[functor]] from [[Top]] to the 
[[category of chain complexes]] of [[abelian groups]] sends the mapping cone to a mapping cone in the sense of chain complexes (up to conventions on the orientation of the interval and vector order in the definition of mapping cone of chain complexes). 


### For chain complexes
 {#InChainComplexes}


Let $Ch_\bullet = Ch_\bullet(R Mod)$ be the [[category of chain complexes]] in $R$[[Mod]] for some [[ring]] $R$. 

(For instance if $R = \mathbb{Z}$ the [[integers]], then this is $Ch_\bullet(Ab)$, chain complexes of [[abelian groups]]. More generally $R Mod$ can be replaced by any [[abelian category]] in the following, with the evident changes in  the presentation here and there.)

We derive an explicit presentation of the mapping cone $cone(f)$ of a [[chain map]] $f$, according to the general definition \ref{CylindersAndCones}. The end result is prop. \ref{ComponentsOfMappingConeInChainComplexes} below,
reproducing the classical formula for the mapping cone.

+-- {: .num_defn }
###### Definition

Write $*_\bullet \in Ch_\bullet(\mathcal{A})$ for the chain complex
concentrated on $R$ in degree 0

$$
  *_\bullet 0 
   = 
  [\cdots \to 0 \to 0 \to R]
  \,.
$$

=--

+-- {: .num_remark }
###### Remark

This may be understood as the [[normalized chain complex]] of [[simplicial homology|chains of simplices]] on the terminal [[simplicial set]] $\Delta^0$, the 0-[[simplex]].

=--

+-- {: .num_defn #BoundaryInclusionIntoChainComplexIntervalObject}
###### Definition

Let $I_\bullet \in Ch_{\bullet}(\mathcal{A})$ be given by

$$
  I_\bullet
  = 
  (\cdots 0 \to 0 \to R \stackrel{(-id,id)}{\to} R \oplus R)
  \,.
$$

Denote by

$$
  i_0 : *_\bullet \to I_\bullet
$$

the [[chain map]] which in degree 0 is the canonical inclusion into the second summand of a [[direct sum]] and by

$$
  i_1 : *_\bullet \to I_\bullet
$$

correspondingly the canonical inclusion into the first summand.

=--


+-- {: .num_remark }
###### Remark

This is the standard [[interval object in chain complexes]].

It is in fact the [[normalized chain complex]] of [[chains on a simplicial set]] for the canonical simplicial interval, the 1-[[simplex]]:

$$
  I_\bullet = C_\bullet(\Delta[1])
  \,.
$$

The [[differential]] $\partial^I = (-id, id)$ here expresses the [[alternating face map complex]] [[boundary]] operator, which in terms of the three non-degenerate [[basis]] elements is given by

$$
  \partial ( 0 \to 1 ) = (1) - (0)
  \,.
$$


=--


We decompose the proof of this statement is a sequence of substatements.


+-- {: .num_prop }
###### Proposition

For $X_\bullet \in Ch_\bullet$ the
[[tensor product of chain complexes]] 

$$
  (I \otimes X)_\bullet
  \in
  Ch_\bullet
$$

is a [[cylinder object]] of $X_\bullet$
for the structure of a [[category of cofibrant objects]] on $Ch_\bullet$
whose cofibrations are the [[monomorphisms]] and whose weak equivalences are the [[quasi-isomorphisms]] (the substructure of the standard [[injective model structure on chain complexes]]).

=--

+-- {: .num_prop }
###### Proposition

The complex $(I \otimes X)_\bullet$ has components

$$
  (I \otimes X)_n
  = 
  X_n \oplus X_n \oplus X_{n-1}
$$

and the [[differential]] is given by

$$
  \array{
    X_{n+1} \oplus X_{n+1} &\stackrel{\partial^X \oplus \partial^X}{\to}& X_n \oplus X_n
    \\
    \oplus &\nearrow_{(-id,id)}& \oplus
    \\
    X_{n} &\underset{-\partial^X}{\to}& X_{n-1}
  }
  \,,
$$

hence in [[matrix calculus]] by

$$
  \partial^{I \otimes X}
   =
  \left(
    \array{
      \partial^X \oplus \partial^X & (-id, id)
      \\
      0 & -\partial^X
    }
  \right)
  \;\;\colon\;\;
  (X_{n+1} \oplus X_{n+1}) \oplus X_{n}
  \to
  (X_{n} \oplus X_{n}) \oplus X_{n-1}
  \,.
$$

=--

+-- {: .proof}
###### Proof

By the formula discussed at [[tensor product of chain complexes]]
the components arise as the [[direct sum]]

$$
  (I \otimes X )_n
  =
  (R_{(0)} \otimes X_n )
  \oplus
  (R_{(1)} \otimes X_n )
  \oplus 
  (R_{(0 \to 1)} \otimes X_{(n-1)} )
$$

and the [[differential]] picks up a sign when passed past the 
degree-1 term $R_{(0 \to 1)}$:

$$
  \begin{aligned}
    \partial^{I \otimes X}
    (
      (0 \to 1), x
    )
    &= 
    ( (\partial^I (0 \to 1)), x )
    -
    ( (0\to 1), \partial^X x )
    \\
    & = 
    ( - (0) + (1), x )
    -
    ( (0 \to 1), \partial^X x )  
    \\
    & = -((0), x) + ((1), x) -  ( (0 \to 1), \partial^X x )
  \end{aligned}
  \,.
$$

=--

+-- {: .num_remark #InclusionOfChainComplexIntoItsCylinder}
###### Remark

The two boundary inclusions of $X_\bullet$ into the cylinder
are given in terms of def. \ref{BoundaryInclusionIntoChainComplexIntervalObject} by

$$
  i^X_0 
   : 
  X_\bullet \simeq *_\bullet \otimes X_\bullet 
   \stackrel{i_0 \otimes id_X}{\to} (I\otimes X)_\bullet
$$

and

$$
  i^X_1 
   : 
  X_\bullet \simeq *_\bullet \otimes X_\bullet 
   \stackrel{i_1 \otimes id_X}{\to} (I\otimes X)_\bullet
$$

which in components is the inclusion of the second or first 
direct summand,
respectively

$$
  X_n \hookrightarrow X_n \oplus X_n \oplus X_{n-1}
  \,.
$$

=--

One part of definition \ref{CylindersAndCones} now reads:

+-- {: .num_defn }
###### Definition

For $f_\bullet : X_\bullet \to Y_\bullet $ a [[chain map]],
the [[mapping cylinder]] $cyl(f)$ is the [[pushout]]

$$
  \array{
    cyl(f)_\bullet &\leftarrow& Y_\bullet
    \\
    \uparrow && \uparrow^{\mathrlap{f}}
    \\
    I_\bullet \otimes X_\bullet  &\stackrel{i_0}{\leftarrow}& X_\bullet
  }
  \,.
$$

=--

+-- {: .num_prop #MappingConeForChainComplexesExplicitly}
###### Proposition

The components of $cyl(f)_\bullet$ are

$$
  cyl(f)_n = X_n \oplus Y_n \oplus X_{n-1}
$$

and the [[differential]] is given by

$$
  \array{
    X_{n+1} \oplus Y_{n+1} &\stackrel{\partial^X \oplus \partial^Y}{\to}& X_n \oplus Y_n
    \\
    \oplus &\nearrow_{(-id,f)}& \oplus
    \\
    X_{n} &\underset{-\partial^X}{\to}& X_{n-1}
  }
  \,,
$$

hence in [[matrix calculus]] by

$$
  \partial^{cyl(f)}
   =
  \left(
    \array{
      \partial^X \oplus \partial^Y & (-id, f_n)
      \\
      0 & -\partial^X
    }
  \right)
  : 
  (X_{n+1} \oplus Y_{n+1}) \oplus X_{n}
  \to
  (X_{n} \oplus Y_{n}) \oplus X_{n-1}
  \,.
$$


=--

+-- {: .proof}
###### Proof

The [[colimits]] in a [[category of chain complexes]] $Ch_\bullet(\mathcal{A})$ are computed in the underlying 
[[presheaf category]] of [[towers]] in $\mathcal{A}$. 
There they are computed 
degreewise in $\mathcal{A}$
(see at [limits in presheaf categories](limits+and+colimits+by+example#limitsinpresheafcat)). 
Here the statement is evident:

the pushout identifies one [[direct sum|direct summand]] $X_n$
with $Y_n$ along $f_n$ and so where previously a $id_{X_n}$
appeared on the diagonl, there is now $f_n$.


=--

The last part of definition \ref{CylindersAndCones} now reads:

+-- {: .num_defn }
###### Definition

For $f_\bullet : X_\bullet \to Y_\bullet $ a [[chain map]],
the **mapping cone** $cone(f)$ is the [[pushout]]

$$
  \array{
    cone(f) &\leftarrow& cyl(f)
    \\
    \uparrow && \uparrow
    \\
    cone(X) &\leftarrow& X \otimes I
    \\
    \uparrow && \uparrow^{\mathrlap{i_1}}
    \\
    0 &\leftarrow& X
  }
$$

=--

In the literature this appears for instance as ([Schapira, def. 3.2.2](#Schapira)).

+-- {: .num_prop #ComponentsOfMappingConeInChainComplexes}
###### Proposition

The components of the mapping cone $cone(f)$ are

$$
  cone(f)_n =   Y_n \oplus X_{n-1} 
$$

with differential given by

$$
  \array{
    Y_{n+1} &\stackrel{\partial^Y}{\to}& Y_n
    \\
    \oplus &\nearrow_{f_n}& \oplus
    \\
    X_{n} &\underset{-\partial^X}{\to}& X_{n-1}
  }
  \,,
$$

and hence in [[matrix calculus]] by

$$
  \partial^{cone(f)}
   =
  \left(
    \array{
      \partial^Y_{n+1} & f_n
      \\
      0 & -\partial^X_n
    }
  \right)
  : 
  Y_{n+1} \oplus X_{n}
  \to
  Y_{n} \oplus X_{n-1}
  \,.
$$


=--

+-- {: .proof}
###### Proof

As before the pushout is computed degreewise.
This identifies the remaining unshifted copy of $X$ with 0. 

=--

+-- {: .num_prop #InclusionIntoChainComplexCone}
###### Proposition

For $f : X_\bullet \to Y_\bullet$ a [[chain map]], 
the canonical inclusion $i : Y_\bullet \to cone(f)_\bullet$ 
of $Y_\bullet$ into the  mapping cone of $f$ is given in 
components

$$
 i_n : Y_n \to cone(f)_n = Y_n \oplus X_{n-1}
$$

by the canonical inclusion of a summand into a [[direct sum]].

=--

+-- {: .proof}
###### Proof

This follows by starting with 
remark \ref{InclusionOfChainComplexIntoItsCylinder} and then 
following these inclusions through the formation of the two colimits
as discussed above.

=--

The construction above builds the mapping cone explicitly via the standard formula for [[homotopy pushouts]]. Often however other presentations are more convenient:


+-- {: .num_prop #ConeViaDoubleComplex}
###### Proposition

For $f_\bullet \colon X_\bullet \to Y_\bullet$ a [[chain map]], 
consider the [[double complex]] $D_{\bullet,\bullet}$ concentrated 
in degrees $D_{1,\bullet} \coloneqq X_\bullet$ and 
$D_{0,\bullet} \coloneqq Y_\bullet$ with 
$\partial_{0,\bullet} \coloneqq f_\bullet \colon D_{1,\bullet} \to D_{0,\bullet}$.

Then the [[total complex]] of $D_{\bullet, \bullet}$ is also
a model for the mapping cone of $f$:

$$
 Cone(f) \simeq tot(D_{\bullet,\bullet})
  \,.
$$

=--

+-- {: .proof}
###### Proof

One checks by inspection that 
$tot(D_{\bullet,\bullet}) = Cone(\tilde f)$
for $\tilde f\colon X_\bullet \to Y_\bullet$
for which there is a [[chain homotopy]] $f \Rightarrow f'$
(given only by multiplication by signs).

=--

This appears for instance as ([Weibel, Exercise 1.2.8](#Weibel)).



### For cochain complexes
 {#InCochainComplexes}

We spell out the situation in more detail in a [[category of cochain complexes]].

Let $\mathcal{A}$ be some [[concrete category|concrete]] [[additive category]] and $Ch^\bullet(\mathcal{A})$ the [[category of chain complexes]] in $\mathcal{A}$. For

$$
  f : V^\bullet \to W^{\bullet}
$$

a morphism, the mapping cone is the complex

$$
  \begin{aligned}
   Cone(f) 
    & \coloneqq
  (\cdots \to Cone(f)^{k-1} \stackrel{d_{Cone(f)}}{\to} Cone(f)^k) \to \cdots)
   \\
   & \coloneqq
  \left(
    \array{
      \cdots \to & V^k &\stackrel{- d_V}{\to}& V^{k+1} & \to \cdots
      \\
      & \oplus &\searrow^{f^k}& \oplus
      \\
      \cdots \to & W^{k-1} &\underset{d_W}{\to}& W^k & \to \cdots
    }
  \right)
  \end{aligned}
  \,.
$$

There is a canonical co[[chain homotopy]]

$$
  \array{
    Cone(f) &\leftarrow& 0
    \\
    {}^{\mathllap{i}}\uparrow &\swArrow_{\eta}& \uparrow
    \\
    W &\stackrel{f}{\leftarrow}& V 
  }
$$

where $i : W \to Cone(f)$ is the canonical inclusion, componentwise given by

$$
  i^k : W^k \stackrel{(0,Id)}{\to} V_{k+1} \oplus W^k
$$

and where the cochain homotopy $\eta$ has components

$$
  \eta^k : V^k \stackrel{(Id,0)}{\to} Cone(f)^{k-1} = V^k \oplus W^{k-1}
$$ 

which we denote on $v \in V^k$ by

$$
  \eta : v \mapsto (f(v))[1] 
  \,.
$$

The fact that this is a cochain homotopy means that

$$
  [d,\eta] = i \circ f - 0
  \,,
$$

which we check on any $v \in V^k$ by computing

$$
  \begin{aligned}
    [d, \eta](v) &= 
    d_{Cone(f)} \circ \eta (v) 
    + \eta(d_V v)
    \\
    & = d_{Cone(f)} (f(v)[1]) + (f(d_V v))[1]
    \\
    & =
    \left( 
      f(v)
      - 
      (d_{W}f(v))[1]
    \right)
    +
    (d_W (f(v)))[1]
    \\
    & = f(v)
  \end{aligned}
  \,,
$$

where we used the above definition of $d_{Cone(f)}$ and the fact that $f$ is a chain homomorphism and hence intertwines the differentials.

This cochain homotopy is universal in that 
for any other cochain homotopy

$$
  \array{
    X &\leftarrow& 0
    \\
    {}^{\mathllap{j}}\uparrow &\swArrow_{\rho}& \uparrow
    \\
    W &\stackrel{f}{\leftarrow}& V 
  }
$$

hence

$$
  j \circ f = [d,\rho]
$$

we have a morphism

$$
  (j,\rho) :  Cone(f) \to X
$$

given on $W$ by $j$ and on $V$ by $\rho$

$$
  (j,\rho)^k : V^{k+1} \oplus W^k \stackrel{(\rho, j)}{\to} X^k
$$

which is indeed a cochain homomorphism because for all $v + w \in Cone(f)$ we have 

$$
  \begin{aligned}
    d_X (j,\rho)(v + w) 
     & = 
    d_X (\rho v) +  d_X (j(w))
     \\
     & = [d,\rho](v) - \rho d_V v + j (d_W w)
     \\
     & = j f (v) - \rho d_V v + j (d_{Cone(f)} w)
     \\
     & = (j,\rho) d_{Cone(f)}(v + w)
  \end{aligned}
$$

and which is unique with the property that [[whiskering]] of [[2-morphism]]s gives

$$
  \array{
    X &\leftarrow& 0
    \\
    {}^{\mathllap{j}}\uparrow &\swArrow_{\rho}& \uparrow
    \\
    W &\stackrel{f}{\leftarrow}& V 
  }
  \;\;\;\;\;
   =
  \;\;\;\;\;
  \array{
    X
    \\
    & \nwarrow^{\mathrlap{(j,\rho)}}
    \\
    &&  Cone(f) &\leftarrow& 0
    \\
    && {}^{\mathllap{i}}\uparrow &\swArrow_{\eta}& \uparrow
    \\
    && W &\stackrel{f}{\leftarrow}& V 
  }  
$$

hence that

$$
  j = (j,\rho) \circ i
$$

and

$$
  \rho = (j,\rho) \circ \eta
  \,.
$$


### In additive categories with translation


Let $\mathcal{A}$ be an [[additive category]] [[category with translation|with translation]] $T=[1] : \mathcal{A} \to \mathcal{A}$. Let $X$ and $Y$ be two [[differential objects]] in $(\mathcal{A},T)$ and $f : X \to Y$ any [[morphism]] in $C$. 

The **mapping cone** $Cone(f)$ of $f$ is the [[differential object]] whose underlying object is the [[direct sum]] $T X \oplus Y$ and whose differential $d_{cone f} : T X \oplus X \to T T X \oplus T X$ is given in [[matrix calculus]] notation by

$$
  d_{cone f} :=
  \left(
   \array{
    d_{T X} & 0
    \\
    T(f) & d_Y
   }
  \right)
  =
  \left(
   \array{
    - T(d_X) & 0
    \\
    T(f) & d_Y
   }
  \right)
  \,.
$$

Notice the minus sign here, coming from the definition of a [[differential object|shifted differential object]].





## Properties

### Homology exact sequences and fiber sequences
 {#HomologyExactSequencesAndFiberSequences}

We discuss the relation between mapping cones 
in [[categories of chain complexes]], as [above](#InChainComplexes), 
and  [[long exact sequences in homology]]. For an exposition of the following see there the section _[Relation to homotopy fiber sequences](long+exact+sequence+in+homology#RelationToHomotopyFiberSequences)_.

Let $f : X_\bullet \longrightarrow Y_\bullet$ be a [[chain map]]
and write $cone(f) \in Ch_\bullet(\mathcal{A})$
for its mapping cone
as explicitly given in prop. \ref{ComponentsOfMappingConeInChainComplexes}.


+-- {: .num_defn #ProjectionOutOfChainComplexMappingCone}
###### Definition

Write $X[1]_\bullet \in Ch_\bullet(\mathcal{A})$
for the [[suspension of a chain complex]] of $X$. Write

$$
  p : cone(f) \to X[1]_\bullet
$$

for the [[chain map]] which in components 

$$
  p_n : cone(f)_n \to X[1]_n
$$

is given, via prop. \ref{ComponentsOfMappingConeInChainComplexes}, 
by the canonical projection out of a direct sum

$$
  p_n : Y_\n \oplus X_{n-1} \to X_{n-1}
  \,.
$$

=--

+-- {: .num_prop #ProjectionOutOfChainComplexMappingConeIsHoCofiber}
###### Proposition

The chain map $p : cone(f)_\bullet \to X[1]_\bullet$
represents the [[homotopy cofiber]] of the 
canonical map 
$i : Y_\bullet \to cone(f)_\bullet$.

=--

+-- {: .proof}
###### Proof

By prop. \ref{InclusionIntoChainComplexCone} and 
def. \ref{ProjectionOutOfChainComplexMappingCone} the sequence

$$
  Y_\bullet 
    \stackrel{i}{\to}
  cone(f)_\bullet
    \stackrel{p}{\to}
  X[1]_\bullet
$$

is a [[short exact sequence]] of chain complexes (since it is so degreewise, in fact degreewise it is even a [[split exact sequence]]). In particular we have a [[cofiber]] [[pushout]] diagram

$$
  \array{
     Y_\bullet &\stackrel{i}{\hookrightarrow}& cone(f)_\bullet
     \\
     \downarrow && \downarrow
     \\
     0 &\to& X[1]_\bullet
  }
  \,.
$$

Now, in the [[injective model structure on chain complexes]] all chain complxes are [[cofibrant objects]] and an inclusion such as $i : Y_\bullet \hookrightarrow cone(f)_\bullet$ is a [[cofibration]]. By the detailed discussion at [[homotopy limit]] this means that the ordinary colimit here is in fact a [[homotopy colimit]], hence exhibits $p$ as the [[homotopy cofiber]] of $i$.

=--

+-- {: .num_cor #HomotopyCofiberSequenceOfChainMap}
###### Corollary

For $f_\bullet : X_\bullet \to Y_\bullet$ a [[chain map]], 
there is a **[[homotopy cofiber sequence]]** of the form

$$
  X_\bullet 
    \stackrel{f_\bullet}{\to}
  Y_\bullet
    \stackrel{i_\bullet}{\to}
  cone(f)_\bullet
    \stackrel{p_\bullet}{\to}
  X[1]_\bullet
    \stackrel{f[1]_\bullet}{\to}
  Y_\bullet
    \stackrel{i[1]_\bullet}{\to}
  cone(f)_\bullet
    \stackrel{p[1]_\bullet}{\to}
  X[2]_\bullet
    \to 
  \cdots
$$

=--

In order to compare this to the discussion of [[nLab:connecting homomorphisms]], we now turn attention to the case that $f_\bullet$ happens to be a [[monomorphism]]. Notice that this we can always assume, up to [[quasi-isomorphism]], for instance by prolonging $f$ by the map into its [[mapping cylinder]]

$$
  X_\bullet \to Y_\bullet \stackrel{\simeq}{\to} cyl(f) 
  \,.
$$

By the axioms on an [[abelian category]] in this case we have a [[short exact sequence]]

$$
  0 \to X_\bullet \stackrel{f_\bullet}{\to} Y_\bullet \stackrel{p_\bullet}{\to} Z_\bullet \to 0
$$

of chain complexes. The following discussion revolves around the fact that now $cone(f)_\bullet$ as well as $Z_\bullet$ are both models for the homotopy cofiber of $f$.



+-- {: .num_lemma #ConeInjectionEquivalentToZigzag}
###### Lemma

Let 
$$
  X_\bullet \stackrel{f_\bullet}{\to} Y_\bullet \stackrel{p_\bullet}{\to} Z_\bullet
$$

be a [[short exact sequence]] of [[chain complexes]]. 


The collection of linear maps

$$
  h_n : Y_n \oplus X_{n-1} \to Y_n \stackrel{}{\to} Z_n
$$

constitutes a [[chain map]]

$$
  h_\bullet : cone(f)_\bullet \to Z_\bullet
  \,.
$$


This is a [[quasi-isomorphism]]. The inverse of $H_n(h_\bullet)$ is given by sending a representing [[cycle]] $z \in Z_n$ to 

$$
  (\hat z_n, \partial^Y \hat z_n) \in Y_n \oplus X_{n+1}
  \,,
$$

where $\hat z_n$ is any choice of lift through $p_n$ and where $\partial^Y \hat z_n$ is the formula expressing the [[connecting homomorphism]] in terms of elements, as discussed at [Connecting homomorphism -- In terms of elements](connecting%20homomorphism#OnHomologyInTermsOfElements).
 
Finally, the morphism $i_\bullet : Y_\bullet \to cone(f)_\bullet$ is eqivalent in the [[homotopy category]] (the [[derived category]]) to the [[zigzag]]

$$
  \array{
    && cone(f)_\bullet 
    \\
    && \downarrow^{\mathrlap{h}}_{\mathrlap{\simeq}}
    \\
    Y_\bullet &\to& Z_\bullet
  }
  \,.
$$

=--

In the literature this appears for instance as ([Schapira, cor. 7.2.2](#Schapira)).

+-- {: .proof}
###### Proof

To see that $h_\bullet$ defines a chain map recall the differential $\partial^{cone(f)}$ from prop. \ref{ComponentsOfMappingConeInChainComplexes}, which acts by

$$
  \partial^{cone(f)} (x_{n-1}, \hat z_n)
  = 
  (  -\partial^X x_{n-1} , \partial^Y \hat z_n + x_{n-1} )
$$

and use that $x_{n-1}$ is in the [[kernel]] of $p_n$ by exactness, hence

$$
  \begin{aligned}
    h_{n-1}\partial^{cone(f)}(x_{n-1}, \hat z_n)
    &= 
    h_{n-1}( -\partial^X x_{n-1}, \partial^Y \hat z_n + x_{n-1}  )
    \\
    & = p_{n-1}( \partial^Y \hat z_n + x_{n-1})
    \\
    & = p_{n-1}( \partial^Y \hat z_n )
    \\
    & = \partial^Z p_n \hat z_n
    \\
    & = \partial^Z h_n(x_{n-1}, \hat z_n)
  \end{aligned}
  \,.
$$

It is immediate to see that we have a [[commuting diagram]] of the form

$$
  \array{
    && cone(f)_\bullet 
    \\
    & {}^{\mathllap{i_\bullet}}\nearrow& \downarrow^{\mathrlap{h}}_{\mathrlap{\simeq}}
    \\
    Y_\bullet &\to& Z_\bullet
  }
$$

since the composite morphism is the inclusion of $Y$ followed by the bottom morphism on $Y$. 

Abstractly, this already implies that $cone(f)_\bullet \to Z_\bullet$ is a [[quasi-isomorphism]], 
for this diagram gives a morphism of [[cocones]] under the diagram defining $cone(f)$ in prop. \ref{HomotopyCofiberByFactorizationLemma} and by the above both of these cocones are [[homotopy colimit|homotopy-colimiting]].

But in checking the claimed inverse of the induced map on homology groups, we verify this also explicity:

We first determine those cycles $(x_{n-1}, y_n) \in cone(f)_n$ which lift a cycle $z_n$. By lemma \ref{HomotopyCofiberByFactorizationLemma}
a lift of chains is any pair of the form $(x_{n-1}, \hat z_n)$ where $\hat z_n$ is a lift of $z_n$ through $Y_n \to X_n$. So $x_{n-1}$ has to be found such that this pair is a cycle.
By prop. \ref{ComponentsOfMappingConeInChainComplexes} the differential acts on it by

$$
  \partial^{cone(f)} (x_{n-1}, \hat z_n)
  = 
  (  -\partial^X x_{n-1} , \partial^Y \hat z_n + x_{n-1} )
$$

and so the condition is that 

$x_{n-1} \coloneqq -\partial^Y \hat z_n$ (which implies $\partial^X x_{n-1} = -\partial^X \partial^Y \hat z_n = -\partial^Y \partial^Y \hat z_n = 0$ due to the fact that $f_n$ is assumed to be an inclusion, hence that $\partial^X$ is the restriction of $\partial^Y$ to elements in $X_n$).

This condition clearly has a unique solution for every lift $\hat z_n$ and a lift $\hat z_n$ always exists since $p_n : Y_n \to Z_n$ is surjective, by assumption that we have a [[short exact sequence]] of chain complexes. This shows that $H_n(h_\bullet)$ is surjective.

To see that it is also injective we need to show that 
if a [[cycle]] $(-\partial^Y \hat z_n, \hat z_n) \in cone(f)_n$ maps to a cycle $z_n = p_n(\hat z_n)$ that is trivial in $H_n(Z)$ in that there is $c_{n+1}$ with $\partial^Z c_{n+1} = z_n$, then also the original cycle was trivial in homology, in that there is $(x_n, y_{n+1})$ with

$$
  \partial^{cone(f)}(x_n, y_{n+1})
  \coloneqq
  (-\partial^X x_n, \partial^Y y_{n+1} + x_n)
  =
  (-\partial^Y \hat z_n, \hat z_n)
  \,.
$$

For that let $\hat c_{n+1} \in Y_{n+1}$ be a lift of $c_{n+1}$ through $p_n$, which exists again by surjectivity of $p_{n+1}$. Observe that

$$
  p_{n}( \hat z_n -  \partial^Y \hat c_{n+1})
  = 
  z_n -\partial^Z ( p_n \hat c_{n+1} )
  = 
  z_n - \partial^Z ( c_{n+1} ) 
  = 
  0
$$

by assumption on $z_n$ and $c_{n+1}$,
and hence that $\hat z_n - \partial^Y \hat c_{n+1}$ is in $X_n$ by exactness.

Hence 
$(z_n - \partial^Y \hat c_{n+1}, \hat c_{n+1}) \in cone(f)_n$
trivializes the given cocycle:

$$
  \begin{aligned}
    \partial^{cone(f)}( \hat z_n - \partial^Y \hat c_{n+1}  , \hat c_{n+1})
    & = 
   (-\partial^X(\hat z_n - \partial^Y \hat c_{n+1} ), \partial^Y \hat c_{n+1} + (\hat z_n - \partial^Y \hat c_{n+1} ) )
    \\
    & = (-\partial^Y(\hat z_n - \partial^Y \hat c_{n+1}),  \hat z_n )
    \\
    & =
    ( -\partial^Y \hat z_n, \hat z_n )
  \end{aligned}
  \,.
$$


=--

+-- {: .num_theorem }
###### Theorem

Let 
$$
  X_\bullet \stackrel{f_\bullet}{\to} Y_\bullet \to Z_\bullet
$$

be a [[short exact sequence]] of [[chain complexes]]. 

Then the  [[chain homology]] functor

$$
  H_n(-) : Ch_\bullet(\mathcal{A}) \to \mathcal{A}
$$

sends the homotopy cofiber sequence of $f$, cor. \ref{HomotopyCofiberSequenceOfChainMap}, to the 
[[long exact sequence in homology]] induced by the given short
exact sequence, hence to

$$
  H_n(X_\bullet)
  \to
  H_n(Y_\bullet)
   \to 
  H_n(Z_\bullet)
   \stackrel{\delta}{\to}
  H_{n-1}(X_\bullet)
   \to 
  H_{n-1}(Y_\bullet)
   \to 
  H_{n-1}(Z_\bullet)
   \stackrel{\delta}{\to}
  H_{n-2}(X_\bullet)
   \to \cdots
  \,,
$$

where $\delta_n$ is the $n$th [[connecting homomorphism]].


=--

+-- {: .proof}
###### Proof

By lemma \ref{ConeInjectionEquivalentToZigzag} the 
homotopy cofiber sequence is equivalen to the [[zigzag]]

$$
  \array{
     && && && && && cone(f)[1]_\bullet &\to& \cdots
     \\
     && && && && && \downarrow^{\mathrlap{h[1]_\bullet}}_{\mathrlap{\simeq}}
     \\
     && && cone(f)_\bullet &\to& X[1]_\bullet &\stackrel{f[1]_\bullet}{\to}& Y[1]_\bullet &\to& Z[1]_\bullet
     \\
     && && \downarrow^{\mathrlap{h_\bullet}}_{\mathrlap{\simeq}}
     \\
     X_\bullet 
       &\stackrel{f_\bullet}{\to}&
     Y_\bullet
       &\stackrel{}{\to}&
     Z_\bullet
  }
  \,.
$$

Observe that 

$$
  H_n( X[k]_\bullet) \simeq H_{n-k}(X_\bullet)
  \,.
$$

It is therefore sufficient to check that 

$$
  H_n
  \left(
    \array{
      cone(f)_\bullet &\to& X[1]_\bullet
      \\
      \downarrow^{\mathrlap{\simeq}}
      \\
      Z_\bullet
    }
  \right)
  \;\;
   : 
  \;\;
  H_n(Z_\bullet) \to H_n(cone(f)_\bullet) \to H_{n-1}(X_\bullet)
$$

equals the [[connecting homomorphism]] $\delta_n$ induced by the short exact sequence.

By prop. \ref{ConeInjectionEquivalentToZigzag} the inverse of the vertical map is given by choosing lifts and forming the corresponding element given by the connecting homomorphism.
By prop. \ref{ProjectionOutOfChainComplexMappingConeIsHoCofiber} the horizontal map is just the projection, and hence the assignment is of the form

$$
  [z_n] \mapsto [x_{n-1}, y_n] \mapsto [x_{n-1}]
  \,.
$$

So in total the image of the zig-zag under homology sends

$$
  [z_n]_Z \mapsto -[\partial^Y \hat z_n]_X
  \,.
$$

By the discussion [there](connecting%20homomorphism#OnHomologyInTermsOfElements), this is indeed the action of the [[connecting homomorphism]].

=--


### Distinguished triangles from mapping cones 
 {#DistinguishedTriangles}

In summary, the [above](#HomologyExactSequencesAndFiberSequences) says that for every [[chain map]] $f_\bullet : X_\bullet \to Y_\bullet$ we obtain maps

$$
  X_\bullet \stackrel{f}{\to}
  Y_\bullet
  \stackrel{
    \left(
      \array{
          0 
          \\
          id_{Y_\bullet}
      }
    \right)
  }{\to}
   cone(f)_\bullet
  \stackrel{
    \left(
      \array{
         id_{X[1]_\bullet} & 0
      }
    \right)
  }{\to}
  X[1]_\bullet
$$

which form a [[homotopy fiber sequence]] and such that this sequence continues by forming [[suspension of a chain complex|suspensions]], hence for all $n \in \mathbb{Z}$ we have

$$
  X[n]_\bullet \stackrel{f}{\to}
  Y[n]_\bullet
  \stackrel{
    \left(
      \array{
          0 
          \\
          id_{Y[n]_\bullet}
      }
    \right)
  }{\to}
   cone(f)[n]_\bullet
  \stackrel{
    \left(
      \array{
         id_{X[n+11]_\bullet} & 0
      }
    \right)
  }{\to}
  X[n+1]_\bullet
$$

To amplify this quasi-cyclic behaviour one sometimes depicts the situation as follows:

$$
  \array{
     X_\bullet &&\stackrel{f}{\to}&& Y_\bullet
     \\
     & {}_{\mathllap{[1]}}\nwarrow && \swarrow
     \\
     && cone(f)_\bullet
  }
$$

and hence speaks of a "triangle", or **distinguished triangle** or **mapping cone triangle** of $f$. 

* distinguished triangle = period of [[homotopy fiber sequence]] .

Due to these "triangles" one calls the [[homotopy category]] of chain complexes [[localization|localized]] at the [[quasi-isomorphisms]], hence the  [[derived category]], a **[[triangulated category]]**.

Notice that equivalently we can express the triangles via the 
[[mapping cylinder]].
For every map of [[chain complex]]es $f:A\to B$, the cylinder $Cyl(f)$ is quasi-isomorphic to $B$, and moreover in the [[homotopy category]] of chain complexes, every distinguished triangle is quasi-isomorphic to a distinguished triangle of the form 

$$ A\to Cyl(u)\to Cone(u)\to A[1]$$

for some $u:A\to B$ where all the morphisms in the triangle are appropriatedly induced by $u$. 

## Related concepts

[[!include universal constructions of topological spaces -- table]]


## References

In the context of [[chain complexes]]:

* {#Schapira} [[Masaki Kashiwara]], [[Pierre Schapira]], sections 4.2 & 7 of: _An Introduction to Categories and Homological Algebra_ (2024) &lbrack;[pdf](http://webusers.imj-prg.fr/~pierre.schapira/LectNotes/HA.pdf)&rbrack;
 
* {#Weibel} [[Charles Weibel]], section 1.5 of  _[[An Introduction to Homological Algebra]]_ .

In the context of [[spectra]]:

* {#Switzer75} [[Robert Switzer]], around 8. 17 of _Algebraic Topology - Homotopy and Homology_, Die  Grundlehren der Mathematischen Wissenschaften in Einzeldarstellungen, Vol. 212, Springer-Verlag, New York, N. Y., 1975. 

The above graphics is taken from

* {#Muro10} [[Fernando Muro]], _Representability of Cohomology Theories_, Joint Mathematical Conference CSASC 2010, 22–27 January 2010, Prague, Czech Republic ([slides](https://personal.us.es/fmuro/files/slides/praha.pdf))

[[!redirects mapping cones]]