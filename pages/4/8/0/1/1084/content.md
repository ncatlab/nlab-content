
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


## Definition
 {#Definition}

The mapping cone construction is a means to _present_ in a [[category with weak equivalences]] the following canonical
construction in [[homotopy theory]]/[[(∞,1)-category theory]].

+-- {: .num_defn }
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

+-- {: .num_prop }
###### Proposition

If the [[(∞,1)-category]] $\mathcal{C}$ is presented by (is [[equivalence of (infinity,1)-categories|equivalent]] to the [[simplicial localization]] of) a [[category of cofibrant objects]] $C$ (for instance given by the [[cofibrant objects]] in a [[model category]]) then this homotopy cofiber is presented by the ordinary [[colimit]] 

$$
  \array{
    && X &\stackrel{f}{\to}& Y
    \\
    && \downarrow^{\mathrlap{i_1}} && \downarrow
    \\
    X &\stackrel{i_0}{\to}& cyl(X)
    \\
    \downarrow && &\searrow & \downarrow
    \\
    {*} &\to& &\to& coker(f) 
  }
$$

in $C$ using any [[cylinder object]] $cyl(X)$ for $X$.

=--

This is discussed at [[factorization lemma]] and at [[homotopy pullback]].


+-- {: .num_prop }
###### Proposition

This colimit, in turn, may be computed in two stages by two consecutive [[pushouts]] in $C$, and in two ways by the following [[pasting diagram]]:

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
    cyl(x) &\to& cyl(f)
    \\
    \downarrow && \downarrow
    \\
    cone(X) &\to& cone(f)
  }
$$

defines es the **mapping cone** $cone(f)$ of $f$: the result of forming the cyclinder over $X$ and then identifying one end with the point and the other with $Y$, via $f$.

=--

The geometric intuition behind this is best seen in the archetypical example of the [[model category]] [[Top]]. See the example _[For topological spaces](#ForTopologicalSpaces)_ below. The example _[For chain complexes](InChainComplexes)_ can be understood similarly geometrically by thinking of all chain complexes as [[singular chain complex|singular chains]] on topological spaces.


## Examples

We discuss realizations of the general construction in various contexts.
Some of these examples are regarded in parts of the literature as the default examples, notably that [for topological spaces](#ForTopologicalSpaces) and that [for chain complexes](#InChainComplexes).

### Suspension 

The mapping cone of the morphism $X \to {*}$ to the [[terminal object]] is the [[suspension object]] $\Sigma X$ of an object $X$. The dual notion of the [[loop space object]] of $X$.

### For topological spaces
 {#ForTopologicalSpaces}

The notion _mapping cone_  derives its name from its geometrica 
interpretation in the category [[Top]] of [[topological spaces]].

With respect to the standard [[model structure on topological spaces]] every [[CW-complex]] is a cofibrant object, and hence mapping cones on maps between CW-complexes have intrinsic meaning in [[homotopy theory]].

Write $I \coloneqq [0,1] \subset \mathbb{R} \in $ [[Top]] for the standard topological interval. This is an [[interval object]] for the standard model structure. We may therefore take the [[cylinder object]] of a topological space $X$ to be 

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

Let $I_\bullet \in Ch_{\bullet}(\mathcal{A})$ be given by

$$
  I_\bullet
  = 
  (\cdots 0 \to 0 \to R \stackrel{(-id,id)}{\to} R \oplus R)
  \,.
$$

=--


+-- {: .num_remark }
###### Remark

This is the standard [[interval object in chain complexes]].

It is in fact the [[normalized chain complex]] of [[chains on a simplicial set]] for the canonical simplicial interval, the 1-[[simplex]]:

$$
  I_\bullet = C_\bullet(\Delta[1])
  \,.
$$

The [[differential]] $\partial^I = (id, -id)$ here expresses the [[alternating face map complex]] [[boundary]] operator, which in terms of the three non-degenerate [[basis]] elements is given by

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
      & -\partial^X
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

One part of definition \ref{CylindersAndCones} now reads:

+-- {: .num_defn }
###### Definition

For $f_\bullet : X_\bullet \to Y_\bullet $ a [[chain map]],
the [[mapping cylinder]] $cyl(f)$ is the [[pushout]]

$$
  \array{
    cyl(f) &\leftarrow& Y
    \\
    \uparrow && \uparrow^{\mathrlap{f}}
    \\
    X \otimes I &\stackrel{i_0}{\leftarrow}& X
  }
  \,.
$$

=--

+-- {: .num_prop }
###### Proposition

The components of $cyl(f)$ are

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
      \partial^Y_n & f_n
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

(...)
see at [[homology exact sequence]]
(...)


### Distinguished triangles from mapping cones 

A [[homotopy category]] of the [[category of chain complexes]] (with respect to chain [[homotopy equivalence]]s) has a natural structure of a [[triangulated category]] where the distinguished triangles are the triangles isomorphic to **mapping cone triangle**s

$$
  A \stackrel{f}{\to}
  B
  \stackrel{
    \left(
      \array{
          0 
          \\
          Id_B
      }
    \right)
  }{\to}
   Cone(f)
  \stackrel{
    \left(
      \array{
         Id_{A[1]} & 0
      }
    \right)
  }{\to}
  A[1]
  \,.
$$

For every map of [[chain complex]]es $f:A\to B$, the cylinder $Cyl(f)$ is quasi-isomorphic to $B$, and moreover in the [[homotopy category]] of chain complexes, every distinguished triangle is quasi-isomorphic to a distinguished triangle of the form 

$$ A\to Cyl(u)\to Cone(u)\to A[1]$$

for some $u:A\to B$ where all the morphisms in the triangle are appropriatedly induced by $u$. 


## References

In the context of [[chain complexes]] the construction is discussed for instance in section 1.5 of 

* [[Charles Weibel]], _[[An Introduction to Homological Algebra]]_ .

[[!redirects mapping cones]]
