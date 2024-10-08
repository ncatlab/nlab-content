

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include algebra - contents]]
=--
=--
=--

\tableofcontents

# Idea

A [[ring]] $R$ is **simple** if it is it is a [[simple object]] in the [[category]] of $R$-$R$-[[bimodules]].

This can be stated in more elementary terms in any of the following equivalent ways:

*  $R$ is nontrivial and has no nontrivial two-sided [[ideals]].

*  $R$ has exactly two two-sided ideals (which must be $R$ itself and its [[zero ideal]]).

In [[constructive mathematics|constructive]] algebra, this is too strong; we must say:

*  For each two-sided ideal $I$, $I$ is the zero ideal if and only if $I$ is proper (not equal to $R$).

## Examples 

* A [[field]], or a [[division ring]], is simple. 

* If $D$ is a division ring, then the ring $M_n(D)$ of $n \times n$ [[matrices]] with entries in $D$ is a simple ring. 

* The [[Weyl algebra]] $k\langle x, y\rangle/(x y - y x - 1)$ over a field $k$ is a simple ring. (In different language: this is the ring of differential operators with polynomial coefficients in one variable $t$, obtained as the image of the ring homomorphism from the noncommutative [[polynomial ring]] $k \langle x, y \rangle$ to the ring of $k$-linear endomorphisms $Vect(k[t], k[t])$ that sends $x$ to the derivative operator $\frac{d}{d t}$ and $y$ to the multiplication operator $t \cdot -$.) An explanation of why this is simple may be found [here](https://qchu.wordpress.com/2012/05/30/the-jacobson-radical/) at [[Qiaochu Yuan]]'s blog. 


## Related concepts

* [[semisimple ring]]

[[!redirects simple rings]]

