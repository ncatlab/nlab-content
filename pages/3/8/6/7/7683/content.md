
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Duality
+--{: .hide}
[[!include duality - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

_Cartier [[duality]]_ is a refinement of [[Pontryagin duality]] form [[topological groups]] to [[group schemes]].

## Definition

+-- {: .num_defn}
###### Definition


Let $G$ be a finite [[group scheme]] over $k$, regarded as a
[[sheaf]] of groups $G \in Sh(Ring^{op}_k)$. Write $\mathbb{G}_m$ for the [[multiplicative group]], similarly regarded. 

Then the _Cartier dual_ $\widehat G$ is the [[internal hom]]

$$
  \widehat G \coloneqq [G,\mathbb{G}_{m}]
$$

of group [[homomorphisms]], hence the [[sheaf]] which to $R \in Ring_k^{op}$ assigns the [[set]]

$$
  \widehat G \;\colon\; R \mapsto Hom_{Grp/Spec R}(G \times Spec R, \mathbb{G}_m \times Spec R)
$$

of group homomorphisms over $Spec(R)$

=--

This appears for instance as ([Polishuk, (10.1.11)](#Polishchuk)).

+-- {: .num_prop}
###### Proposition

Cartier duality is indeed a duality in that for any $G$ as above there is an [[isomrophism]]

$$
  \widehat{\widehat{G}} \simeq G
$$

of the double Cartier dual with the original group scheme.

=--

over ([Polishuk, right above (10.1.11)](#Polishchuk))


## References

A textbook account is in section 10.1 of

* Alexander Polishchuk, _Abelian Varieties, Theta Functions and the Fourier Transform_
 {#Polishchuk}
 

lecture notes include

* [pdf](http://www.math.ethz.ch/~pink/ftp/FGS/Lecture11.pdf)
