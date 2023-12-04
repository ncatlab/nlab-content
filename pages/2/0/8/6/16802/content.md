
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Consider a [[Lie algebra action]] of a [[Lie algebra]] $\mathfrak{g}$ on Lie algebra $\mathfrak{a}$, hence a Lie algebra [[homomorphism]] 

$$
  \rho 
    \;\colon\; 
  \mathfrak{g}
    \longrightarrow 
   \mathfrak{der}(\mathfrak{a})
$$ 

to the [[derivation Lie algebra]] of $\mathfrak{a}$. 

There is a [[Lie algebra extension]] of $\mathfrak{g}$ by $\mathfrak{a}$ whose [[underlying]] [[vector space]] is the [[direct sum]] ([[product]] in [[Vect]]) 

$$
  \hat \mathfrak{g} 
  \;=\; 
  \mathfrak{g} \oplus \mathfrak{a}
$$ 

and whose [[Lie bracket]] is given by the formula

$$
  \big[(x_1,t_1), (x_2,t_2)\big]
  \;=\;
  \big( 
    [x_1,x_2], 
    \;
    [t_1,t_2] + \rho(x_1)(t_2) - \rho(x_2)(t_1)   
  \big)
  \,.
$$

This is the _semidirect product_ or *semidirect sum* of $\mathfrak{g}$ with $\mathfrak{a}$.

## Related concepts

* [[Lie algebra extension]]

* [[semidirect product group]]

## References

* Tadeusz Ostrowski, *A note on semidirect sum of Lie algebras*, Discussiones Mathematicae - General Algebra and Applications (2013) **33** 2 (2013) 233-247 &lbrack;[eudml:270203](https://eudml.org/doc/270203)&rbrack;

* Mohammad Reza Alemi, Farshid Saeedi, *Derivation algebra of semi-direct sum of Lie algebras*, Asian-European Journal of Mathematics **15** 04 2250063 (2022) &lbrack;[doi:10.1142/S1793557122500632](https://doi.org/10.1142/S1793557122500632)&rbrack;

See also:

* Wikipedia, *[Lie algebra extension -- Construction](https://en.wikipedia.org/wiki/Lie_algebra_extension#Construction)*

[[!redirects semidirect product Lie algebras]]
[[!redirects semi-direct product Lie algebra]]
[[!redirects semi-direct product Lie algebras]]

[[!redirects semidirect sum Lie algebra]]
[[!redirects semidirect sum Lie algebras]]

[[!redirects semi-direct sum Lie algebra]]
[[!redirects semi-direct sum Lie algebras]]


