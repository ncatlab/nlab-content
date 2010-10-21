

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
=--
=--

#Contents#
* automatic table of contents goes here
{:toc}

## Idea

A [[sheaf]] $F$ on (the [[site]] [[category of open subsets|of open subsets]] of) a [[topological space]] $X$ corresponds to an [[étalé space]] $\pi_F : Y_F \to X$.  This space $Y_F$ has itself a [[sheaf topos]] associated to it, and the map $Y_F \to X$ induces a [[geometric morphism]] of [[sheaf topos]]es

$$
  \pi_F : Sh(Y_F) \to Sh(X)
  \,.
$$

Due to the special nature of $Y_F$, the topos on the left is equivalent to the [[overcategory]] topos $Sh(X)/F$, and the projection morphism above factors through a canonical standard [[geometric morphism]] $Sh(X)/F \to Sh(X)$

$$
  \pi_F : Sh(Y_F) \stackrel{\simeq}{\to} Sh(X)/F \to Sh(X)
  \,.
$$

And conversely, every [[local homeomorphism]] $Y \to X$ of [[topological space]]s corresponds to a [[geometric morphism]] of sheaf toposes of this form.

This motivates calling a [[geometric morphism]]

$$
  \mathcal{X} \to \mathcal{Y}
$$

a **local homeomorphism of toposes** or **&#233;tale geometric morphism** if it factors as an equivalence followed by a projection out of an overcategory topos.

If the topos is a locally ringed topos, or moro generally a [[structured (∞,1)-topos]], it makes sense to require additionally that the local homeomorphism is compatible with the extra structure.

## Definition

For $\mathbf{H}$ a [[topos]] (or [[(∞,1)-topos]], etc.) and for $X \in \mathbf{H}$ an [[object]], the [[overcategory]] $\mathbf{H}_{/X}$ is also a topos ($(\infty,1)$-topos, etc). This is sometimes called the [[petit topos]] associated to $X \in \mathbf{H}$.

The canonical projection $\pi_! : \mathbf{H}_{/X} \to \mathbf{H}$ is part of an [[essential geometric morphism|essential]] (in fact, [[locally connected geometric morphism|locally connected]]) geometric morphism:

$$
  \pi = (\pi_! \dashv \pi^* \dashv \pi_*) : 
  \mathbf{H}_{/X}
   \stackrel{\overset{\pi_!}{\to}}{\stackrel{\overset{\pi^*}{\leftarrow}}{\underset{\pi_*}{\to}}}
  \mathbf{H}
  \,.
$$

This is the [[base change geometric morphism]] for the terminal morphism $X \to *$.

### For toposes

+-- {: .un_defn}
###### Definition
A [[geometric morphism]] $\mathbf{K} \to \mathbf{H}$ is called a
**local homeomorphism of toposes**, or an **&#233;tale geometric morphism**, if it is equivalent to such a projection--- in other words, if it factors by geometric morphisms as $\mathbf{K} \stackrel{\simeq}{\to} \mathbf{H}_{/X} \stackrel{\pi}{\to} \mathbf{H}$ for some $X \in \mathbf{H}$ .
=--

### For structured toposes

If the [[(∞,1)-topos]]es in question are [[structured (∞,1)-topos]]es, then this is refined to the following

+-- {: .un_defn}
###### Definition

A morphism $f : (\mathcal{X}, \mathcal{O}_{\mathcal{X}}) \to (\mathcal{Y}, \mathcal{O}_{\mathcal{Y}})$ of [[structured (∞,1)-topos]]es is an **&#233;tale morphism** if

1. the underlying morphism of $(\infty,1)$-toposes is an &#233;tale geometric morphism;

1. the induced map $f^* \mathcal{O}_\mathcal{Y} \to \mathcal{O}_\mathcal{X}$
   is an equivalence.


=--

This is [[Structured Spaces|StSp, Def. 2.3.1]].



## Examples

If $\mathbf{H}$ is a [[localic topos]] $Sh(S)$ over a [[topological space]] $S$ we have that $X \in Sh(S)$ corresponds to an [[étalé space]] over $X$ and $\mathbf{H}/X \to \mathbf{H}$ to an [[étale map]].


If $\mathcal{G}$ is a [[geometry (for structured (∞,1)-toposes)]] 
then for $f : U \to X$ an _admissible_ morphism in $\mathcal{G}$, 
the induced morphism of [[structured (∞,1)-topos]]es

$$
  Spec^\mathcal{G} U \to Spec^{\mathcal{G}} X
$$

is an &#233;tale geometric morphism of structured $(\infty,1)$-toposes.

This is [[Structured Spaces|StrSp, example 2.3.8]]. 







  

## Properties

+-- {: .un_prop}
###### Proposition
**(recognition of &#233;tale geometric morphisms)**

A [[geometric morphism]] $(f^* \dashv f_*) : \mathbf{K} \to \mathbf{H}$ is &#233;tale precisely if

1. it is [[essential geometric morphism|essential]];

1. $f_!$ is a [[conservative functor]];

1. For every [[diagram]] $X \to Y \leftarrow f_! Z$ in $\mathbf{H}$ the
   induced diagram

   $$
     \array{
       f_!(f^* X \times_{f^* Y} Z) &\to& f_! Z
       \\
       \downarrow && \downarrow
       \\
       X &\to& Y
     }
   $$

   is a [[pullback]] diagram.

=--

For [[(∞,1)-topos]]es this is [[Higher Topos Theory|HTT, prop. 6.3.5.11]].

## References

The notion of local homeomorphisms of toposes is page 651 (chapter C3.3) of

* [[Peter Johnstone]], _[[Elephant|Sketches of an Elephant]]_ .

The notion of &#233;tale geometric morphisms between [[(∞,1)-topos]]es is introduced in section 6.3.5 of 

* [[Jacob Lurie]], _[[Higher Topos Theory]]_ .

Discussion of the refinement to [[structured (∞,1)-topos]]es is in section 2.3 of

* [[Jacob Lurie]], _[[Structured Spaces]]_ .
 

[[!redirects etale geometric morphism]]
[[!redirects etale geometric morphisms]]
[[!redirects étale geometric morphism]]
[[!redirects étale geometric morphisms]]
[[!redirects locally homeomorphic geometric morphism]]
[[!redirects local homeomorphism of toposes]]
[[!redirects local homeomorphism of topoi]]
