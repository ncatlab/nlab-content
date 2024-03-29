
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

_Cartier [[duality]]_ is a refinement of [[Pontryagin duality]] from [[topological groups]] to [[group schemes]].

## Definition

+-- {: .num_defn}
###### Definition


Let $G$ be a [[finite group scheme]] over $k$, regarded as a
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

This appears for instance as ([Polishchuk, (10.1.11)](#Polishchuk)).

+-- {: .num_prop}
###### Proposition

Cartier duality is indeed a duality in that for any finite commutative group scheme $G$ there is an [[isomorphism]]

$$
  \widehat{\widehat{G}} \simeq G
$$

of the double Cartier dual with the original group scheme.

=--

(e.g. [Polishchuk, right above (10.1.11)](#Polishchuk), [Hida 00, theorem 1.7.1](#Hida00)) 

## Related concepts

* [[dual abelian group scheme]]

* [[Picard scheme]]

* [[Poincaré line bundle]]

## References

The classical textbook account is in chapter 1 of

* [[Jean Dieudonné]], _Introduction to the theory of formal groups_, Marcel Dekker, New York 1973.

and a more recent textbook account is in section 10.1 of

* [[Alexander Polishchuk]], _Abelian Varieties, Theta Functions and the Fourier Transform_
 {#Polishchuk}

or section 1.7 of 

*  Haruzo Hida, _Geometric Modular Forms and Elliptic Curves_, 2000, World scientific
 {#Hida00}

lecture notes include

* [pdf](http://www.math.ethz.ch/~pink/ftp/FGS/Lecture11.pdf)

Generalization beyond finite group schemes is  discussed in 

* Amelia &#193;lvarez S&#225;nchez, Carlos Sancho de Salas, Pedro Sancho de Salas, _Functorial Cartier duality ([arXiv:0709.3735](http://arxiv.org/abs/0709.3735))


and in 

* [[Dima Arinkin]], appendix in [[Ron Donagi]], [[Tony Pantev]], _Torus fibrations, gerbes, and duality_, ([arXiv:math/0306213](http://arxiv.org/abs/math/0306213))

Discussion in the context of [[higher algebra]] ([[brave new algebra]]) is in 

* [[Jacob Lurie]], section 5.3 of _[[Ambidexterity in K(n)-Local Stable Homotopy Theory]]_
* [[Jacob Lurie]], section 3 of _[[Elliptic Cohomology I]]_ 

[[!redirects Cartier dual]]
[[!redirects Cartier duals]]