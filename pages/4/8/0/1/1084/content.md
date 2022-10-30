
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

The _mapping cone_ of a [[morphism]] $f : X \to Y$ in some [[homotopical caetgory]] (precisely: a [[categor of cofibrant objects]]) is, if it exists, a particular representative of the [[homotopy fiber|homotopy cofiber]] of $f$. 

It is also called the _homotopy [[cokernel]]_ of $f$ or the _[[weak quotient]]_ of $Y$ by the [[image]] of $X$ in $Y$ under $f$. 

The dual notion is that of [[mapping cocone]].


## Definition

In an [[(∞,1)-category]] the [[homotopy fiber|homotopy cofiber]] of a [[morphism]] $f : X \to Y$ is the [[homotopy pushout]]

$$
  \array{
     X &\stackrel{}{\to}& {*}
     \\
     \downarrow^f && \downarrow
     \\
     Y &\to& coker(f)
  }
  \,.
$$

When the [[(∞,1)-category]] is [[presentable (∞,1)-category|presented]] by a [[category of fibrant objects|category of cofibrant objects]] (for instance a  [[model category]] with only cofibrant objects) then this may be computed by the ordinary [[colimit]] 

$$
  \array{
    && X &\stackrel{f}{\to}& Y
    \\
    && \downarrow^{i_1} && \downarrow
    \\
    X &\stackrel{i_0}{\to}& Cyl(X)
    \\
    \downarrow && &\searrow & \downarrow
    \\
    {*} &\to& &\to& coker(f) 
  }
$$

using a [[cylinder object]] $Cyl(X)$ for $X$, that models the [[left homotopy]] filling the original homotopy pushout diagram. This colimit, in turn, may be computed in two stages by two consecutive [[pushout]]s as

$$
  \array{
    && X &\stackrel{f}{\to}& Y
    \\
    && \downarrow^{i_1} && \downarrow
    \\
    X &\stackrel{i_0}{\to}& Cyl(X)
    \\
    \downarrow && \downarrow 
    \\
    {*} &\to& cone(X) &\to& coker(f) 
  }
  \,.
$$

The first [[pushout]] here 

$$
  \array{
     X &\stackrel{i_0}{\to}& Cyl(X)
     \\
     \downarrow && \downarrow
     \\
     {*} &\to& cone(X)
  }
$$

is  the **cone** over $X$: the result of taking the [[cylinder object|cylinder]] over $X$ and identifying one $X$-shaped end with the [[point]].

The remaining [[pushout]]

$$
  \array{
    X &\stackrel{f}{\to}& Y
    \\
    \downarrow && \downarrow
    \\
    cone(X) &\to& coker(f) & =: cone(f)
  }
$$

is the **mapping cone** of $f$:

this is the result of taking that _other_ remaining end of the cyclinder and gluing that to $Y$, using the identification given by $f$.

The geometric intuition behind this is best seen in the archetypical example of the [[model category]] [[Top]]. See the examples below.


## Examples

### Suspension 

The mapping cone of the morphism $X \to {*}$ to the [[terminal object]] is the [[suspension object]] $\Sigma X$ of an object $X$. The dual notion of the [[loop space object]] of $X$.

### For topoligical space

The construction is geometrically most obvious in the category [[Top]] of [[topological spaces]].

Here for $I = [0,1]$ the standard [[interval object]] we may take the [[cylinder object]] to be $Cyl(X) = X \times I$, literally the cylinder over $X$. 

Given a continuous map $f:X\to Y$, the 
[[topological space]] $cone(f)$ is

$$
  X\times I \cup_{f} Y
$$

(here for all $x\in X$, $(x,1)$ is identified with $f(x)$) modulo the contraction of $X\times \{0\}$ to a point. The opposite convention is also possible: identify $(x,0)$ with $f(x)$ for all $x$ and then contract $X\times\{1\}$ to a point; the two constructions of cones are canonically homeomorphic; the first is sometimes called the "inverse mapping cone".

Singular chain complex functor from [[Top]] to the 
[[category of chain complexes]] of abelian groups sends the mapping cone to a mapping cone in the sense of chain complexes (up to conventions on the orientation of the interval and vector order in the definition of mapping cone of chain complexes). 


### In additive categories with translation

Let $C$ be an [[additive category]] [[category with translation|with translation]] $T=[1] : C \to C$. Let $X$ and $Y$ be two [[differential object]]s in $(C,T)$ and $f : X \to Y$ any [[morphism]] in $C$. 

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

### In chain complexes
 {#InChainComplexes}


(...)

### In cochain complexes
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
