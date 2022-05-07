
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

### For small (∞,1)-categories

For $C$ a [[small (∞,1)-category]] and $\kappa$ a [[regular cardinal]], the $(\infty,1)$-category of $\kappa-$**pro-objects** in $C$ is the [[opposite (∞,1)-category]] of [[ind-object in an (∞,1)-category|ind-objects]] in the opposite of $C$:

$$
  Pro_\kappa(C) := (Ind_\kappa(C^{op}))^{op}
  \,.
$$

For $\kappa = \omega$ we write just $Pro(C)$.

By the properties listed there, if $C$ has all $\kappa$-small [[(∞,1)-limit]]s then this is equivalent to

$$
  \cdots \simeq Lex_\kappa(C, \infty Grpd)^{op} \subset Func(C,\infty Grpd)^{op}
$$

the full [[sub-(∞,1)-category]] of the [[(∞,1)-category of (∞,1)-functors]] on those that preserve these limits.


### For large (∞,1)-categories

Generalizing this definition:

\begin{definition}\label{CategoryOfProObjectsOfLargeAccessibleCategory}
If $\mathcal{C}$ is a possibly [[large category|non-small]] but [[accessible (∞,1)-category|accessible]] [[(infinity,1)-category|$(\infty,1)$-category]] with [[finite (infinity,1)-limits|finite $(\infty,1)$-limits]], we write :

$$
  Pro(\mathcal{C}) 
  \;\coloneqq\; 
  AccLexFunc(C ,\, \infty Grpd)^{op}
$$
for the [[opposite (infinity,1)-category|opposite $\infty$-category]] of [[(infinity,1)-functors|$\infty$-functors]] $\mathcal{C} \to $ [[∞Grpd]] which are

1. [[left exact functor|left exact]]  in that they [[preserved limit|preserve]] [[finite (infinity,1)-limit|finite $(\infty,1)$-limits]];

1. [[accessible (∞,1)-functor|accessible]].  

\end{definition}
([Lurie 2009, Def. 7.1.6.1](#Lurie09))
\begin{remark}
Yet more generally, if $C$ is just [[locally small]], then one can take $Pro(\mathcal{C})$ to be the $\infty$-category of [[small functors]] whose [[Grothendieck construction]] is [[cofiltered]].  Equivalently, $Pro(\mathca;{C})$ consists of the functors which are "*small* cofiltered limits of representables".
\end{remark}

\begin{remark}\label{PlainObjectsInLargeAccessibleCategoryAreProObjects}
For $\mathcal{C}$ a possibly [[large category|large]] but [[accessible (∞,1)-category|accessible]]  [[(infinity,1)-category|$(\infty,1)$-category]] which is [[tensoring|tensored]] over [[∞Grpd]], in that there is a [[natural equivalence|natural]] [[equivalence in an (∞,1)-category|equivalence]]
$$
  \infty Grpd
  \big(
    S
    ,\,
    \mathcal{C}(X,Y)
  \big)
  \;\;
  \simeq
  \;\;
  \infty Grpd
  \big(
    S \cdot X
    ,\,
    Y
  \big)
$$
then it is still a [[full sub-(infinity,1)-category|full sub-$(\infty,1)$-category]] of its pro-objects, in the sense of Def. \ref{CategoryOfProObjectsOfLargeAccessibleCategory}, via the usual [[(infinity,1)-Yoneda embedding|$(\infty,1)$-Yoneda embedding]]:
$$
  \array{
    \mathcal{C}
    &\xhookrightarrow{\phantom{---}}&
    Pro(\mathcal{C})
    \\
    c 
      &\mapsto&
    \mathcal{C}(c,-)
  }
$$
This is because the above tensoring means that $\mathcal{C}(c,-)$ is a [[right adjoint|right]]$\,$[[adjoint (infinity,1)-functor|adjoint $(\infty,1)$-functor]] and [[right adjoints preserve limits|these preserve limits]] and are accessible (by [this Prop.](accessible+infinity1-functor#AdjointFunctorsAreAccessible))
\end{remark}

## Related concepts

* [[ind-object]] / [[ind-object in an (∞,1)-category]]

* [[pro-object]] 

* [[shape of an (infinity,1)-topos|shape of an $\infty$-topos]]

## References

The large version is mentioned in:

* {#Lurie09} [[Jacob Lurie]], around def. 7.1.6.1 of: _[[Higher Topos Theory]]_, 2009

See also:

* [[Ilan Barnea]], [[Yonatan Harpaz]], [[Geoffroy Horel]], _Pro-categories in homotopy theory_ ([arXiv:1507.01564](https://arxiv.org/abs/1507.01564)).

[[!redirects pro-object in an (∞,1)-category]]

[[!redirects pro-objects in an (∞,1)-category]]

[[!redirects pro-object in an (infinity,1)-category]]
[[!redirects pro-objects in an (infinity,1)-category]]

[[!redirects pro-object in an infinity1-category]]

