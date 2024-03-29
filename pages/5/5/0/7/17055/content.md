
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Goodwillie calculus
+--{: .hide}
[[!include Goodwillie calculus - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

In the context of [[Goodwillie calculus]] an [[(∞,1)-functor]] is called _analytic_ if it behaves in [[analogy]] with an [[analytic function]] in that it its [[Goodwillie-Taylor tower]] converges to it.


## Definition

### (Co-)Cartesian cubical diagrams

Let $\mathcal{C}$ be an [[(∞,1)-category]] with [[finite (∞,1)-colimits]].

+-- {: .num_defn #StronglyCoCartesian}
###### Definition

An $n$-[[cube]] in $\mathcal{C}$, hence an [[(∞,1)-functor]] $\Box^n \longrightarrow \mathcal{C}$, is called _strongly homotopy co-cartesian_ or just _strongly co-cartesian_, if all its 2-dimensional square faces are [[homotopy pushout]] [[diagrams]] in $\mathcal{C}$.

=--

+-- {: .num_defn #Cartesian}
###### Definition

An $n$-[[cube]] in $\mathcal{D}$, hence an [[(∞,1)-functor]] $\Box^n \longrightarrow \mathcal{D}$, is called _homotopy cartesian_ or just _cartesian_, if its "first" object exhibits a [[homotopy limit]]-[[cone]] over the remaining objects.

=--


### Analytic functors

+-- {: .num_defn #rhoAnalyticFunctor}
###### Definition

An  [[(∞,1)-functor]] $F \colon \mathcal{C} \to \mathcal{D}$ is _stably $n$-excisive_ with constants $c$ and $\kappa$_ -- or _satisfies "condition $E_n(c,\kappa)$"_ -- if for every strongly co-Cartesian $(n)+1$-cube $X$ in $\mathcal{C}$, def. \ref{StronglyCoCartesian}, such that $X(\emptyset) \to X(s)$ is $k_s$-[[n-connected object of an (infinity,1)-topos|connective]] for $k_s \geq \kappa$ for all $s\in \{1,\cdots, n+1\}$, then  $F(X)$ is an $(n+1)$-cube in $\mathcal{D}$ such that the comparison map

$$
  F(\emptyset) \longrightarrow \underset{{K\,subcube\,of\,F(X)}\atop {K \neq \emptyset}}{\lim} F(K)
$$

(to the indicated [[homotopy limit]]) is $(-c + \sum_s k_s)$-[[n-connected object of an (infinity,1)-topos|connective]].

The functor $F$ is called _$\rho$-analytic_ if there is $q$ such that it satisfies the condition $E_n(n\rho - q,\rho + 1)$ for all $n$.

=--

(e.g. [Johnson 95, def. 1.1, def. 1.3](#Johnson95))


## Properties

### Convergence of the Goodwillie-Taylor tower

For $\rho$-analytic functors their [[Goodwillie-Taylor tower]] converges to them on $\rho$-[[n-connected object of an (infinity,1)-topos|connective objects]]. See there.

## Examples

### The identity functor on homotopy types

The identity $(\infty,1)$-functor on [[∞Grpd]] is 1-analytic, def. \ref{rhoAnalyticFunctor}. For $n = 2$ this is the statement of the [[Blakers-Massey theorem]], for $n \gt 2$ this is the statment of the [higher cubical BM-theorems](Blakers-Massey+theorem#HigherCubical).

(see e.g. [Munson-Volic 15, example 10.1.18](#MunsonVolic15))

## Related concepts

* [[excisive (∞,1)-functor]]

* [[polynomial (∞,1)-functor]]


## References

The concept is due to 

* [[Tom Goodwillie]], _Calculus II: Analytic functors_, K-Theory  01/1991; 5(4):295-332. DOI: 10.1007/BF00535644

Review includes

* [[Tom Goodwillie]], section 3 of _The differential calculus of homotopy functors_, Proceedings of the International Congress of Mathematicians in Kyoto 1990, Vol. I, Math. Soc. Japan, 1991, pp. 621–6 ([article pdf](https://math.mit.edu/juvitop/old/notes/2009_Fall/goodwillie-icm.pdf), [full proceedings Vol I pdf](https://www.mathunion.org/fileadmin/ICM/Proceedings/ICM1990.2/ICM1990.2.ocr.pdf), [[GoodwillieICM1990.pdf:file]])

* {#Johnson95} Brenda Johnson, _The derivatives of homotopy theory_, Transactions of the AMS, Volume 347, 1995 ([pdf](http://www.ams.org/journals/tran/1995-347-04/S0002-9947-1995-1297532-6/S0002-9947-1995-1297532-6.pdf))

A textbook account is in 

* {#MunsonVolic15} [[Brian Munson]], [[Ismar Volic]], _Cubical homotopy theory_, Cambridge University Press, 2015 [pdf](http://palmer.wellesley.edu/~ivolic/pdf/Papers/CubicalHomotopyTheory.pdf)


[[!redirects analytic (∞,1)-functors]]

[[!redirects analytic (infinity,1)-functor]]
[[!redirects analytic (infinity,1)-functors]]

[[!redirects analytic functor]]
[[!redirects analytic functors]]
