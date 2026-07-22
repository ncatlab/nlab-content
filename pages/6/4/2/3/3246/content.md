


\tableofcontents


## Statement
 {#Statement}

The **Jacobian conjecture** asserts that: *In the [[category]] of [[smooth scheme|smooth]] [[complex numbers|complex]] [[algebraic varieties]] with [[regular maps]] between them, any [[étale map]] $F \colon \mathbb{C}^n \to \mathbb{C}^n$ is an [[isomorphism]].*  

In simpler terms, suppose we are given a [[map]] $F = (F_1, \dots, F_n) \colon \mathbb{C}^n \to \mathbb{C}^n$ such that the $F_i$ are [[polynomials]]. Then the Jacobian conjecture says that if the [[differential]] of $F$ is [[invertible]] at each point, $F$ itself is invertible. 


## State of the research

The conjecture was stated by [Keller 1939](#Keller1939) for $n = 2$.  It is known to hold at least for those maps $F$ which have a rational inverse. There were many failed attempts to prove the conjecture, especially in $n = 2$. 

An explicit [[counterexample]] for $n = 3$ was stated by [Alpöge 2026](#Alpöge2026): the polynomial map $F \colon \mathbb{C}^3 \to \mathbb{C}^3$ given by

$$ 
  F(x,y,z) 
   \;=\; 
  \big(
    y^2 (3x y+4)(x y+1) + z(x y + 1)^3,  
    3x y^2(3x y + 4) + 3x z(x y+1)^2 + y, 
    2x - x^3 z - 3x^2 y
  \big) 
$$

has $det \partial F_i / \partial x_j = -2$ everywhere but $F$ is not one-to-one since for example

$$ 
  F(0, 0, -1/4) 
   \;=\;  
  F(1, -3/2, 13/2) 
    \;=\;  
  F(-1, 3/2, 13/2) 
    \;=\; 
  (-1/4, 0, 0)
  \mathrlap{\,.}
$$

This counterexample for $n = 3$ implies counterexamples for all $n \geq 3$ ([Zhang 2026](#Zhang2026)).

The conjecture remains open for $n = 2$ (the case for which it was originally stated by [Keller 1939](#Keller1939)).




## Literature 

### General

The conjecture was originally stated for two variables in:

* {#Keller1939} Ott-Heinrich Keller: *Ganze Cremona-Transformationen*, Monatsh. f. Mathematik und Physik **47** (1939) 299--306 &lbrack;[doi:10.1007/BF01695502](https://doi.org/10.1007/BF01695502)&rbrack;

Surveys:

* [[Hyman Bass]], E. H. Connell, D. Wright, _The Jacobian conjecture: Reduction of degree and formal expansion of the inverse_, Bull Amer. Math. Soc. 7 (1982)

* {#Wikipedia} Wikipedia: *[Jacobian conjecture](https://en.wikipedia.org/wiki/Jacobian_conjecture)*

* A. van den Essen: *[Jacobian conjecture](http://eom.springer.de/J/j120010.htm)*, Springer [[Encyclopedia of Mathematics]]

See also:

* A. van den Essen, _Polynomial automorphisms and the Jacobian conjecture_, [pdf](http://www.emis.de/journals/SC/1997/2/pdf/smf_sem-cong_2_55-81.pdf), Alg&#232;bre non commutative, groupes quantiques et invariants (Reims, 1995),  55--81, S&#233;min. Congr., 2, Soc. Math. France, Paris, 1997. 

* Arno van den Essen, _Polynomial automorphisms and the Jacobian conjecture_, Progress in Mathematics, 190. Birkh&#228;user Verlag, Basel, 2000. xviii+329 pp. ISBN: 3-7643-6350-9

The Jacobian conjecture is equivalent to the Dixmier conjecture: every endomorphism of the $r$-th [[Weyl algebra]] $A_{r,k}$ over $k$ is an automorphism for all $r$.  This is a statement of: 

* [[Alexei Belov-Kanel]], [[Maxim Kontsevich]]: _The Jacobian conjecture is stably equivalent to the Dixmier conjecture_, Mosc. Math. J. __7__ 2 (2007) 209--218 &lbrack;[math.RA/0512171](http://arxiv.org/abs/math/0512171)&rbrack;

which does contain an error in the proof, that has been later amended by others.  A shorter algebraic proof is given in

* V. Bavula: _The $\text{Jacobian Conjecture}_{2n}$ implies the $\text{Dixmier Problem}_n$_ &lbrack;[math.AG/0512250](http://arxiv.org/abs/math/0512250)&rbrack;

It is known that each [[endomorphism]] of the $r$-th Weyl algebra is *injective*, and the Jacobian conjecture claimed it must also be *surjective*. The disproof of the Jacobian conjecture gives an explicit counterexample.

A related statement by [[Maxim Kontsevich]] on automorphisms of [[Weyl algebras]] is here:

* [[Alexei Kanel-Belov]], Andrey Elishev, Jie-Tai Yu, _Automorphisms of Weyl Algebra and a Conjecture of Kontsevich_, [arxiv/1802.01225](https://arxiv.org/abs/1802.01225)

There is an interesting blog discussion, from the point of view of [[algebraic geometry]]:

* [[David Speyer]] at _secret blogging seminar_: [how not to prove the Jacobian conjecture](http://sbseminar.wordpress.com/2009/05/27/how-not-to-prove-the-jacobian-conjecture)

### Counterexamples

A [[counterexample]] for $n = 3$ was announced by:

* {#Alpöge2026} [Levent Alpöge](https://alpo.ge/) (20 July 2026) &lbrack;[x.com:2079028340955197566](https://x.com/__alpoge__/status/2079028340955197566)&rbrack;

<center>
<div style="margin:-30px 0px 00px 00px;">
<a href="https://x.com/__alpoge__/status/2079028340955197566">
<img src="/nlab/files/Alpoge_JacobiCounterexample.png" width="450"/>
</a>
</div>
</center>

The observation that this implies counterexamples for all $n \geq 3$:

* {#Zhang2026} Zihan Zhang: *[Direct Consequences of the Three-Dimensional Counterexample to the Jacobian Conjecture](https://zzhang-iu.github.io/papers/direct-consequences-jacobian/)* (20 July 2026)



category: algebra