
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


# Contents
* table of contents
{: toc}

## The idea ##

The concept of *separable algebras* is a strengthening of the concept of *[[semisimple algebras]]*, and a generalization of the concept of *[[separable field extensions]]*.

## Definition ##

There are a several equivalent characterizations of separable algebras.  For all of these we fix a [[field]] $k$.  In what follows, all $k$-algebras will be assumed [[associative algebra|associative]] and [[unital algebra|unital]]. 

First, a $k$-algebra $A$ is defined to be **separable** if for every [[field extension]] $K$ of $k$, the [[tensor product]] algebra $A \otimes_k K$ is [[semisimple algebra|semisimple]].

Second, a $k$-algebra $A$ is separable if and only if it is [[flat module|flat]] when considered as a right [[module]] of $A^e = A \otimes_k A^{op}$ in the obvious (but perhaps not quite standard) way.  

Third, a $k$-algebra $A$ is separable if and only if it is [[projective module|projective]] when considered as a left [[module]] of $A^e$ in the usual way.

Fourth, a $k$-algebra $A$ is separable if and only if the $A^e$-module morphism 
$$ \array{
m : & A^e &\to & A  \\
     & a \otimes b & \mapsto & a b 
}
$$
has a right inverse, that is a $A^e$-module morphism
$$  f: A \to  A^e  $$
with $m f = 1_A$.

It is easy to see that the third and fourth definitions are equivalent.  We have an epimorphism of $A^e$-modules
$$  A^e \stackrel{m}{\longrightarrow} A \to 0 $$
If $f$ as above exists, this splits, so $A$ is a summand of a free $A^e$-module, namely $A^e$ itself, so $A$ is projective as an $A^e$-module.  Conversely, if $A$ is projective, any epimorphism to $A$ splits.

We can also state the fourth characterization in a more grungy way in terms of the element $p = f(1)$.  Namely, a $k$-algebra $A$ is separable if and only if there exists an element 
$$ p = \sum_{i=1}^n a_i \otimes b_i  \in A^e $$
such that 
$$ \sum_{i=1}^n a_i b_i = 1 $$  
and 
$$ a p = p a $$
for all $a \in A$.  Such an element $p$ is called a **separability idempotent**, since it satisfies $p^2 = p$. 
While grungy, finding a separability idempotent is a practical way to prove that an algebra is separable.

## Classification ##

There is a classification theorem for separable algebras: separable algebras are the same as finite products of matrix algebras over finite-dimensional [[division algebras]] whose centers are finite-dimensional [[separable field extension|separable field extensions]] of the field $k$.  

A [[perfect field]] is one for which every extension is [[separable field extension|separable]].  Examples include fields of characteristic zero, or finite fields, or algebraically closed fields, or extensions of perfect fields.  If $k$ is a perfect field, separable algebras are the same as finite products of matrix algebras over finite-dimensional division algebras over field $k$.  In other words, if $k$ is a perfect field, there is no difference between a separable algebra over $k$ and a finite-dimensional [[semisimple algebra]] over $k$.

## Relation to Frobenius algebras ##

A result of Eilenberg and Nakayama states that any [[separable algebra]] over a field $k$ can be given the structure of a [[Frobenius algebra|symmetric Frobenius algebra]].  Since the underlying vector space of a Frobenius algebra is isomorphic to its dual, any Frobenius algebra is necessarily finite dimensional, and so the same is true for separable algebras.  For more details, see:

