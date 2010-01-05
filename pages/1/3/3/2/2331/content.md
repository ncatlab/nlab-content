
#Contents#
* automatic table of contents goes here
{:toc}

## Idea {#Idea}

Deformation theory studies problems of extending structures to  extensions of their domains. Formal deformation theory, is the part where the extensions are _[[infinitesimal object|infinitesimal]]_.

A typical problem in deformation theory has the structure that 

* a [[morphism]] $f : X \to Y$ of certain [[space]]s is given, 

* and [[infinitesimal object|infinitesimal]] thickenings $\tilde X$ and $\tilde Y$ of $X$ and $Y$ are prescribed, with injection morphisms $X \to \tilde X$ and $Y \to \tilde Y$

and asks whether a bottom horizontal morphism $\tilde f$ in the diagram

$$
  \array{
    X &\stackrel{f}{\to}& Y
    \\
    \downarrow && \downarrow
    \\
    \tilde X &\stackrel{\tilde f}{\to}& \tilde Y
  }
$$

may be found. This morphism $\tilde f$ would be called an _infinitesimal deformation_ of $f$.

In other words:

+-- {: .standout}

Deformation theory studies the **obstruction theory** of extensions to **infinitesimal** thickenings.

=--

A typical example of an _infinitesimal thickening_ is a _square-0-extension_ of a [[ring]]:

let $R$ be a [[ring]], to be thought of as the ring of functions on the [[space]] $X$ in the above diagram. Let furthermore $N$ be an $R$-module, to be thought of as the $R$-modules of [[section]]s of a [[vector bundle]] over $X$.

Then consider the new ring, whose underlying group is the [[direct sum]] $R \oplus N$, equipped with the product structure

$$
  (r_1, n_1) \cdot (r_2, n_2) = (r_1 r_2, r_1 n_2 + n_2 r_1)
  \,.
$$

This is the **square 0-extension** of $R$ by $N$. It should be thought of as the algebra of functions that consists of elements of $R$ and  $N$, where the elements in $N$ are thought of as functions with values in [[infinitesimal object|infinitesimal quantities]], so that their wouldd-be product "$n_1 \cdot n_2$" vanishes.

So the ring $R \oplus N$ may be thought of as the ring of functions on the infinitesimal extension $\tilde X$ of $X$, which is the space obtained by adding to $X$ all the _vectors of infinitesimal length_ in the vector bundle over $X$.

There is a canonical ring homomorphism $R\oplus N \to R$ that is the identity on $R$ and $0$ on $N$. This is to be thought of as the pullback of functions on spaces along the inclusion of spaces $X \to \tilde X$ (which in turn may be thought of as the 0-[[section]] of the vector bundle on $X$).

Similarly, let $R_2$ be another ring with module $N_2$ and square-0 extension $R_2 \oplus N_2$, though of, respectively, as the ring of functions on a space $Y$, the module of sections of a vector bundle on $Y$ and the ring of functions on the space of infinitesimal vectors of this vector bundle.

In terms of these function rings, a morphism $f : X \to Y$ of spaces corresponds to a ring homomorphism $R_1 \leftarrow R_2 : f^*$. Hence we have a situation

$$
  \array{
    R_1 &\stackrel{f^*}{\leftarrow}& R_2
    \\
    \uparrow && \uparrow
    \\
    R_1 \oplus N_1 && R_2 \oplus N_2
  }
  \,.
$$

The obvious obstruction problem now is whether we can **deform** $f^*$ to a morphism $R_1 \oplus N_1 \leftarrow R_2 \oplus N_2 : \tilde f^*$ of rings, such that we get a commuting diagram

$$
  \array{
    R_1 &\stackrel{f^*}{\leftarrow}& R_2
    \\
    \uparrow && \uparrow
    \\
    R_1 \oplus N_1 &\stackrel{\tilde f^*}{\leftarrow}& R_2 \oplus N_2
  }
  \,.
$$

The obstruction to the existence of such lifts is measured by [[cohomology]] with coefficients in the [[cotangent complex]] of $R_1$. 

This is the archetypical problem that deformation theory deals with. As always, after studying this a bit it turns out that in order to obtain a good theory, one needs to adopt the [[nPOV]]. Problems as above may be stated in the [[category]] [[Ring]] of rings, but they may have good answers only in [[vertical categorification|categorifications]] of this for instance to the [[(∞,1)-category]] of [[E-∞-ring]]s.

### Modules, derivations and K&#228;hler differentials {#Modules}

In order to better see the structure of the above archetypical problem of defomration theory, we describe some aspects of the canonical [[bifibration]] of ring modules in a way that nicely organizes all the concepts [[module]], [[derivation]], [[Kähler differential]] in a single picture that lends itself to [[vertical categorification]]. (Following [[Deformation Theory|DefTheory]].)

With [[Ring]] denoting the [[category]] of (commutative, unital) [[rings]], write 

$$
  p : Mod \to Ring
$$ 

for the [[bifibration]] of [[modules]] over [[rings]]: objects of $Mod$ are pairs consisting of a ring $R$ an an $R$-[[module]] $N$, and morphism $(R_1,N_1) \to (R_2, N_2)$ are pairs consisting of a ring homomorphism $f : R_1 \to R_2$ and a morphism $F : N_1 \to N_2 \otimes_f R_2$ of $R_2$-modules.

(Recall for instance from the discussion at [[Sweedler coring]]) 
that this bifibration is a way to think of the [[stack]] of algebraic [[vector bundles]].)

But there is also another functor $G : Mod \to Ring$ of interest: for $N$ any $R$-module, we may form the ring $G(N) := R \oplus N$ called the **square 0-extension** of $R$, in which multiplication is given by

$$
  (r_1,n_1) \cdot (r_2, n_2) := (r_1 r_2, n_1 r_2 + n_2 r_1)
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

that sends a ring $R$ to the $R$-module $\Omega_K(R)$ of [[Kähler differentials]], i.e. to the module that encodes the [[cotangent bundle]].



### Cotangent complex

The above situation generalizes from the category [[Ring]] to an arbitrary presentable [[(∞,1)-category]] $C$ by replacing the [[bifibration]] $Mod \to Ring$ by the [[stabilization]] $T_C \to C$ of the [[codomain fibration]] of $C$: the [[tangent (∞,1)-category]] of $C$.

The projection $p : T_C \to C$ still has a [[left adjoint]]

$$
  \Omega : C \to T_C
$$

called the [[cotangent complex]] functor for $C$. It still has the special property, as in the motivating example above, that it is also a [[section]] of the tangent propjection, i.e. that 

$$
  C \stackrel{\Omega}{\to} T_C \stackrel{p}{\to} C
$$

is the identity [[(∞,1)-functor]].



### Further categorification

...

## Related entries and references 

Related $n$lab entries include [[cotangent complex]], [[Maurer-Cartan equation]], [[derived algebraic geometry]], [[formal scheme]], [[formal smoothness]]. Deformation problems are often phrased in terms of [[differential graded Lie algebras]], and, more generally, [[L-infinity algebras]]. 

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