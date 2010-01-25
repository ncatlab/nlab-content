

#Contents#
* automatic table of contents goes here
{:toc}


## Idea

In an [[(∞,1)-category]] $C$ with $(\infty,1)$-[[pullback]]s, the _free loop space object_ $\mathcal{L}X$ of any object $X$ is an object that behaves as if its [[generalized element]]s are loops in $X$, morphisms between generalized elements [[homotopy|homotopies]] of loops, and so on.

For the case that $C = $ [[Top]] this reproduces the ordinary notion of free [[loop space]] objects of [[topological space]]s.

Over each fixed element $x \in X$, the free loop space object $\mathcal{L}X$ looks like the based [[loop space object]] $\Omega_x X$ of $X$.

Free loop space objects come naturally equipped with various structures of interest, such as a categorical circle action. The [[cohomology]] of $\mathcal{L}X$ is [[Hochschild cohomology]] or [[cyclic cohomology]] of function algebras $C(X)$ on $X$. The categorical circle action induces [[differential]]s on these cohomolgies, identifying them, in suitable cases, with algebras of [[Kähler differential|Kähler]] [[differential form]]s on $X$.


## Definition

### Intrinsic $(\infty,1)$-categorical definition

+-- {: .un_defn}
###### Definition

In an [[(∞,1)-category]] $C$, for $X \in C$ an [[object]], its **free loop space object** $\mathcal{L}X$ is the $(\infty,1)$-[[pullback]]

$$
  \array{
    \mathcal{L} X &\to& X
    \\
    \downarrow && \downarrow^{\mathrlap{(Id,Id)}}
    \\
    X &\stackrel{(Id,Id)}{\to}& X \times X
  }
  \,.
$$

=--

This is the $(∞,1)$-categorical [[span trace]] of the identity-[[span]]

$$
  \mathcal{L}X =
  Tr
  \left(
    \array{
       && X
       \\
       & {}^{\mathllap{Id}}\swarrow && \searrow^{\mathrlap{Id}}
       \\
       X &&&& X
    }
  \right)
  \,.
$$


### Models by homotopy pullbacks

To see what this amounts to in more detail, assume that the [[(∞,1)-category]] is modeled by a [[homotopical category]], say for simplicity a [[category of fibrant objects]], for instance the full subcategory on fibrant objects of a [[model category]]. 

Then following the discussion at [[homotopy pullback]] and [[generalized universal bundle]] we can compute the about $(\infty,1)$-pullback as the ordinary [[limit]] 

$$
  \array{
    \mathcal{L}X &\to& &\to& X
     \\
    \downarrow && && \downarrow^{\mathrlap{(Id,Id)}}
    \\
    && (X \times X)^I &\stackrel{(d_0,d_0)}{\to}& X \times X
    \\
    \downarrow &&  {}^{\mathllap{(d_1,d_1)}}\downarrow
    \\
    X &\stackrel{(Id,Id)}{\to} &  X \times X
    \,,
  }
$$

where $(X\times X)^I$ is a [[path space object]] for $X \times X$.  At least if we have the structure of a [[model category]] we may take $(X \times X)^I = X^I \times X^I$ for a [[path space object]] $X^I$ of $X$. 

From this description one sees that $\mathcal{L}X$ is built from _pairs of paths_ in $X$ with coinciding endpoints, that are _glued at their coinciding endpoint_ . So the loops here are all built from two semi-ciricle paths.


## Properties

### Relation to based loop space object

The fiber of $\mathcal{L}X$ over a [[point]] $x : {*} \to X$ is the corresponding (based) [[loop space object]] $\Omega_x X$ of $X$: we have an $(\infty,1)$-[[pullback]] diagram

$$
  \array{
    \Omega_x X &\to& \mathcal{L}X &\to& X
    \\
    \downarrow && \downarrow && \downarrow^{\mathrlap{(Id,Id)}} 
    \\
    {*} &\stackrel{x}{\to} & X &\stackrel{(Id,Id)}{\to}& X\times X
  }
  \,.
$$

To see this, use that [[homotopy pullback]]s paste to homotopy pullbacks, so that the outer pullback is modeled by the ordinary [[limit]]

$$
  \array{
    \Omega_x^{I \vee I}X &\to& &\to& X
     \\
    \downarrow && && \downarrow^{\mathrlap{(Id,Id)}}
    \\
    && (X \times X)^I &\stackrel{(d_0,d_0)}{\to}& X \times X
    \\
    \downarrow &&  {}^{\mathllap{(d_1,d_1)}}\downarrow
    \\
    {*} &\stackrel{(x,x))}{\to} &  X \times X
    \,,
  }
$$

which builds based loops on $X$ from two consecutive paths, the first starting at the basepoint $x$, the second ending there. This is weakly equivalent $\Omega_x X = \Omega^I_x X \stackrel{\simeq}{\to} \Omega^{I \vee I} X$ to the based [[loop space object]] $\Omega_x X$ built from just the path space object $X^I$ with a single copy of $I$, by standard arguments as for instance form page 12 on in 

* Ken Brown, _[[BrownAHT|Abstract Homotopy Theory and Generalized Sheaf Cohomology]]_ .



### Hochschild cohomology and cyclic cohomology

[[quasicoherent ∞-stack]]s on $\mathcal{L}X$ form the [[Hochschild cohomology|Hochschild homology]] object of $X$ (if the axioms of [[geometric function theory]] are met) as described there. The circle acton on $\mathcal{L}X$ induces differentials on these.

> ... details to be written, but see [[Hochschild cohomology]] and [[cyclic cohomology]] for more.




## Examples 

### Free topological loop spaces

* From the above [[limit]] description we see that in [[Top]] this yields a version for the ordinary free loop space of a [[topological space]].


