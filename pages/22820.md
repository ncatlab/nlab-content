## Idea

Analytic monads are [[monads]] on [[Set]] that correspond to [[operads]] in [[Set]].

## Definition

More precisely, an [[operad]] $O$ in [[Set]] induces a [[monad]] $T$
on [[Set]]:
$$T(S)=\coprod_{n\ge0} O_n \times_{\Sigma_n} S^n.$$

Such a monad $T$ is equipped with a canonical weakly [[cartesian natural transformation]] to the [[monad]] $Sym$ arising from the [[commutative operad]].

## Properties

A theorem of Joyal \cite{Joyal} states that
there is a [[monoidal equivalence]]
between the [[monoidal category]] of [[endofunctors]] $Set\to Set$
that admits a weakly [[cartesian natural transformation]] to $Sym$
and the [[monoidal category]] of [[species]],
i.e., symmetric sequences in [[Set]] with the [[substitution product]].

In particular, the category of analytic [[monads]] on [[Set]]
is equivalent to the category of [[operads]] in [[Set]].

## The colored case

The correspondence carries over to [[colored operads]] (with a [[set]]
of colors $C$)
if we use the [[slice category]] $Set/C$ instead of [[Set]].

## The nonsymmetric case

A similar correspondence can be established for [[nonsymmetric operads]],
except that we must include the data of a _cartesian_ (not weakly cartesian) transformation to the [[monad]] of the [[associative operad]],
which is no longer unique.

See Example 4.2.14 in Leinster's book \cite{Leinster}.

## The homotopical case

The correspondence generalizes to [[(∞,1)-categories]], with
some statements becoming more elegant.
See Gepner–Haugseng–Kock \cite{GHK}.

## Related concepts

* [[species]]

* [[operad]]

* [[monad]]

## References

* {#Joyal} [[André Joyal]], _Foncteurs analytiques et espèces de structures_, Combinatoire énumérative (Montréal/Québec, 1985), Lecture Notes in Mathematics 1234 (1986), 126-159.  [doi](http://dx.doi.org/10.1007/bfb0072514).

* [[Mark Weber]], _Generic morphisms, parametric representations and weakly Cartesian monads_, Theory Appl. Categ. 13 (2004), 191–234.

* [[Tom Leinster]], _[[Higher Operads, Higher Categories]]_, London Mathematical Society Lecture Note Series 298 (2004), [doi](http://dx.doi.org/10.1017/cbo9780511525896).

* {#GHK} [[David Gepner]], [[Rune Haugseng]], [[Joachim Kock]], _∞-Operads as Analytic Monads_, [arXiv:1712.06469](https://arxiv.org/abs/1712.06469).

