

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Definition

A group $G$ is **perfect** if it equals its own commutator subgroup $[G, G]$, i.e., if every element of $G$ is a product of commutators (elements of the form $[g, h] = g h g^{-1} h^{-1}$). 

Equivalently: let $G^{ab}$ denote the [[abelianization]] of $G$ (the target of the homomorphism $G \to G^{ab}$ that is universal among homomorphisms from $G$ to [[abelian groups]], or the largest abelian quotient of $G$). Then $G$ is perfect precisely when $G^{ab}$ is a [[trivial group]], since 
$G^{ab} \cong G/[G, G]$:

$$
  G \;\; \text{perfect}
  \;\;\;\Leftrightarrow\;\;\;
  G^{ab} \;\; \text{is trivial}
$$


## Examples

The [[trivial group]] is perfect, trivially.

+-- {: .num_prop }
###### Proposition

The [[alternating group]] $A_5$ is the smallest nontrivial perfect group.

=--

+-- {: .num_prop #2IIsPerfect}
###### Proposition

The [[binary icosahedral group]] $2I$ is a [[perfect group]]: its [[abelianization]] is the [[trivial group]].

In fact, up to [[isomorphism]], the [[binary icosahedral group]] is the unique [[finite group]] of [[order of a group|order]] 120 which is a [[perfect group]].

=--

Since $2I \simeq SL_2(\mathbb{F}_5)$ ([this prop.](icosahedral+group#IsomorphismToSL25)), this is a special case of the following class of examples, in fact it is smallest example from this class:

+-- {: .num_prop} 
###### Proposition 

The [[special linear group]] $SL_n(\mathbb{F})$ is perfect for any [[field]] $\mathbb{F}$ and any $n \geq 1$, except for the cases $SL_2(\mathbb{Z}/(2))$ and $SL_2(\mathbb{Z}/(3))$. 

=-- 

See for example [here](http://people.brandeis.edu/~igusa/Math101b/SL.pdf), or Lang's Algebra ($3^{rd}$ edition), page (to be looked up). 
 
+-- {: .num_prop} 
###### Proposition 
The [[quotient group]] of a perfect group is again perfect. 
=-- 

This last assertion is easy to see: $G$ is perfect if it has no nontrivial abelian quotients. If a quotient $H$ had a nontrivial abelian quotient, then obviously so would $G$. 

Relatedly, we have 

+-- {: .num_prop} 
###### Proposition 
An arbitrary colimit of perfect groups (as calculated in [[Grp]], the category of groups) is again perfect. 
=-- 

+-- {: .proof} 
###### Proof 
The abelianization functor, being a [[left adjoint]], preserves a [[colimit]] of perfect groups $colim_i G_i$, taking it to $colim_i (G_i)^{ab} \cong \colim_i 1 \cong 1$ (since an arbitrary colimit of [[initial object]]s is again initial). 
=-- 

[[!redirects perfect groups]]