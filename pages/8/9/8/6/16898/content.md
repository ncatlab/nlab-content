[[!redirects pseudo-Banach ring]]
[[!redirects Pseudo-Banach ring]]
[[!redirects pseudo-Banach rings]]
[[!redirects proxi-Banach ring]]
[[!redirects proxi-Banach rings]]
[[!redirects proxi-normed ring]]
[[!redirects proxi-normed rings]]


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Analytic geometry
+--{: .hide}
[[!include analytic geometry -- contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea and motivations

The notion of proxi-Banach ring is a generalization of the notion of [[Banach ring]], essentially obtained by replacing the usual triangular inequality $|a+b|\leq |a|+|b|$ that appears in the theory of [[metric spaces]] by the more natural (in a categorical sense) weak triangular inequality
$|a+b|\leq C\cdot\max(|a|,|b|)$
that appears in the theory of [[proxi-metric spaces]].

Their use allows the definition of an $\mathbb{R}_+^*$-action on various categories of [[global analytic spaces]].

They are also the natural objects that appear as $\pi_0$ of spectral rings in
[[spectral global analytic geometry]].

## Definition

A pseudo-Banach ring is a ring object in the rig category $(\mathbb{R}_{+\leq}^\mathrm{Sets},\oplus_\infty,\otimes_m)$
of $\mathbb{R}_+$-graded sets (with bounded maps between them).
This means a set $R$ with a norm
$|\cdot|_R:R\to \mathbb{R}_+$ such that there exists $C$, $D$ and $E$, $F$ with

* $|a+b|\leq C\cdot \max(|a|,|b|)$,

* $|ab|\leq D\cdot|a|\cdot|b|$,

* $|-a|\leq E|a|$,

* $|0|=0$,

* $|1|\leq F\cdot 1$ (one often supposes additionally that $|1|=1$).

## The free module

If $X$ is an $\mathbb{R}_+$-graded set, and $R$ is a pseudo-Banach ring, one may define an associated pseudo-normed free module $R^{(X)}$ by putting on
the usual free module the following convenient grading (not given by the usual $\ell^1$ grading): if $\sum a_x\{x\}$ is an element with support $supp(a)$, one may write it $\sum a_i\{x_i\}$, and parenthesize it in binary terms. In the case of a support of cardinal three, we may write for example
$$P(a_1\{x_1\}+a_2\{x_2\}+a_3\{x_3\})=((a_1\{x_1\}+a_2\{x_2\})+a_3\{x_3\}).$$
Each parenthesis contains only two terms, and there is a finite set of choices for the position of parenthesis, denoted $\mathcal{P}a(supp(a))$. We then define by induction ($C$ denotes the norm, i.e., infimum of the $C$ constants for the addition map), for $P$ an element of this set,
$$|(u)+(v)|_{C,P}:=C\cdot \max(|u|_{C,Pu},|v|_{C,Pv}).$$
One then takes the maximum of all these expressions to define a natural pseudo-norm on $R^{(X)}$ by
$$
\left|\sum a_x\{x\}\right|_{\infty,C}:=\max_{P\in \mathcal{P}a(supp(a))}\left|P(\sum a_x\{x\})\right|_{C,P}.
$$
If $C=1$, i.e., in the non-archimedean case, this gives back the usual non-archimedean (maximum) seminorm on the free module.

## Modules and their operations

Using the free module, and the coproduct and product of $\mathbb{R}_+$-graded sets, one defines direct sums and tensor products of modules, and throught the symmetric algebra construction, the free $\mathbb{R}_+$-graded algebra (algebra of convergent "power series" with coefficients in $R$ and polyradii in $X$).

One may also work with the category of ind-pseudo-Banach ring, and of ind-pseudo-Banach modules over them, to develop an overconvergent version of the theory.

## A natural flow

The action of $\mathbb{R}_+^*$ on all these objects is simply given by acting on the grading through
$$|\cdot|\mapsto |\cdot|^t:=e^{t\mathrm{ln}|\cdot|}.$$

## Related subjects

[[global analytic geometry]]

[[overconvergent global analytic geometry]]

[[spectral global analytic geometry]]

## Reference

For the category of $\mathbb{R}_+$-graded sets:

* [[Frédéric Paugam]] _Overconvergent global analytic geometry_ ([arXiv:1410.7971](http://arxiv.org/abs/1410.7971))