* Samuel Eilenberg and Tadasi Nakayama, On the dimension of modules and algebras. II. Frobenius algebras and quasi-Frobenius rings, _Nagoya Math. J._ **9** (1955), 1-16. 
([web](https://projecteuclid.org/journals/nagoya-mathematical-journal/volume-9/issue-none/On-the-dimension-of-modules-and-algebras-II-Frobenius-algebras/nmj/1118799677.pdf))
* Endo, Shizuo and Watanabe, Yutaka, On separable algebras over a commutative ring, _Osaka J. Math._ **4**(2) (1967), 233-242. ([web](https://projecteuclid.org/download/pdf_1/euclid.ojm/1200691953)). See in particular Thm. 4.2.

A separable algebra is said to be **strongly separable** if there exists a separability idempotent $p$ that is **symmetric**, meaning
$$ p = \sum_{i=1}^n a_i \otimes b_i = \sum_{i=1}^n b_i \otimes a_i $$
An algebra is strongly separable if and only if it can be made into a [[Frobenius algebra|special Frobenius algebra]].  When this can be done, it can be done in a unique way.

There is an equivalent characterization of strongly separable algebras which makes this fact clearer.  Any element $a$ of an associative unital algebra gives a left multiplication map 
$$ \array{ 
L_a : &A &\to& A \\
      &b &\mapsto& a b 
}
$$
When $A$ is finite-dimensional, there is a bilinear pairing $g: A \times A \to k$ defined by
$$ g(a,b) = tr(L_a L_b) $$
An algebra $A$ is strongly separable if and only if $g$
is **nondegenerate**, i.e., if there is a vector space isomorphism $A \to A^*$ given by
$$ a \mapsto g(a, -)  $$
In this case, there is just one way to make $A$ into a special Frobenius algebra, namely by defining the counit to be 
$$ \epsilon(a) = tr(L_a) $$

Here are some examples of strongly separable algebras:

* the algebra of $n \times n$ matrices with entries in a field $k$ is always separable, but strongly separable if and only if $n$ is not divisible by the characteristic of $k$.  

* the group algebra $k[G]$ of a finite group is strongly separable if and only if the order of $G$ is not divisible by the characteristic of $k$.

For more details, see Aguiar's book below.



## Over commutative rings ##

More generally, if $k$ is any unital [[commutative ring]], we can define a separable $k$-algebra to be an algebra $A$ such that $A$ is projective as a module over $A^e = A \otimes_k A^{op}$. 

As in the case of algebras over a field, an algebra $A$ over a commutative ring $k$ is separable if and only if the $A^e$-module epimorphism 
$$ \array{
m : & A^e &\to & A  \\
     & a \otimes b & \mapsto & a b 
}
$$
splits, and this in turn is equivalent to the existence of a separability idempotent.

If a separable algebra $A$ is also projective as a module over $k$, it must be finitely generated as a $k$-module.  For more details see DeMeyer-Ingraham.

## Separable extensions of noncommutative rings

The ring extension $S$ over $R$ is said to be a separable extension if all short exact sequences of $S$-$S$-bimodules that are split as $S$-$R$-bimodules also split as $S$-$S$-bimodules. This is equivalent to the statement that the relative Hochschild cohomology $HH^n(S,R;M) = 0$ for all $n\gt 0$ and all coefficient bimodules $M$.

## In algebraic geometry ##

Commutative separable algebras are important in algebraic geometry.   The concept of [[etale morphism|étale cover]] in  is a way of implementing the idea of [[covering space]] in the context of [[algebraic geometry]], but any étale cover of the spectrum of a field corresponds to a commutative separable algebra over that field.  Lieven Le Bruyn has written "in categorical terms, studying the monoidal category of commutative separable $k$-algebras is the same as studying the &#233;tale site of $k$".   This idea is partially captured by the so-called *fundamental theorem of Grothendieck Galois theory*: the  category of commutative separable algebras over a field $k$ is contravariantly equivalent to the category of continuous actions on finite sets of the profinite fundamental group of $k$.   As a group, the *profinite fundamental group* of $k$ is the Galois group $Gal(k_s|k)$ where $k_s$ is a *separable closure* of $k$, that is, a maximal [[separable field extension]] of $k$.

Separable algebras play a major role in the [[Galois theory]] of extensions of algebras.  There are further generalizations, leading to [[separable functor|separable functors]]...

## Related entries

* [[separable functor]]

* [[separable field extension]]

* [[separable coring]]


## References

* K. Hirata, K. Sugano, _On semisimple and separable extensions of noncommutative rings_, J. Math. Soc. Japan 18 (1966), 360-373.

* F. DeMeyer and E. Ingraham, _Separable algebras over commutative rings_, Lecture Notes in Mathematics **181**, Springer, Berlin (1971)


* [[Marcelo Aguiar]], *A note on strongly separable algebras*, Bolet&#237;n de la Academia Nacional de Ciencias (C&#243;rdoba, Argentina), special issue in honor of Orlando Villamayor, **65** (2000) 51-60  &lbrack;[pdf](http://www.math.cornell.edu/~maguiar/strongly.pdf)&rbrack;



See also:

* Wikipedia, *[Separable algebra](http://en.wikipedia.org/wiki/Separable_algebra)*


An explicit proof of the Grothendieck Galois theory statement that the category of commutative separable algebras over a field $K$ is anti-equivalent to the category of continuous actions on finite sets of the profinite fundamental group of $K$:

* Federico G. Lastaria, _On separable algebras in Grothendieck Galois theory_, Le Mathematiche 51:3, 1996, [link](http://www.dmi.unict.it/ojs/index.php/lematematiche/article/view/464/0)

[[!redirects separable algebras]]
[[!redirects separable ring extension]]
[[!redirects separable ring extensions]]