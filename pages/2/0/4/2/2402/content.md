[[!redirects basic ideas of moduli stacks of curves and Gromov-Witten theory]]



+-- {: .standout}

This is a sub-entry of [[Gromov-Witten invariants]]. See there for further background and context.

This entry is supposed to provide an exposition of some basic ideas underlying Gromov-Witten theory.

=--


> **raw material**: notes taken verbatim in some seminar -- needs to be polished



#Contents#


* [part I: basics of moduli stacks of curves](#intropart1)

* [part I: basics of Gromov-Witten theory](#intropart2)


## Intro Part I: basics of moduli stacks of curves {#intropart1}


**question**: what is a **moduli problem**?

* some kind of object;

* a notion of "familiy"/"deformation" of these objects

* some [[equivalence relation]] $\sim$ (possibly trivial)
  on the set of such families $S(B)$ over $B$

from this we get a [[functor]] (a [[presheaf]])

$$
  F : C^{op} \to Set
$$

$$
  B \mapsto S(B)/_\sim
$$

**terminology** an object $M$ is called a [[fine moduli space]] if the corresponding [[representable functor|represented functor]]

$$
  Y_M : C^{op} \to Set
$$

$$
  x \mapsto Hom(x,M)
$$

is isomorphic to $F$, i.e. if it represents $F$.

**examples** in the [[homotopy category]] of [[topological space]]s we have

$$
  \left\{
    complex line bundles over B
  \right\}/isom
  \leftrightarrow
  Hom_{Ho(Top)}(B, \mathbb{C}P^\infty)
$$

so $\mathbb{C}P^\infty$ is a [[classifying space]] for complex line bundle. Similarly for higher rank vector bundles and Grassmannians.

The analogue in the algebraic category is

$$
  \left\{ 
      line bundles L over B with generating sections s_0,...,s_n \in \Gamma(L) \right\} / isom
\leftrightarrow
Hom(B, \mathbb{P}^n).
$$

And also similarly for higher rank [[vector bundle]]s and Grassmannians.


Despite these examples, in a lot of cases the functors are not representable. We'll see some of these examples below.


Why are [[fine moduli space]]s desireable?

They allow us to study a _single_ family which tells us universal things about all families. Even if you do not care about families or deformations, moduli spaces can help, because they can tell you something about trivial families, i.e. the objects that you are studying to begin with.

**example** studying the [[cohomology ring]]s of $Gr_n(\mathbb{R}^\infty)$ or $Gr_n(\mathbb{C}^\infty)$, which are the classifying space for higher rank real and complex [[vector bundle]]s gives universal relations among [[Chern class]]es, etc.

Let's look at [[elliptic curve]]s (work over $\mathbb{C}$).

the functor of families here is 

$$
  F : Sch/\mathbb{C}^{op} \to Set
$$

$$
  B \mapsto \left\{
     \array{
        E \\ \downarrow \\ B
     }
     flat families of elliptic curves
  \right\}
$$

**Fact**: there is no [[fine moduli space]] of [[elliptic curve]]s representing this functor

**why not?** 

there is something called the  [[j-invariant]] which classifies [[elliptic curve]]s up to [[isomorphism]]

let 

$$
  E : y^2 = x^3 + a x + b
$$

be an [elliptic curve]] given by parameters $a,b$. Then its [[j-invariant]] is the number

$$
  j(E) = \frac{2^8 3^3 a^3}{4 a^3 + 27 b^2}
$$

so we might guess that the "$j$-line" $\mathbb{A}^1$ is a [[fine moduli space]] for [[elliptic curve]]s,

i.e. that there is a "universal family" of elliptic curves $C \to \mathbb{A}^1$ such that the fiber over $j \in \mathbb{A}^1$ is the elliptic cuvre with that $j$-invariant.

so that for any family $E \to B$ we'd have a [[pullback]]

$$
  \array{
    E &\to& C
    \\
    \downarrow && \downarrow
    \\
    B &\to& \mathbb{A}^1
  }
$$

where $B \to \mathbb{A}^1$ sends a point in $B$ to the [[j-invariant]] of the elliptic curve in the fiber over $B$.

Now consider the family 

$$
  \chi = (y^2 = x(x-1)(x+\lambda)) \subset \mathbb{A}^1 \times \mathbb{A}_\lambda^1 \times \mathbb{P}^2
$$

$$
  \array{
    \chi &\to& C
    \\
    \downarrow && \downarrow
    \\
    \mathbb{A}^1_\lambda &\to& \mathbb{A}^1
  }
$$

$$
  j(\chi_\lambda) = s^8 \frac{(\lambda^2 - \lambda + 1)^2}{\lambda^2(\lambda-1)^2}
$$


now send $\mathbb{A}^1_\lambda \to \mathbb{A}^1_{\lambda}$

by dually sending $\lambda \mapsto 1-\lambda$  

check that $j(\chi_\lambda) = j(\chi_{1-\lambda})$


this induces in the fibers a map

$\phi : \chi \to \chi$

$$
  \phi : (x,y,\lambda) \mapsto (1-x,\pm i y , 1-\lambda)
$$

this maps further to $(x,-y,\lambda)$. But this would have to be the identity for $\mathbb{A}^1$ to be a fine moduli space, which it is not. So $\mathbb{A}^1$ at least is not a fine moduli space, even though it might look like one.

so that gives some computational insight that something goes wrong

This argument does not prove that there exists no moduli space of elliptic curves. It merely proves that the "j-line" $\mathbb{A}^1$ can not be the moduli space of elliptic curves. However, the basic argument can be adapted, if one so desires, to in fact prove that there is no moduli space of elliptic curves. Alternatively you can use the sheaf argument below (however, I think the make that argument work out completely you need to introduce some extra language, etale covers and so forth).

**abstract argument** (oversimplified) generally, [[fine moduli space]]s tend to not exist if the objects to be classified have nontrivial [[automorphism]]s. These allow to build families of objects that are locally trivial but globally not and no 
[[fine moduli space]] will be able to represent that.

>this argument makes use of the fact that if we have a moduli space, then the preshesaf we started with must actually be a [[sheaf]] (with respect to a [[subcanonical topology]] that is implicitly assumed, probably -- but notice that in the example of $Ho(Top)$ above the standard topology is not subcanonical, so the argument breaks down). so we know that we should be able to compute it from gluing its local assignments. But locally our locally trivial family looks, well, trivial, so it all looks the same to our sheaf. So it will just try to glue the trivial object to itself, which is not what we actually have.

**General principle** [[automorphism]]s of objects are obstructions to the existence of an (ordinary) [[fine moduli space]] classifying these objects.


**How to "fix" these problems**. 

1. add extra structure to the objects under consideration (add marked points)

2. instead of looking for representing [[topological space]]s, look for representing [[groupoid]]s / [[stack]]s.

3. use [[coarse moduli space]]s  $M \in Sch/\mathbb{C}$ with $\Psi_M : F \to h_M$ such that 

   a) $F(Spec(\mathbb{C})) \to h_M(Spec \mathbb{C}) = hom(Spec \mathbb{C}, M)$ is a [[bijection]]
 
   b) given $M'$ and $\Psi_{M'} : F \to h_{M'}$ then there exists unique $M \to M'$ such that $\array{ F && \stackrel{\Psi_{M'}}{\to}&& h_{M'} \\ & {}_{\Psi_M}\searrow && \nearrow \\ && h_M} $

   so a [[coarse moduli space]] is one that at least has the right underlying set of points as the _right_ [[moduli stack]] has: as long as we don't look at families but just at single things, it does give the right classification.



**exercise** show that the $j$-line $\mathbb{A}^1$ _is_, while not a [[fine moduli space]], a [[coarse moduli space]]

**fact** there exists a [[coarse moduli space]] $M_{g,n}$ of [[Riemann surface]]s of [[genus]] $g$ with $n$ marked points and a [[fine moduli stack]] $M_{g,n}$ such that for all $g,n$ we have

$M_{g,n}$ is a [[smooth scheme|smooth]] [[Deligne-Mumford stack]] - aka [[orbifold]]

**except** for $(g,n) =$ $(0,0), (0,1), (0,2), (1,0)$ (these are the cases where the [[automorphism group]] is infinite, so in these cases we don't get a [[Deligne-Mumford stack]])

**Issues**:

1. $M_{g,n}$ is not proper, meaning: not compact, so we don't have, for example, [[Poincare duality]] on $M_{g,n}$ and no [[integration]] theory. Proper, or even better projective, schemes or stacks are just a lot easier to deal with.

2. sometimes one wants to study singular curves or families with degeneracies.

Both "issues" can be "resolved" via [[Deligne-Mumford compactification]].

$$
  \bar M_{g,n}
$$

which parameterizes at-most-nodal curves, that are connected, arithmetic [[genus]] $g$, with $n$ smooth marked points, and the group of [[automorphism]]s is finite.

$\bar M_{g,n}$ is a smooth proper [[Deligne-Mumford stack]].

smooth here means smoothness as for [[orbifold]]s.

Deligne and Mumford were able to prove many theorems about the ordinary moduli space of curves by studying instead the compactification.



#Intro Part II: basics of Gromov-Witten theory{#intropart2}

**Gromov** was looking for invariants of [[symplectic manifold]]s: he used $J$-holomorphic curves in compact symplectic manifolds to get symplectic invariants

**[[Edward Witten]]** studied [[worldsheet]]s of [[string theory|string]]s in some [[spacetime]] [[manifold]] (e.g a [[Calabi-Yau space|Calabi-Yau 3-fold]])

we want to consider now [[genus]] $g$ [[Riemann surface]]s with $n$ marked points mapping into some space $X$

For a fixed

$$
  \beta \in H_2(X, \mathbb{Z}),
$$


$$
  M_{g,n}(X,\beta)
$$

is the space that parameterizes maps

$$
  \Sigma \stackrel{f}{\to} X
$$

where $\Sigma$ is smooth, and has $n$ marked points, and 
such that for $[\Sigma]$ the [[fundamental homology class]] of $\Sigma$ we have

$$
  f_*[\Sigma] = \beta
  \,.
$$

this is a smooth [[Deligne-Mumford stack]]. (Again we must exclude the cases of small $(g,n)$.)

similarly, write $\bar M_{g,n}(X,\beta)$ for the same setup but with $\Sigma$ from $\bar M_{g,n}$ as above in part 1 (the DM compactified moduli stack). EXCEPT here we do not require that $\Sigma$ (with its $n$ marked points) has finite automorphism group; we require instead that the MAP has finite automorphism group, which means.......(fill in)

This is a _proper_ (compact) [[Deligne-Mumford stack]] - but _not_ smooth (not even in the sense of smooth stacks!). This is very important. This is what makes the theory difficult/nontrivial/interesting.

we have

$$
  \bar M_{g,n}(pt,0) = \bar M_{g,n}
$$

what do [[string theory|string theorists]] want to do? 

we have evaluation maps

$$
  \bar M_{g,n}(X,\beta) \stackrel{ev_i}{\to} X
$$

where $i$ labels a marked point, and we want morphisms

$$
  H^\bullet(X)^{\otimes n}
  \stackrel{ev^*_1 \wedge ev^*_2 \wedge \cdots}{\to}
  H^*(\bar M_{g,n}(X,\beta))
  \stackrel{\int_{[\bar M_{g,n}(x,\beta)]^{virtual}}}{\to}
  \mathbb{C}
$$

**string theorists conjectured** : there exists a virtual fundamental class $[\bar M_{g,n}(x,\beta)]^{virtual}$ that makes the maps above into the [[correlation function]]s of a [[quantum field theory]] (the integral would be the [[path integral]] of the [[worldsheet]] [[sigma-model]]) with state space $H^\ast(X)$.

Why do we want to use a "virtual" fundamental class? Because \bar M_{g,n}(x,\beta) is not smooth, the actual fundamental class may not behave very well.

the mathematical structure of GW-theory was elucidated Ruan and then by [[Maxim Kontsevich]] and Manin in 1994.

$$
  \array{
    \bar M_{g,n}(X,\beta)
    \\
    \downarrow^\phi
    \\
    \bar M_{g,n}
  }
$$

$$
  I_{g,n,\beta} : 
  H^*(X)^{\otimes}
  \to
  H^*(\bar M_{g,n}(X,\beta))
  \stackrel{\phi_*}{\to}
  H^*(\bar M_{g,n})
$$

where the map $\phi_*$ is some kind of "pushforward" or "integration along the fibers"; this map uses the virtual fundamental class

there is also a map

$$
  \alpha
  :
  \bar M_{g_1,n_1+1}
  \times
  \bar M_{g_2,n_2+1}
  \to
  \bar M_{g,n}
$$

with $g = g_1 + g_2$ and $n = n_1 + n_2$ obtained by gluing the last marked point of the first curve to the first marked point of the second curve.

so consider now the combination of these two maps

$$ 
  \array{
    H^\bullet(X)^{\otimes}
    &\stackrel{I_{g,n,\beta} }{\to}&
    H^\bullet(\bar M_{g,n}(X,\beta))
   \stackrel{\phi_*}{\to}
   H^*(\bar M_{g,n})
   \\
   \downarrow^{- \otimes \Delta \otimes -}
   &&
   \downarrow^\alpha
   \\   
   H^\bullet(X)^{\otimes n_1}
  \otimes H^\bullet(X) \otimes
   H^\bullet(X) \otimes H^\bullet(X)^{\otimes n_2}
   && 
   H^{\bullet}(\bar M_{g_1,n_1+1} \times \bar M_{g_2,n_2+1})
   \\
   \downarrow^\simeq
   && \downarrow^{\simeq} 
   \\
   H^\bullet(X)^{\otimes n_1 + 1}
   \otimes
   H^\bullet(X)^{\otimes n_2 + 1}    
   &\stackrel{I_{g_1,n_1+1} \otimes I_{g_2,n_2+1}}{\to}&
   H^{\bullet}(\bar M_{g_1,n_1+1}) \otimes H^\bullet (\bar M_{g_2,n_2+1}))
   }
  $$

where the bottom right iso uses the [[Künneth formula]]

here $\Delta_a$ is a homogeneous basis of $H^\bullet(X)$

$$
  g_{a b} = \int_X \Delta_a \wedge \Delta_b
$$

$$
  \Delta = \sum g^{a b} \Delta_a \wedge \Delta_b
$$

where

$$
  g^{a b} = (g_{a b})^{-1}
$$

so this diagram above says that this satisfies the [[sewing law]]s that defines a [[quantum field theory]].

There are various other axioms that Gromov-Witten theory must satisfy, but the sewing law above is the most important. The hard part of all of this is constructing the virtual fundamental class, and then proving that this class indeed makes the sewing law and the other axioms satisfied.

The above discussion does not yet reveal much of the rich structure of Gromov-Witten invariants. But GW invariants indeed have a very rich and beautiful mathematical structure. Indeed, if we look at just the easiest part of the theory, namely g=0, we are lead to quantum cohomology and Frobenius manifolds. 

There is also the mirror symmetry conjecture, which roughly posits that the GW invariants can be found via calculations that a priori seem completely unrelated.

#References#
* M. Kontsevich, Yu. Manin, _Gromov-Witten classes, quantum cohomology, and enumerative geometry_, Comm. Math. Phys. 164 (1994), no. 3, 525--562 ([euclid](http://projecteuclid.org/euclid.cmp/1104270948)).

* [[Yuri Manin]], _Frobenius manifolds, quantum cohomology and moduli spaces_, Amer. Math. Soc., Providence, RI, 1999.

* W. Fulton, R. Pandharipande, _Notes on stable maps and quantum cohomology_, in: Algebraic Geometry-
Santa uz 1995 ed. Kollar, Lazersfeld, Morrison. Proc. Symp. Pure Math. 62, 45&#8211;96 (1997)

* J Robbin, D A Salamon, _A construction of the Deligne-Mumford orbifold_,  J. Eur. Math. Soc. (JEMS)  8  (2006),  no. 4, 611--699 ([arxiv](http://arxiv.org/abs/math/0407090); [pdf at JEMS](http://www.ems-ph.org/journals/show_pdf.php?issn=1435-9855&vol=8&iss=4&rank=3)); corrigendum  J. Eur. Math. Soc. (JEMS)  9  (2007),  no. 4, 901--905 ([pdf at JEMS](http://www.ems-ph.org/journals/show_pdf.php?issn=1435-9855&vol=9&iss=4&rank=11)).

* J Robbin, Y Ruan, D A Salamon, _The moduli space of
regular stable maps_,  Math. Z.  259  (2008),  no. 3, 525--574 ([doi](http://dx.doi.org/10.1007/s00209-007-0237-x)).

* Martin A. Guest, _From quantum cohomology to integrable systems_, Oxford Graduate Texts in Mathematics, 15. Oxford University Press, Oxford, 2008. xxx+305 pp.

* Joachim Kock, Israel Vainsencher, _An invitation to quantum cohomology. Kontsevich's formula for rational plane curves_, Progress in Mathematics, 249. Birkh&#228;user Boston, Inc., Boston, MA, 2007. xiv+159 pp. 

* Sheldon Katz, _Enumerative geometry and string theory_, Student Math. Library __32__. IAS/Park City AMS & IAS 2006. xiv+206 pp.