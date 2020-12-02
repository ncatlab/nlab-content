

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

An **$(\infty,1)$-pullback**  is a [[limit in an (∞,1)-category]] $\mathcal{C}$ over a [[diagram]] of the shape

$$
  \{a \to c \leftarrow b\} \to \mathcal{C}
  \,.
$$

In other words it is a [[cone]]

$$
  \array{
    A \times_C B &\to& B
    \\
    \downarrow &\cong\swArrow& \downarrow
    \\
    A &\to& C
  }
$$

which is [[universal property|universal]] among all such cones in the $(\infty,1)$-categorical sense.

This is the analog in [[(∞,1)-category theory]] of the notion of [[pullback]] in [[category theory]]. 

## Incarnations

### In quasi-categories

Let $\mathcal{C}$ be a [[quasi-category]]. Recall the notion of [[limit in a quasi-category]].

The non-degenerate cells of the [[simplicial set]] $\Delta[1] \times \Delta[1]$ obtained as the [[cartesian product]] of the simplicial 1-[[simplex]] with itself look like

$$
  \array{
    (0,0) &\to& (1,0)
    \\
    \downarrow &\searrow& \downarrow
    \\
    (0,1) &\to& (1,1)
  }
$$

A **square** in a [[quasi-category]] $C$ is an image of this in $C$, i.e. a morphism

$$
  s : \Delta[1] \times \Delta[1] \to C
  \,.
$$

The simplicial square $\Delta[1]^{\times 2}$ is [[isomorphism|isomorphic]], as a [[simplicial set]], to the [[join of simplicial sets]] of a 2-[[horn]] with the point:

$$
  \Delta[1] \times \Delta[1]
  \simeq
  \{v\} \star \Lambda[2]_2
  = 
  \left(
  \array{
    v &\to& 1
    \\
    \downarrow &\searrow& \downarrow
    \\
    0 &\to& 2
  }
  \right)
$$

and

$$
  \Delta[1] \times \Delta[1]
  \simeq
  \Lambda[2]_0 \star \{v\}
  = 
  \left(
  \array{
    0&\to& 1
    \\
    \downarrow &\searrow& \downarrow
    \\
    2 &\to& v
  }
  \right)
  \,.
$$

If a square $\Delta[1] \times \Delta[1] \simeq \Lambda[2]_0 \star \{v\} \to C$ exhibits $\{v\} \to C$ as a [[limit in a quasi-category|quasi-categorical limit]] over $F : \Lambda[2]_0 \to C$, we say the limit

$$
  v := \lim_\leftarrow F := F(1) \prod_{F(0)} F(2)
$$

is [[generalized the|the]] **quasi-categorical pullback** of the diagram $F$.

#### Pasting law {#QuasiCatPastingLaw}

