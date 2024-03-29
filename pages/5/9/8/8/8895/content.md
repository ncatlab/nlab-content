
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Internal $(\infty,1)$-Categories
+--{: .hide}
[[!include internal infinity-categories contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A _semi-Segal space_ is like a [[Segal space]] but without specified identities/degeneracies. It is to [[semicategories]] as Segal spaces are to [[categories]].

## Definition

Let $\mathcal{C} = $ [[sSet]], equipped with the standard [[model structure on simplicial sets]].

+-- {: .num_defn}
###### Definition

A **semi-Segal space** is a [[semi-simplicial object]] in $\mathcal{C}$ such that

1. it is a [[fibrant object]] in the [[Reedy model structure]] on $\mathcal{C}^{\Delta^{op}_+}$;

1. it satisfies the [[Segal conditions]] be [[weak equivalences]].

=--

+-- {: .num_remark}
###### Remark

A [[semi-simplicial object]] $X_\bullet$ being Reedy fibrant means that for each $n \in \mathbb{N}$ the morphisms

$$
  \array{
   X_{n} 
   \\
   \downarrow^{\mathrlap{(\partial_0, \cdots, \partial_{n})}}
   \\
    X^{\partial \Delta^n}
  }
$$

are [[fibrations]].

=--

+-- {: .num_remark}
###### Remark

Equivalently this says that it is a semi-simplicial object which satisfies the [[Segal conditions]] by [[homotopy pullbacks]]. This is just as for [[Segal spaces]], see there for details.

=--


+-- {: .num_defn #Completeness}
###### Definition

A **complete semi-Segal space** is a semi-Segal space $X_\bullet$ such that the two morphisms

$$
  X_1^{inv} \hookrightarrow X_1 \stackrel{\partial_1, \partial_0}{\to} X_0
$$

are [[weak equivalences]].

=--

This is the completeness/[[univalence]] condition just as for [[complete Segal spaces]].

+-- {: .num_defn #QuasiUnitalness}
###### Definition

A semi-Segal space is **quasiunital** if (...)

=--

([Harpaz 12, p. 38](#Harpaz12))

+-- {: .num_prop}
###### Proposition

A complete semi-Segal space, def. \ref{Completeness} is quasi-unital, def. \ref{QuasiUnitalness}.

=--

([Harpaz 12, Cor 4.1.11](#Harpaz12)).

+-- {: .num_remark}
###### Remark

A morphism of complete semi-Segal spaces $f_\bullet \colon X_\bullet \to Y_\bullet$ is quasi-unital if it preserves the weak equivalences, hence if

$$
  \array{  
     X_1^{inv} &\hookrightarrow& X_1
     \\
     \downarrow^{\mathrlap{f_1|_{inv}}} && \downarrow^{\mathrlap{f_1}}
     \\
     Y_1^{inv} &\hookrightarrow & Y_1
  }
  \,.
$$

=--

## Related concepts

* [[semi-category]]

* [[semi-simplicial object]]

## References

The notion is mentioned in 

* [[Jacob Lurie]], _[[On the Classification of Topological Field Theories]]_

More details are spelled out in

* {#Harpaz12} [[Yonatan Harpaz]], _Quasi-unital $\infty$-Categories_ ([arXiv:1210.0212](http://arxiv.org/abs/1210.0212))
 
See also

* {#Tanaka16} [[Hiro Lee Tanaka]], _Functors (between $\infty$-categories) that aren't strictly unital_ ([arXiv:1606.05669](http://arxiv.org/abs/1606.05669))

* Wolfgang Steimle, _Degeneracies in quasi-categories_, [arxiv:1702.08696](https://arxiv.org/abs/1702.08696)


[[!redirects semiSegal space]]
[[!redirects semi Segal space]]

[[!redirects semi-Segal spaces]]
[[!redirects semiSegal spaces]]
[[!redirects semi Segal spaces]]

[[!redirects complete semi-Segal space]]
[[!redirects complete semiSegal space]]
[[!redirects complete semi Segal space]]

[[!redirects complete semi-Segal spaces]]
[[!redirects complete semiSegal spaces]]
[[!redirects complete semi Segal spaces]]
