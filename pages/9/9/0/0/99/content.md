#Idea#

In as far as a [[Chevalley-Eilenberg algebra]] of an $L_\infty$-[[Lie infinity-algebroid|algebroid]] is the algebra of functions on an [[NQ-supermanifold]] $\mathbf{X}$, the **Weil algebra** is the algebra of functions on the shifted tangent bundle $T[1] \mathbf{X}$.

#Definition#

+-- {: .query}
Warning: the X in the Idea section is not the X in this definition. I suggest calling it M and saying that M is the manifold with algebra of functions the degree zero part of $CE(\mathfrak{g})$.  ---Maarten

What if anything is the relationship between the $\mathbf{X}$ above and the $X$ (or $M$) here?  (Sorry, I don\'t know anything about this stuff.)  ---Toby
=--

For $CE(\mathfrak{g}) = \wedge^\bullet_{C^\infty(X)} \mathfrak{g}^*$ the Chevalley-Eilenberg algebra of a $L_\infty$-[[Lie infinity-algebroid|algebroid]] $g$ over $X$, the corresponding Weil algebra is

$$
  \mathrm{W}(\mathfrak{g})
  :=
  \left(
    \wedge^\bullet_{C^\infty(X)}
    (
      \mathfrak{g}^* \oplus \Gamma(T^* X) 
      \otimes \mathfrak{g}^*[1]
    )
    , d_{\mathrm{W}(\mathfrak{g})}
  \right)
$$

where the differential acts as the deRham differential on $\wedge^\bullet \Gamma(T^* X)$ and is defined on generators in $\mathfrak{g}^* \oplus \mathfrak{g}^*[1]$ by 
$$
  d_{\mathrm{W}(\mathfrak{g})}
  =
  \left(
    \array{
       d_{\mathrm{CE}(\mathfrak{g})}
       &
       0
       \\
       \sigma
       &
       - \sigma \circ d_{\mathrm{CE}(\mathfrak{g})}
       \circ \sigma^{-1}
    }
    \,,
  \right)
$$
where $\sigma|_{\mathfrak{g}^*} : \mathfrak{g}^* \to \mathfrak{g}^*[1]$ is the canonical degree-shifting isomorphism.

##Remarks

* This generalizes the notion of [[superdifferential form]] from ordinary supermanifolds to [[NQ-supermanifolds]].

#References

For the role played by the Weil algebra in the general context of higher [[Lie theory]] see

* Hisham Sati, Urs Schreiber, Jim Stasheff, _$L_{\infty}$ algebra connections and applications to String- and Chern-Simons $n$-transport_ ([arXiv](http://arxiv.org/abs/0801.3480))