### Details for $\mathcal{L} \mathbf{B}G$

Let the ambient [[(∞,1)-category]] be [[∞Grpd]], let $G$ be an ordinary [[group]] and $\mathbf{B}G$ its one-object [[delooping]] [[groupoid]]. 

+-- {: .un_prop}
###### Proposition

We have 

$$
  \mathcal{L} \mathbf{B}G \simeq G//_{Ad} G
  \,,
$$

the [[action groupoid]] of the adjoint action of $G$ on itself.

=--


+-- {: .proof}
###### Proof

We spell this out in full pedestrian detail, as a little exercise in computing [[homotopy pullback]]s.

We have that the [[path space object]] is $\mathbf{B}G^I = [I,\mathbf{B}G]$ -- the [[functor category|functor groupoid]], where $I$ is the free groupoid $I = \{a \stackrel{\simeq}{\to} b\}$ on the standard [[interval object]] -- which is (by the definition of [[natural transformation]]) the [[action groupoid]]

$$
  \mathbf{B}G^I = G\backslash \backslash G // G
$$

for the action of $G$ on itself, by _inverse_ left and direct right multiplication separately: the naturality square of a [[natural transformation]] defining a morphism $g \stackrel{h_1,h_2}{\to} h_1^{-1} g h_2$ in this groupoid is the commuting square

$$
  \array{
    \bullet &\stackrel{g}{\to}& \bullet
    \\  
    {}^{\mathllap{h_1}}\downarrow && \downarrow^{\mathrlap{h_2}}
    \\
    \bullet &\stackrel{h_1^{-1}g h_2}{\to}& \bullet    
  }
$$

in $\mathbf{B}G = {*}//G$.

The [[pullback]] of the top right corner of the above defining limit diagram is

$$
  \array{
    (G\backslash\backslash G \times 
    G\backslash\backslash G)//G
    &\to& \mathbf{B}G
    \\
    \downarrow && \downarrow^{\mathrlap{(Id,Id)}} 
    \\
    (G\backslash\backslash G//G) \times
    (G\backslash\backslash G//G)
    &\to& \mathbf{B}G \times \mathbf{B}G
  }
$$

identifying the two actions from the right, and then the remaining pullback completing the limit diagram is

$$
  \array{
    G\backslash\backslash (G\times G)//G
    &\to& 
    (G\backslash\backslash G \times 
    G\backslash\backslash G)//G
    \\
    \downarrow && \downarrow
    \\
    \mathbf{B}G &\stackrel{(Id,Id)}{\to}&  
    \mathbf{B}G \times \mathbf{B}G
  }
$$

now identifying also the two actions from the left, so that  $G\backslash\backslash (G\times G)//G$ is the [[action groupoid]] of $G$ acting diagonally on $G \times G$ by multiplication from the left and from the right, separately.

To see better what this is, we pass to an equivalent smaller groupoid (the [[homotopy pullback]] is defined, of course, only up to weak equivalence). Notice that every morphism 
$(g_1,g_2) \stackrel{h_1,h_2}{\to} (g'_1, g'_2)$ 
in $G\backslash\backslash (G\timees G)//G$ corresponding to a [[natural transformation]]

$$
  \array{
     \bullet &\stackrel{(g_1,g_2)}{\to}& \bullet
     \\
     {}^{\mathllap{(h_1,h_1}}\downarrow && \downarrow^{\mathrlap{(h_2,h_2)}}
     \\
     \bullet &\stackrel{(h_1^{-1} g_1 h_2, h_1^{-1} g_2 h_2)}{\to}
     & \bullet
  }
$$

between functors $I\times I \to \mathbf{B}G \times \mathbf{B}G$
may always be decomposed as

$$
  \array{
     \bullet &\stackrel{(g_1,g_2)}{\to}& \bullet
     \\
     {}^{\mathllap{(e,e}}\downarrow 
     && \downarrow^{\mathrlap{(g_2^{-1}, g_2^{-1})}}
     \\
     \bullet &\stackrel{(g_1 g_2^{-1}, e)}{\to}& \bullet
     \\
     {}^{\mathllap{(h_1,h_1}}\downarrow 
     && \downarrow^{\mathrlap{(h_1,h_1)}}
     \\
     \bullet &\stackrel{(h_1^{-1}(g_1 g_2^{-1})h_1, e)}{\to}& \bullet
     \\
     {}^{\mathllap{(e,e}}\downarrow 
     && \downarrow^{\mathrlap{(g'_2,g'_2)}}
     \\
     \bullet &\stackrel{(h_1^{-1}(g_1 g_2^{-1})h_1 g'_2, g'_2)}{\to}& \bullet
  }
  \,.
$$

Staring at this for a moment shows that this is a unique factorization of every morphism through one of the form

$$
  \array{
    \bullet & \stackrel{(g,e)}{\to} & \bullet
    \\
    {}^{\mathllap{k}}\downarrow && \downarrow^{mathrlap{k}}
    \\
    \bullet & \stackrel{(Ad_k g,e)}{\to} & \bullet    
  }
  \,,
$$

which is naturally identified with a morphism in the [[action groupoid]] $G//_{Ad} G$ of the adjoint action of $G$ on itself.

This means that the inclusion

$$
  G//_{Ad} G 
  \stackrel{}{\hookrightarrow}
  G\backslash\backslash(G \times G)//G
$$

given by this identification
is [[essentially surjective functor|essentially surjective]] and [[full and faithful functor|full and faithful]], and hence an [[equivalence of categories|equivalence of groupoids]].

So in conclusion we have that the free loop space object of the [[delooping]] $\mathbf{B}G$ of a group is

$$
  \mathcal{L} \mathbf{B}G \simeq G//_{Ad}G
  \,.
$$

=--
