
#Contents#
* automatic table of contents goes here
{:toc}

## Idea

...

### Modules, derivations and K&#228;hler differentials {#Modules}

We describe some aspects of the canonical [[bifibration]] of ring modules in a way that nicely organizes all the concepts [[module]], [[derivation]], [[Kähler differential]] in a single picture that lends itself to [[vertical categorification]]. (Following [[Deformation Theory|DefTheory]].)

With [[Ring]] denoting the [[category]] of (commutative, unital) [[rings]], write 

$$
  p : Mod \to Ring
$$ 

for the [[bifibration]] of [[module]]s over [[ring]]s: objects of $Mod$ are pairs consisting of a ring $R$ an an $R$-[[module]] $N$, and morphism $(R_1,N_1) \to (R_2, N_2)$ are pairs consisting of a ring homomorphism $f : R_1 \to R_2$ and a morphism $F : N_1 \to N_2 \otimes_f R_2$ of $R_2$-modules.

(Recall for instance from the discussion at [[Sweedler coring]]) 
that this bifibration is a way to think of the [[stack]] of algebraic [[vector bundle]]s.)

But there is also another functor $G : Mod \to Ring$ of interest: for $N$ any $R$-module, we may form the ring $G(N) := R \oplus N$ called the **square 0-extension** of $R$, in which multiplication is given by

$$
  (r_1,n_1) \cdot (r_2, n_2) := (r_1 r_2, n_1 r_2 + n_2 r_1
  \,.
$$

Moreover, there is a [[natural transformation|natural]] morphism of rings $G(N) \to R$ given by sending $(r,n) \mapsto r$. A [[section]] $v : R \to G(n)$ of this morphism is precisely a [[derivation]] of $R$ with values in the module $N$.

This may be organized into a single functor

$$
   Mod \to [I,Ring]
$$

into the [[arrow category]] of [[Ring]], that sends to the $R$-module $N$ to the morphism $G(N) \to R$. The original bifibration factors through this morphism by the right endpoint evaluation

$$
  \array{
    Mod &&\stackrel{p}{\to}&& Ring
    \\
    & \searrow && \nearrow_{\mathrlap{d_1}}
    \\
    && [I,Ring]
  }
  \,.
$$

Finally notice that the [[functor]] $G$ has a [[left adjoint|left]] [[adjoint functor]]

$$
  \Omega : Ring \to Mod
$$

that sends a ring $R$ to the $R$-module $\Omega_K(R)$ of [[Kähler differential]]s, i.e. to the module that encodes the [[cotangent bundle]].



### Cotangent complex

The above situation generalizes from the category [[Ring]] to an arbitrary [[(∞,1)-category]] $C$ by replacing the [[bifibration]] $Mod \to Ring$ by the [[stabilization]] $T_C \to C$ of the [[codomain fibration]] of $C$: the [[tangent (∞,1)-category]] of $C$.

The projection $p : T_C \to C$ still has a [[left adjoint]]

$$
  \Omega : C \to T_C
$$

called the [[cotangent complex]] functor for $C$. It still has the special property, as in the motivating example above, that it is also a [[section]] of the tangent propjection, i.e. that 

$$
  C \stackrel{\Omega}{\to} T_C \stackrel{p}{\to} C
$$

is the identity [[(∞,1)-functor]].



### Further catergorification

...


## Related entries

* [[cotangent complex]]

* [[Maurer-Cartan equation]]

* [[derived algebraic geometry]]

* [[formal scheme]]

* [[formal smoothness]]. 

Deformation problems are often phrased in terms of [[differential graded Lie algebra]]s.

## References

* Alexander I. Efimov, Valery A. Lunts, Dmitri O. Orlov, _Deformation theory of objects in homotopy and derived categories_ 
   * _I: general theory_ [arXiv:math/0702838](http://arxiv.org/abs/math/0702838);
   * _II: pro-representability of the deformation functor_ [arXiv:math/0702839](http://arxiv.org/abs/math/0702839);
   * _III: abelian categories_ [arXiv:math/0702840](http://arxiv.org/abs/math/0702840)

* E. Sernesi, _Deformations of algebraic schemes_
Grundlehren der Math. Wiss. __334__, Springer 2006. xii+339 pp. MR2247603 (2008e:14011)

* [[Maxim Kontsevich]], [[Yan Soibelman]], _Notes on A-infinity algebras, A-infinity categories and non-commutative geometry. I_, [math.AG/0606241](http://arxiv.org/abs/math/0606241)

* Wikipedia: [deformation theory](http://en.wikipedia.org/wiki/Deformation_theory), [cotangent complex] (http://en.wikipedia.org/wiki/Cotangent_complex)

* A. Grothendieck, _Cat&#233;gories cofibr&#233;es additives et complexe cotangent relatif_, Lecture Notes in Mathematics 79

* L. Illusie, _Complexe cotangent et d&#233;formations I_, Lec. Notes Math. __239__, Springer 1971, xv+355 pp.; _II_, LNM __283__, Springer 1972. vii+304 xv+355 pp. 

* Kai Behrend, B. Fantechi, _The intrinsic normal cone_, Invent. Math. __128__ (1997), no. 1, 45--88, MR1437495 (98e:14022) [arXiv:alg-geom/9601010](http://arxiv.org/abs/alg-geom/9601010)

* B. Fantechi, M. Manetti, _Obstruction calculus for functors of Artin rings I_, J. Algebra __202__ (1998), no. 2, 541--576, MR1617687 (99f:14004).

* Martin C. Olsson, _Deformation theory of representable morphisms of algebraic stacks_, Mathematische Zeitschrift
__253__, n. 1, 25--62 (2006) [doi:10.1007/s00209-005-0875-9](http://dx.doi.org/10.1007/s00209-005-0875-9)

* S. Merkulov, B. Vallette, _Deformation theory of properads_, [arXiv:0707.0889](http://arxiv.org/abs/0707.0889)

* M. Doubek, M. Markl, P. Zima, _Deformation theory (lecture notes)_, Archivum mathematicum __43__ (5), 2007, 333--371, [arXiv:0705.3719](http://arxiv.org/abs/0705.3719)

* [[Jacob Lurie]], [[Deformation Theory]] ([arXiv:0709.3091](http://arxiv.org/abs/0709.3091))

* W. Lowen, M. Van den Bergh, _Deformation theory of abelian categories_, Trans. Amer. Math. Soc. __358__  (2006),  no. 12, 5441--5483; [arXiv:math.CT/0405226](http://arxiv.org/abs/math/0405226).