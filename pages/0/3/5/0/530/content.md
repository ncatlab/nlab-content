
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The notion of _$k$-surjective functor_ is the continuation of the sequence of notions

* [[essentially surjective functor]]

* essentially surjective and [[full functor]]

* essentially surjective and [[full and faithful functor]]

from [[category theory]] to an infinite sequence of notions in [[higher category theory]].

Roughly, a functor $F : C \to D$ between [[∞-categories]] $C$ and $D$ is _$k$-surjective_ if for each boundary of a [[k-morphism]]s in $C$, each $k$-morphism between the image of that boundary in $D$ is in the image of $F$.


## Generalization to $\infty$-categories

### $k$-Surjectivity

For the moment, this here describes the notion for _globular_ models of $\infty$-categories. See below for the simplicial reformulation.

An $\omega$-functor $f : C \to D$ between $\infty$-[[infinity-category|categories]] is 
0-surjective if $f_0 : C_0 \to D_0$ is an epimorphism.

For $k \in \mathbb{N}$, $k \geq 1$ the functor is _$k$-surjective_ 
if the universal morphism 
$$
  C_k \to P_k
$$
to the pullback $P_k$ in
$$
  \array{
     P_k
     &\to&
     D_k
     \\
     \downarrow && \downarrow^{s \times t}
     \\
     C_{k-1} \times C_{k-1}
     &\stackrel{F_{k-1} \times F_{k-1}}{\to}&
     D_{k-1} \times D_{k-1}
  }
$$
coming from the commutativity of the square
$$
  \array{
     C_k
     &\stackrel{f_{k}}{\to}&
     D_k
     \\
     \downarrow^{s \times t} && \downarrow^{s \times t}
     \\
     C_{k-1} \times C_{k-1}
     &\stackrel{F_{k-1} \times F_{k-1}}{\to}&
     D_{k-1} \times D_{k-1}
  }
$$
(which commutes due to the functoriality axioms of $f$) is an [[epimorphism]].

If you interpret $C_k$ and $P_k$ as sets and take 'epimorphism' in a strict sense (the sense in [[Set]], a [[surjection]]), then you have a __strictly $k$-surjective functor__.  But if you interpret $C_k$ and $P_k$ as $\infty$-categories or $\infty$-groupoids and take 'epimorphism' in a weak sense (the [[homotopy limit|homotopy]] sense from $\infty$-[[infinity-Grpd|Grpd]]), then you have an __essentially $k$-surjective functor__; equivalently, project $C_k$ and $P_k$ to $\omega$-[[equivalence]]-classes before testing surjectivity.  A functor is essentially $k$-surjective if and only if it is equivalent to some strictly $k$-surjective functor, so essential $k$-surjectivity is the notion that respects the [[principle of equivalence]].


+-- {: .un_prop}
###### Proposition

For $C$ and $D$ [[categories]] we have

 1. $f$ is (essentially) $0$-surjective $\Leftrightarrow$
    $f$ is [[essentially surjective functor|(essentially) surjective on objects]];
 2. $f$ is (essentially) $1$-surjective $\Leftrightarrow$ $f$ is [[full functor|full]];
 3. $f$ is (essentially) $2$-surjective $\Leftrightarrow$ $f$ is [[faithful functor|faithful]];
 4. $f$ is always $3$-surjective.
=--


### In terms of lifting diagrams {#Lifting}

+-- {: .un_prop}
###### Proposition

An $\omega$-functor $f : C \to D$ is $k$-surjective for $k \in \mathbb{N}$ precisely if it has the right [[weak factorization system|lifting property]] with respect to the inclusion $\partial G_{k} \to G_k$ of the boundary of the $k$-[[globe]] into the $k$-[[globe]].

$$
  \array{
    \partial G_k &\to& C
    \\
    \downarrow &{}^{\exists}\nearrow& \downarrow^f
    \\
    G_k &\to& D
  }
  \,.
$$
=--


One recognizes the similarity to situation for [[geometric definition of higher category]]. A morphism $f : C \to D$ of [[simplicial set]]s is an acyclic fibration with respect to the [[model structure on simplicial sets]] if it all diagrams

$$
  \array{
    \partial \Delta[k] &\to& C
    \\
    \downarrow && \downarrow^f
    \\
    \Delta[k] &\to& D
  }
$$

have a lift

$$
  \array{
    \partial \Delta[k] &\to& C
    \\
    \downarrow &\nearrow& \downarrow^f
    \\
    \Delta[k] &\to& D
  }
$$

for all $k$, where now $\Delta[k]$ is the $k$-[[simplex]].


### Weak equivalences, acyclic fibrations and hypercovers##

With respect to the [[folk model structure]]  on $\omega$-categories an $\omega$-functor is 

* an [[acyclic fibration]] if it is $k$-surjective for all $k \in \mathbb{N}$;

* a [[weak equivalence]] if it is essentially $k$-surjective for all $k \in \mathbb{N}$.
See also [[equivalence of categories]].


###Remarks

All this has close analogs in other models of higher structures, in particular in the context of simplicial sets: an acyclic fibration in the standard [[model structure on simplicial sets]] is a morphism $X \to Y$ for which all diagrams

$$
  \array{
    \partial \Delta[n] &\to& X
    \\
    \downarrow && \downarrow
    \\
    \Delta[n] &\to& Y
  }
$$

have a lift

$$
  \array{
    \partial \Delta[n] &\to& X
    \\
    \downarrow &\nearrow& \downarrow
    \\
    \Delta[n] &\to& Y
  }
  \,.
$$

This is precisely in simplicial language the condition formulated above in globular language.


## Literature

The general idea of $k$-surjectivity is described around [definition 4](http://arxiv.org/PS_cache/math/pdf/0608/0608420v2.pdf#page=17) of

* Baez-Shulman, [[Lectures on n-Categories and Cohomology]]
([arXiv](http://arxiv.org/abs/math.CT/0608420))

The concrete discussion in the context of [[strict omega-category|strict omega-categories]] is in

* Yves Lafont, Francois M&#233;tayer, Krzysztof Worytkiewicz, _A folk model structure on $\omega$-cat_ ([arXiv](http://arxiv.org/abs/0712.0617)).

For the analogous discussion for simplicial sets see 

* [[model structure on simplicial sets]]

and references given there.



[[!redirects k-surjectivity]]