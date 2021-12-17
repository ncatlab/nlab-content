
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

The notion of _monomorphism in an $(\infty,1)$-category_ is the generalization of the notion of [[monomorphism]] from [[category theory]] to [[(∞,1)-category]] theory. It is the special case of the notion of [[n-monomorphisms]] for $n = 1$. In an [[(∞,1)-topos]] every morphism factors by an [[effective epimorphism in an (∞,1)-category|effective epimorphism]] (1-epimorphism) followed by a monomorphism through its [[n-image|1-image]].

The dual concept is that of an [[epimorphism in an (∞,1)-category]].

There is also the concept [[regular monomorphism in an (∞,1)-category]], but beware that this need not be a special case of the definition given here.

There are also a notions of (homotopy) monomorphism in [[model categories]] and [[derivators]].

## Definition

For $\mathcal{C}$ an [[(∞,1)-category]], a [[morphism]] $f \colon Y \to Z$ is a **monomorphism** if regarded as an object in the [[over quasi-category|(∞,1)-overcategory]] $\mathcal{C}_{/Z}$ it is a [[n-truncated object in an (∞,1)-category|(-1)-truncated object]].

Equivalently this means that the projection

$$
  \mathcal{C}_{/f} \longrightarrow \mathcal{C}_{/Z}
$$

is a [[full and faithful (∞,1)-functor]]. This is in [Higher Topos Theory](#ref) after Example 5.5.6.13.

Equivalently this means that for every object $X \in C$ the induced morphism

$$
  \mathcal{C}(X,f) 
  \;\colon\; 
  \mathcal{C}(X,Y) 
    \longrightarrow
  \mathcal{C}(X,Z)
$$

of [[∞-groupoids]] is such that its image in the [[homotopy category of an (∞,1)-category|homotopy category]] exhibits $\mathcal{C}(X,Y)$ as a [[disjoint union|disjoint summand]] in a  [[coproduct]] decomposition of $\mathcal{C}(X,Z)$.

So if 

$$
  \mathcal{C}(X,Y) 
  \;=\; 
  \underset{i \in \pi_0\mathcal{C}(X,Y)}{\coprod} \mathcal{C}(X,Y)_{i }
  \;\;\;\;\;\;
  \text{and}
  \;\;\;\;\;\;
  \mathcal{C}(X,Z) 
  \;=\; 
  \underset{j \in \pi_0(\mathcal{C}(X,Z)}{\coprod} \mathcal{C}(X,Z)_j
$$ 

is the decomposition into [[connected components]], then there is an [[injective function]]

$$
  j 
    \,\colon\, 
  \pi_0 \mathcal{C}(X,Y) 
  \longrightarrow 
  \pi_0 \mathcal{C}(X,Z)
$$

such that $\mathcal{C}(X,f)$ is given by component maps $\mathcal{C}(X,Y)_i \to \mathcal{C}(X,Z)_{j(i)}$ which are each an equivalence.

## Properties

+-- {: .un_defn}
###### Definition

For $Z$ an [[object]] of $\mathcal{C}$, write $Sub(Z)$ 

$$
  Sub(Z) 
    \;\coloneqq\;
  \tau_{\leq -1}\big(  C_{/Z} \big)
  \,.
$$

for the category of [[subobjects in an (∞,1)-category|subobjects]] of $\mathcal{C}$.

=--

This is [[poset|partially ordered]] under inclusion.

+-- {: .un_prop}
###### Proposition


If $\mathcal{C}$ is a [[presentable (∞,1)-category]], then $Sub(Z)$ is a [[small category]].

=--

This appears as [[Higher Topos Theory|HTT, prop. 6.2.1.4]].

+-- {: .num_prop}
###### Proposition

Monomorphisms are stable under [[(∞,1)-pullback]]: if 

$$
  \array{
    A &\to& B
    \\
    {}^{\mathllap{f'}}\big\downarrow && \big\downarrow^{\mathrlap{f}}
    \\
    C &\to& D
  }
$$

is a pullback diagram and $f$ is a monomorphism, then so is $f'$.

=--

This is a special case of the general statement that $k$-[[truncated]] morphisms are stable under pullback. ([[Higher Topos Theory|HTT, remark 5.5.6.12]]).


+-- {: .num_prop}
###### Proposition

In an [[(∞,1)-topos]], monomorphisms are stable under [[(∞,1)-pushout]]: if 

$$
  \array{
    A &\to& B
    \\
    {}^{\mathllap{f}}\big\downarrow 
    && 
    \big\downarrow{}^{\mathrlap{f'}}
    \\
    C &\to& D
  }
$$

is a [[homotopy pushout]] diagram and $f$ is a monomorphism, then so is $f'$.

=--

([Rezk 19, p. 21](#Rezk19))



## Related pages

* The equivalence class of a monomorphism is a [[subobject in an (∞,1)-category]].

* The notion of monomorphism in an $(\infty,1)$-category can also be characterized in its underlying homotopy [[derivator]]; see [[monomorphism in a derivator]].

## References

The definition appears after example 5.5.6.13 in

* [[Jacob Lurie]], _[[Higher Topos Theory]]_{#ref}

with further discussion in section 6.2.

Lecture notes:


* {#Rezk19} [[Charles Rezk]], p. 10 of: _Lectures on Higher Topos Theory_, Leeds 2019 ([pdf](https://faculty.math.illinois.edu/~rezk/leeds-lectures-2019.pdf), [[RezkHigherToposTheory2019.pdf:file]])


For [[model categories]], see

* [[Fernando Muro]], _Homotopy units in A-infinity algebras_, [arXiv:1111.2723](http://arxiv.org/abs/1111.2723).

[[!redirects monomorphism in an (∞,1)-category]]
[[!redirects monomorphisms in an (∞,1)-category]]
[[!redirects monomorphisms in an (infinity,1)-category]]
[[!redirects homotopy monomorphism]]
[[!redirects homotopy monomorphisms]]
