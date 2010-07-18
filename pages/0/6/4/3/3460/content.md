## The idea ##

The concept of separable algebra is a strengthening of the concept of [[semisimple algebra]], and a generalization of the concept of a [[separable field extension]].

## Definition ##

There are a several equivalent characterizations of separable algebras.  For all of these we fix a [[field]] $k$.  In what follows, all $k$-algebras will be assumed [[associative algebra|associative]] and [[unital algebra|unital]]. 

First, a $k$-algebra $A$ is defined to be **separable** if for every [[field extension]] $K$ of $k$, the algebra $A \otimes_k K$ is semisimple.

Second, a $k$-algebra $A$ is separable if and only if it is [[projective module|projective]] when considered as a left module of $A^e = A \otimes_k A^{op}$ in the usual way.

Third, a $k$-algebra $A$ is separable if and only if it is [[flat module|flat]] when considered as a right module of $A^e$ in the obvious (but perhaps not quite standard) way.  

Fourth, a $k$-algebra $A$ is separable if and only if the $A^e$-module morphism 
$$ \array{
m : & A^e &\to & A  \\
     & a \otimes b & \mapsto & a b 
}
$$
has a left inverse, that is a $A^e$-module morphism
$$  f: A \to  A^e  $$
with $f m = 1_{A^e}$.

We can also state the last characterization in a more grungy way in terms of the element $p = f(1)$.  Namely, a $k$-algebra $A$ is separable if and only if there exists an element 

$$ p = \sum_{i=1}^n a_i \otimes b_i  \in A^e $$

such that 

$$ \sum_{i=1}^n a_i b_i = 1 $$  

and 

$$ a p = p a $$

for all $a \in A$.  Such an element $p$ is called a **separability idempotent**, since it satisfies $p^2 = p$. 

## Classification ##

There is a classification theorem for separable algebras: separable algebras are the same as finite products of matrix algebras over [[division algebras]] whose centers are finite dimensional [[separable field extension|separable field extensions]] of the field $k$.  

A [[perfect field]] is one for which every extension of is [[separable field extension|separable]].  Examples include fields of characteristic zero, or finite fields, or a algebraically closed fields, or extensions of perfect fields.  If $k$ is a perfect field, separable algebras are the same as finite products of matrix algebras over division algebras whose centers are finite-dimensional field extensions of the field $k$.  In other words, if $k$ is a perfect field, there is no difference between a separable algebra over $k$ and a finite-dimensional [[semisimple algebra]] over $k$.

## Relation to Frobenius algebras ##

A result of Eilenberg and Nakayama that any separable algebra can be given the structure of a symmetric [[Frobenius algebra]].  Since the underlying vector space of a Frobenius algebra is isomorphic to its dual, any Frobenius algebra is necessarily finite dimensional, and so the same is true for separable algebras.  For more details, see:

* Samuel Eilenberg and Tadasi Nakayama, On the dimension of modules and algebras. II. Frobenius algebras and quasi-Frobenius rings, _Nagoya Math. J._ **9** (1955), 1-16. 
([web](http://projecteuclid.org/DPubS?service=UI&version=1.0&verb=Display&handle=euclid.nmj/1118799677))

A separable algebra is said to be '''strongly separable''' if there exists a separability idempotent $p$ that is '''symmetric''', meaning

$$ p = \sum_{i=1}^n a_i \otimes b_i = \sum_{i=1}^n b_i \otimes a_i $$

An algebra is strongly separable if and only if its trace form is nondegenerate, thus making the algebra into a special Frobenius algebra.   

For more details, see:

* Marcelo Aguiar, A note on strongly separable algebras, Bolet&#237;n de la Academia Nacional de Ciencias (C&#243;rdoba, Argentina), special issue in honor of Orlando Villamayor, 65 (2000) 51-60.  ([web](http://www.math.tamu.edu/~maguiar/strongly.ps.gz))

## In algebraic geometry ##

Commutative separable algebras are important in algebraic geometry.    The concept of [[etale morphism|étale cover]] in [[algebraic geometry]] is sort of a combination of [[covering space]] and separable algebra business. Lieven Le Bruyn has written "in categorical terms, studying the monoidal cat of commutative separable $k$-algebras is the same as studying the &#233;tale site of $k$".   This stuff would be nice to make precise...

A  commutative $k$-algebra $A$ is separable iff it is a finite product of [[separable field extensions]] of $k$.  

Separable algebras play a major role in the [[Galois theory]] of extensions of algebras.  Every separable $k$-algebra is a [[filtered colimit]] of finite-dimensional separable $k$-algebras.   (Isn't this in conflict with the claim above that all separable $k$-algebras _are_ finite-dimensional???)

There are further generalizations, leading to [[separable functor|separable functors]]...

[[!redirects separable algebras]]