We have the following quasi-categorical analog of the familiar [pasting law of pullbacks](http://ncatlab.org/nlab/show/pullback#Pasting) in ordinary [[category theory]]:

A [[pasting]] diagram of two squares is a morphism

$$
  \sigma : \Delta[2] \times \Delta[1] \to \mathcal{c}
  \,.
$$

Schematically this looks like

$$
  \array{
     a &\to& b &\to& c
     \\
     \downarrow && \downarrow && \downarrow
     \\
     d &\to& e &\to& f
  }
$$

in $\mathcal{C}$.

+-- {: .un_prop}
###### Proposition
**(pasting law for quasi-categorical pullbacks)**

If the right square is a pullback diagram in $\mathcal{C}$, then the left square is precisely if the outer square is.

=--

This is [[Higher Topos Theory|HTT, lemma 4.4.2.1]]

+-- {: .proof}
###### Proof

Consider the diagram inclusions

$$
  \left(
    \array{
      && && c
      \\
      && && \downarrow
      \\
      d &\to& e &\to& f
    }
  \right)
  \;\;\to\;\;
  \left(
    \array{
      && b &\to& c
      \\
      && \downarrow && \downarrow
      \\
      d &\to& e &\to& f
    }
  \right)
  \;\;\leftarrow\;\;
  \left(
    \array{
      && b 
      \\
      && \downarrow
      \\
      d &\to& e
    }
  \right)
$$

and the induced diagram of [[over quasi-categories]]

$$
  \mathcal{C}_{/\sigma(c,d,f)}
  \stackrel{\phi}{\leftarrow} 
  \mathcal{C}_{/\sigma(b,c,d,e,f)}
  \stackrel{\psi}{\to}
  \mathcal{C}_{/\sigma(b,d,e)}
  \,.
$$

Notice that by definition of [[limit in a quasi-category]] the quasi-categorical pullback $\sigma(c) \times_{\sigma(f)} \sigma(d)$ is [[generalized the|the]] [[terminal object in a quasi-category|terminal object]] in $\mathcal{C}_{/\sigma(c,d,f)}$, while $\sigma(d) \times_{\sigma(e)} \sigma(b)$ is the terminal object in $\mathcal{C}_{/\sigma(b,d,e)}$. 

The strategy now is to show that both these morphisms $\phi$ and $\psi$ are acyclic [[Kan fibration]]s. That will imply that these terminal objects coincide as objects of $\mathcal{C}$.

First notice that the inclusion   

$$
  \left(
    \array{
      && b 
      \\
      && \downarrow
      \\
      d &\to& e
    }
  \right)
   \;\; \to \;\;
  \left(
    \array{
      && b &\to& c
      \\
      && \downarrow && \downarrow
      \\
      d &\to& e &\to& f
    }
  \right)
$$ 

is a [[left anodyne morphism]], being the composite of [[pushout]]s of left [[horn]] inclusions

$$
  \begin{aligned}  
  \left(
    \array{
      && b 
      \\
      && \downarrow
      \\
      d &\to& e
    }
  \right)
  & \to 
  \left(
    \array{
      && b &\to& c
      \\
      && \downarrow &&       
      \\
      d &\to& e
    }
  \right)
  \\
  & \to 
  \left(
    \array{
      && b &\to& c
      \\
      && \downarrow && \downarrow 
      \\
      d &\to& e && f
    }
  \right)
  \\
  & \to 
  \left(
    \array{
      && b &\to& c
      \\
      && \downarrow &\searrow& \downarrow 
      \\
      d &\to& e && f
    }
  \right)
  \\
  & \to 
  \left(
    \array{
      && b &\to& c
      \\
      && \downarrow &\searrow& \downarrow 
      \\
      d &\to& e &\to& f
    }
  \right)
 \end{aligned}
  \,.
$$

We could also prove this by showing that this functor is [[homotopy final functor|homotopy initial]] using the characterization in terms of slice categories, and then invoking the theorem of [[HTT]] 4.1.1.3(4) which says (in dual form) that an inclusion of simplicial sets is homotopy initial if and only if it is left anodyne.

One of the <a href="http://ncatlab.org/nlab/show/right%2Fleft+Kan+fibration#PropRightAnodyne">properties of left anodyne morphisms</a> is that restriction of [[over quasi-categories]] along left anodyne morphisms produces an acyclic [[Kan fibration]]. This shows the desired statement for $\psi$.

To see that $\phi$ is also an acyclic fibration observe that 
$\phi$ can be factored as 

$$ 
\mathcal{C}_{/\sigma(c,d,f)} \leftarrow 
\mathcal{C}_{/\sigma(c,d,e,f)} \leftarrow 
\mathcal{C}_{/\sigma(b,c,d,e,f)} 
$$

Observe that $\mathcal{C}_{/\sigma(c,d,e,f)}\leftarrow\mathcal{C}_{/\sigma(b,c,d,e,f)}$ 
fits into a pullback diagram  

$$ 
   \array{
      \mathcal{C}_{/\sigma(c,d,e,f)} 
      & \leftarrow &
      \mathcal{C}_{/\sigma(b,c,d,e,f)} \\ 
      \downarrow & & \downarrow \\ 
     \mathcal{C}_{/\sigma(c,e,f)} 
     & \leftarrow & 
     \mathcal{C}_{/\sigma(b,c,e,f)} 
    }
$$

and hence is an acyclic Kan fibration since 
$\mathcal{C}_{/\sigma(c,e,f)} \leftarrow \mathcal{C}_{/\sigma(b,c,e,f)}$ 
is one, on account of the fact that the square 

$$ 
   \array{ 
        \sigma(b) & \to & \sigma(c) \\ 
        \downarrow & & \downarrow \\ 
        \sigma(e) & \to & \sigma(f) 
   } 
$$ 

is a pullback in $\mathcal{C}$.  Finally, 
$\mathcal{C}_{/\sigma(c,d,f)} \leftarrow \mathcal{C}_{/\sigma(c,d,e,f)}$ 
is a trivial fibration since 

$$ 
   \array{ 
      \left( 
          \array{ 
              & & c \\ 
              & & \downarrow \\ 
           d & \to & f 
          } 
     \right) & \to & 
     \left( 
        \array{
           & & & & c \\ 
           & & & & \downarrow \\ 
         d & \to & e & \to & f 
         }
     \right) 
   }
$$

is left anodyne; clearly this is a pushout of 
$(d\to f)\to (d\to e\to f)$ and so it suffices to show 
that $\Delta^{\{0,2\}}\to \Delta^{\{0,1,2\}}$ is left 
anodyne.  But this map factors as 
$\Delta^{\{0,2\}}\to \Lambda^2_0 \to \Delta^{\{0,1,2\}}$ 
and clearly $\Delta^{\{0,2\}}\to \Lambda^2_0$ is left 
anodyne since it is a pushout of $\Delta^{\{0\}}\to 
\Delta^{\{0,1\}}$.  

=--



### In model categories

* [[homotopy pullback]]

### In derivators

* [[pullback in a derivator]]


## Examples

### Fiber sequence

If $\mathcal{C}$ has a [[terminal object]] and $* \to C \in \mathcal{C}$ is a [[pointed object]], then the **fiber** or **$(\infty,1)$-kernel** of a morphisms $f : B \to C$ is the $(\infty,1)$-pullback

$$
  \array{
    ker(f) &\to& *
    \\
    \downarrow && \downarrow
    \\
    B &\stackrel{f}{\to}& C
  }
  \,.
$$

For more on this see [[fiber sequence]].


## Related concepts

[[!include notions of pullback -- contents]]


## References

### In homotopy type theory

A formalization of homotopy pullbacks in [[homotopy type theory]] is [[Coq]]-coded in 

* [[Guillaume Brunerie]], _[Hott/Coq/Limits/Pullbacks.v](https://github.com/guillaumebrunerie/HoTT/blob/master/Coq/Limits/Pullbacks.v)_ 



[[!redirects (∞,1)-pullback]]
[[!redirects (infinity,1)-pullbacks]]
[[!redirects (∞,1)-pullbacks]]

[[!redirects (∞,1)-fiber product]]
[[!redirects (∞,1)-fiber products]]

[[!redirects (infinity,1)-fiber product]]
[[!redirects (infinity,1)-fiber products]]

