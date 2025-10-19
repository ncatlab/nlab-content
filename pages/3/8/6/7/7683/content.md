
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

Let $k$ be a [[commutative ring]]. 

Let $G$ be a commutative [[group scheme]] over $k$, regarded as a
[[sheaf]] of groups $G \in Sh(Ring^{op}_k)$. Write $\mathbb{G}_m$ for the [[multiplicative group]], similarly regarded. 

Then the _Cartier dual_ $\widehat G$ is the [[internal hom]]

$$
  \widehat G \coloneqq [G,\mathbb{G}_{m}]
$$

of [[group homomorphisms]], hence the [[sheaf]] which to $R \in Ring_k^{op}$ assigns the [[set]]

$$
  \widehat G \;\colon\; R \mapsto Hom_{Grp/Spec R}(G \times Spec R, \mathbb{G}_m \times Spec R)
$$

of group homomorphisms over $Spec(R)$

=--

This appears for instance in [Polishchuk, (10.1.11)](#Polishchuk).

Say that $G$ is _finite locally free_ if it is an affine $k$-scheme whose coordinate ring is a finite locally free $k$-module.

+-- {: .num_prop}
###### Proposition 
( [SGA3](#SGA3), Exposé VIIA, §3.3)
If $G$ is a finite locally free commutative $k$-group scheme, then $\widehat{G}$ is also a a finite locally free commutative $k$-group scheme, and the natural map
$$
G \to \widehat{\widehat{G}}
$$
is an isomorphism.
=--

This proposition is also discussed in [Polishchuk, right above (10.1.11)](#Polishchuk) and [Hida 00, theorem 1.7.1](#Hida00).

When $k$ is a [[field]], every finite group scheme is locally free. When $G$ is no longer finite over $k$, it is still true that $G \to \widehat{\widehat{G}}$ is an isomorphism ([Dieudonné 73, p. 21-22](#Dieudonne))

## Related concepts

* [[dual abelian group scheme]]

* [[Picard scheme]]

* [[Poincaré line bundle]]

## References

The case of finite locally free group schemes is covered in: 

* {#SGA3} [[Michel Demazure]],  [[Alexander Grothendieck]] (eds.): _Schémas en groupes. Tome I: Propriétés générales des schémas en groupes_, Séminaire de Géométrie Algébrique du Bois Marie 1962/64 ([[SGA3]])

The classical textbook account over a field is in chapter 1 of

* {#Dieudonne} [[Jean Dieudonné]]: _Introduction to the theory of formal groups_, Marcel Dekker, New York (1973) 

and a more recent textbook account is in section 10.1 of:

* {#Polishchuk} [[Alexander Polishchuk]], _Abelian Varieties, Theta Functions and the Fourier Transform_
 
or section 1.7 of 

* {#Hida00} Haruzo Hida: _Geometric Modular Forms and Elliptic Curves_, World Scientific (2000)
 

lecture notes include

* [pdf](http://www.math.ethz.ch/~pink/ftp/FGS/Lecture11.pdf)

Generalization beyond finite group schemes:

* Amelia &#193;lvarez S&#225;nchez, Carlos Sancho de Salas, Pedro Sancho de Salas, _Functorial Cartier duality ([arXiv:0709.3735](http://arxiv.org/abs/0709.3735))


and in 

* [[Dima Arinkin]], appendix in [[Ron Donagi]], [[Tony Pantev]], _Torus fibrations, gerbes, and duality_, ([arXiv:math/0306213](http://arxiv.org/abs/math/0306213))

Discussion in the context of [[higher algebra]] ([[brave new algebra]]) is in 

* [[Jacob Lurie]], section 5.3 of _[[Ambidexterity in K(n)-Local Stable Homotopy Theory]]_
* [[Jacob Lurie]], section 3 of _[[Elliptic Cohomology I]]_ 

[[!redirects Cartier dual]]
[[!redirects Cartier duals]]