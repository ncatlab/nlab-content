


#Contents#
* table of contents
{:toc}

## Idea

The _height_ of a [[variety]] should reflect how close the variety is to being ordinary and other arithmetic properties.


## Definition

Let $X$ be a [[smooth scheme|smooth]] [[proper scheme|proper]] $n$ [[dimension|dimensional]] [[variety]] over an [[algebraically closed field]] $k$ of [[characteristic]] $p$. Then one can define the [[Artin-Mazur formal group]] $\Phi$. Since it is a one-dimensional [[formal group]], it is completely determined up to [[isomorphism]] by its [[height]]. This is the **height of the variety** . The height could be infinite if $\Phi\simeq \widehat{\mathbb{G}_a}$, otherwise $\Phi$ is a [[p-divisible group]].



### Examples

For an [[elliptic curve]], the height is either $1$ in which case it is ordinary, or $2$ in which case it is supersingular.

A [[Calabi-Yau variety]] of any dimension is ordinary if and only if it has height $1$. For [[K3 surfaces]] the height is less than or equal to $10$ or infinite, but for all higher dimensional Calabi-Yau varieties the height has no known bound. Infinite height Calabi-Yau varieties are known as supersingular.

The height of an [[abelian variety]] depends on its $p$-rank, but must be $1$, $2$, or infinite.


## Relation to Witt Cohomology

Let $\mathcal{W}$ be the sheaf of Witt vectors on a variety $X$ satisfying the conditions above. If $X$ has finite height, then the [[Dieudonne module]] of the [[Artin-Mazur formal group]] is isomorphic to $H^n(X, \mathcal{W})$. By standard Dieudonne theory, $D(\Phi)$ is a free of rank $ht(X)$ module over $W$, so $ht(X)=\dim_K H^n(X, \mathcal{W})\otimes K$ where $K$ is the fraction field of $W$.

One consequence of the above is that $X$ is supersingular (of infinite height) if $H^n(X, \mathcal{W})$ is not a finite-type $W$-module. It is possible also that it is a torsion module in which case $H^n(X, \mathcal{W})\otimes K=0$ and again we can conclude that $X$ is of infinite height (since if $X$ were of finite height it would be a free module).


## Relation to Crystalline Cohomology

Suppose that $X$ is a variety with the above hypotheses, then the torsion free part of the [[crystalline cohomology]] $H^n_{crys}(X/W)$ is a [[Cartier module]] under the action of Frobenius. We can consider the part with slopes less than $1$, i.e. $H^n_{crys}(X/W)\otimes_W K_{[0,1)}$. The dimension of this is the height of $X$.




## Related concepts

* [[formal group]]

* [[Artin-Mazur formal group]]

## References

* [[Michael Artin]], [[Barry Mazur]], _Formal Groups Arising from Algebraic Varieties_, [numdam](http://www.numdam.org/item?id=ASENS_1977_4_10_1_87_0), [MR56:15663](http://www.ams.org/mathscinet-getitem?mr=56:15663)
 {#ArtinMazur}


