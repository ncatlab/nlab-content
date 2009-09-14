
#Definition#

A [[multiplicative cohomology theory|multiplicative]] [[cohomology theory]] $A$ is **weakly periodic** if the natural map

$$
  A^2({*}) \otimes_{A^0({*})} A^n({*}) \stackrel{\simeq}{\to}
  A^{n+2}({*})
$$

is an [[isomorphism]] for all $n \in \mathbb{Z}$.

Compare with the notion of a [[periodic cohomology theory]].

# Relation to formal groups #

One reason why weakly periodic cohomology theories are of interest is that their [[cohomology ring]] over the space $\mathbb{C}P^\infty$ defines a [[formal group]].

To get a [[formal group]] from a [[weakly periodic cohomology theory|weakly periodic]], [[even cohomology theory|even]] [[multiplicative cohomology theory|multiplicative]] [[cohomology theory]] $A^\bullet$, we look at the induced map on $A^\bullet$ from a morphism 

$$
  i_0 : {*} \to \mathbb{C}P^\infty
$$

and take the kernel

$$
  J := ker(i_0^* : A^0(\mathbb{C}P^\infty) \to A^0({*}))
$$ 

to be the [[ideal]] that we complete along to define the [[formal scheme]] $Spf A^0(\mathbb{C}P^\infty)$ (see there for details).

Notice that the map from the point is unique only up to [[homotopy]], so accordingly there are lots of chocies here, which however all lead to the same result.

The fact that $A$ is weakly periodic allows to reconstruct the [[cohomology theory]] essentially from this [[formal scheme]].

To get a [[formal group law]] from this we proceed as follows: if the [[Lie algebra]] $Lie(Spf A^0(\mathbb{C}P^\infty))$ of the [[formal group]] 

$$
  Lie(Spf A^0(\mathbb{C}P^\infty))
  \simeq
  ker(i_0^*)/ker(i_0^*)^2
$$

is a free $A^0({*})$-module, we can pick a generator $t$ and this gives an [[isomorphism]] 

$$
  Spf(A^0(\mathbb{C}P^\infty)) \simeq Spf(A^0({*})[[t]])
$$

if $A^0(\mathbb{C}P^\infty) A^0({*})[ [t] ]$ then $i_0^*$ "forgets the $t$-coordinate".


#Related entries#

* [[A Survey of Elliptic Cohomology - formal groups and cohomology]]