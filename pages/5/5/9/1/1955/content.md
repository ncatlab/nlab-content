#Contents#
* automatic table of contents goes here
{:toc}


## Idea and definition

The notion of _K&#228;hler differential_ is a very general way to encode a notion of [[differential form]]: something that is dual to a [[derivation]] or [[vector field]].

Conceptually, in dual language of algebras, a symmetry of a commutative algebra $A$ is an [[automorphism]] $g\colon A\to A$, i.e., $g(a b)=g(a)g(b)$. The 'infinitesimal' symmetries are the [[derivations]] $X\colon A\to A$, with $X(a b)=X(a)b+X(b)a$. The [[module]] of K&#228;hler differentials $\Omega^1_K(A)$  parametrizes derivations, in the sense that every derivation $X$ corresponds uniquely to a morphism of $A$-modules $\mu_X: \Omega_K^1 (A)\to A$.

### The ordinary definition and its insufficiency

K&#228;hler differentials are traditionally conceived in terms of an algebraic construction of a certain [[module]] $\Omega_K^1(Spec R)$ on a given ordinary [[ring]] $R$. On [[space]]s modeled (in the sense described at [[space]]) on the [[site]] [[CRing]]$^{op}$, such as [[varieties]], [[scheme]]s, [[algebraic space]]s, [[Deligne-Mumford stack]]s, this produces the correct notion of [[differential form]] in this context. This is the case discussed in the section

* [Over ordinary rings](#OrdinaryRings)

below.

The definition, concrete as it is, applies of course also to function rings on spaces not modeled on $CRing^{op}$, such as rings $C^\infty(X)$ of smooth functions on a [[smooth manifold]]. One might expect that the module of K&#228;hler differentials $\Omega_K(Spec C^\infty(X))$ of $C^\infty(X)$, regarded as an ordinary [[ring]], does reproduce the familiar notion of smooth [[differential form]]s on a [[manifold]]. But it does not. This is discussed in the section

* [Over smooth rings regarded as ordinary rings](#SmoothOrPlain).

This shows that the concrete algebraic construction  of K&#228;hler differential forms over plain rings, traditionally thought of as their very definition, does in fact not correctly capture their nature. There is another definition -- obtained from the [[nPOV]] -- which does capture the situation correctly:



### The correct definition of the notion of _module_ ...

In fact, already the definition of [[module]] has to be freed from it concrete realization in the context of ordinary rings, to exhibit its true nature. What this is has been established long ago in

* Dan Quillen, _Homotopical algebra_

and in Jon Beck's thesis, and is discussed in more detail in the entries _[[module]]_ and _[[Beck module]]_ : Beck and Quillen noticed that the [[category]] $R Mod$ of modules over an ordinary commutative ring $R$ is canonically [[equivalence of categories|equivalent]] to the category $Ab(CRing/R)$ of abelian [[group object]]s in the [[overcategory]] $CRing/R$ of all rings, over the given ring $R$:

$$
  R Mod \simeq Ab(CRing/R)
  \,.
$$

Under this equivalence an $R$-module $N$ is sent to the square-0-extension ring $R \oplus N$ that is canonically equipped with a ring homomorphism $R \oplus N \to R$ and with a unital and associative and commutative product operation

$$
  (R \oplus N) \times_R (R \oplus N) \to (R \oplus N)
$$

$$
  ((r, n_1), (r,n_2)) \mapsto (r, n_1 + n_2)
$$

that makes it first an object in the [[overcategory]] $CRing/R$ and in there an abelian group object, hence an object in $Ab(CRing/R)$.

Conversely, every module arises this way, up to [[isomorphism]]. So this gives an equivalent way of defining modules over rings.

And this is the right definition. Notably, this definition does not assume anything about the ring $R$. It does not even assume that $R$ is a ring at all! It could be anything.

Concretely: for $C$ _any_ category of test objects -- so that we may think of objects in the [[opposite category]] $C^{op}$ as function rings on the  test objects $C$ -- we may define the category of _module_ s over an object $R \in C^{op}$ by the above equation:

$$
  R Mod := Ab(C^{op}/R)
  \,.
$$

Notice that this is now a definition. And that $R$ could be anything, and the definition still makes sense.

The category of all modules over _all_ possible objects $R$ is then nothing but the [[codomain fibration]]

$$  
  Mod_C := Ab([I,C^{op}]) \stackrel{p_C}{\to} C^{op}
$$

where $I$ is the [[interval category]] and fiberwise (over $C^{op}$) we form abelian group objects. 

This turns out to be the correct [[category theory|category theoretic]] definition of [[module]] (as discussed there). In fact, this is is the special case of the [[higher category theory|higher categorical]] definition that works for $C$ any [[(∞,1)-category]]. In that case the construction $Ab(C^{op}/R)$ of abelian group objects in the [[overcategory]] is generalized (straightforwardly! and in fact even more elegantly) to the notion of [[tangent (∞,1)-category]].

### ... and the correct definition of _derivations_ and _K&#228;hler modules_ {#AbstractDef}

With the above correct notion of [[module]] in hand, all the other concepts of [[deformation theory]], notably those of [[derivation]]s and of K&#228;hler differentials follow straightforwardly

1. given an $R$-module $N$ regarded as an object $p_N : R \oplus N \to R$; the **[[derivation]]s** on $R$ with coefficients in $N$ are precisely the [[section]]s $\delta : R \to R \oplus N$ of $p_N$.

1. The assignment $Spec R \mapsto \Omega_K(Spec R)$ of modules of **K&#228;hler differential**s is the assignment universal with respect to derivations, which means that

   $$
     \Omega_K : C^{op} \to Mod_C
   $$

   is the 
   [[left adjoint]] to the above projection $p_C : Mod_C \to C^{op}$:

   this means that every [[derivation]] $\delta : R \to \mathcal{N}$
   (being a [[section]] in $C$ of the module which is the overcategory
   element $\mathcal{N} \to R$) is identified conversely with a 
   morphism $\Omega_K(R) \to \mathcal{N}$ in the category of
   abelian [[group object]]s in the [[overcategory]]
   $C^{op}/R$:

   $$
      Hom_{Mod_C}(\Omega_K(R), \mathcal{N}) 
      \simeq
      Hom_{C^{op}}(R, \mathcal{N})
      \,.
   $$

Notice that in all of the above now, $C$ is still a
completely arbitrary [[category]].

### The fully general definition

By allowing $C$ -- the collection of test 
spaces -- to be a general [[(∞,1)-category]], the above 
story gives the following completely general [[nPOV]]
on the nature of K&#228;hler differentials:

+-- {: .standout}

For $C$ any [[(∞,1)-category]] of test spaces, write
$p_{C^{op}} : Mod := T_{C^{op}} \to C^{op}$ for the 
[[tangent (∞,1)-category]] of its [[opposite category]]. 

1. the fiber of $Mod \to C^{op}$ over $R \in C^{op}$ is 
   the [[(∞,1)-category]] $R Mod$ of [[module]]s over $R$;

1. for $(p_{\mathcal{N}} : \mathcal{N} \to R) \in R Mod$,
   a [[derivation]] on $R$ with coefficients in $\mathcal{N}$
   is a [[section]] $\delta : R \to \mathcal{N}$ of $p_{\mathcal{N}}$.

1. The assignment of **modules of K&#228;hler differentials** or
   **cotangent complexes** is the [[left adjoint]]

   $$
     \Omega_K : C^{op} \to Mod
   $$

   of the [[tangent (∞,1)-category]] projection $p_{C^{op}}$.

   Its value $\Omega_R(R)$ on an object $R \in C^{op}$ is the
   module of K&#228;hler differentials on $Spec R \in C$.

=--
 

## Specific definitions 

We spell out very concretely definitions of K&#228;hler differentials
for special concrete choices of base category $C$
as special cases of the above general story. We start with the
familiar cases and then work our way up to more general or richer
cases.

### Over ordinary rings {#OrdinaryRings}

In terms of the above discussion, we now take $C = CRing^{op}$ to be the [[opposite category]] of the category of ordinary (commutative unital) [[ring]]. In fact without changing anything of the discusson we may assume that the ring $R$ in question is equipped with a ring homomorphism $k \to R$ from a [[ring]] or [[field]] $k$. This makes $R$ a $k$-[[algebra]], and we shall often speak of algebras in the following, where we could just as well speak of rings.


Suppose $A$ is a [[commutative algebra]] over a field $k$.   We may define K&#228;hler differentials either by an explicit construction or by a universal property. In fact there are two explicit constructions.

The simplest construction, maybe, is as follows. The module of **K&#228;hler differentials** $\Omega^1_K(A)$ over $A$ is generated by symbols $d a$ for all $a\in A$, subject to these relations:

* $d c = 0$ when $c$ is a 'constant', that is, an element of $k$ regarded as an element of $A$.

* $d(a b)=(d a)b+a(d b)$.

* $d(a+b)=d a+d b$.

* $(d a)b = b(d a)$.

In particular there are only finite sums in the module of K&#228;hler differentials.  

Another more sophisticated construction of $\Omega^1_K(A)$ is given below.  But turning to the universal property, note that we can define **derivations** from $A$ to any $A$-[[module]] $M$: they are $k$-linear maps $X : A \to M$ satisfying the product rule:

$$ X(a b) = X(a) b + a X(b) $$

Then $\Omega^1_K(A)$ may be defined as the [[universal property|universal]] $A$-module equipped with a derivation.  In other words, there is a derivation 

$$d : A \to \Omega^1_K(A), $$

and if $X:A\to M$ is any [[derivation]] from $A$ to some $A$-module $M$, then there is a unique $A$-module morphism 

$$\mu_X:\Omega_K^1(A)\to M$$

such that the following diagram commutes:

$$
\array{
A&\overset{X}\to     & M\\
 & \underset{d}\searr&\uparrow \mu_X\\
 &                   & \Omega_K^1{A}
}
$$

We say that $X$ **factors through** $d$.

#### Relative version

We can replace the commutative algebra $A$ more generally by  a [[morphism]] of [[commutative unital rings]] $f:R\to S$. Then the __module of K&#228;hler differentials__ is the $S$-[[module]] $\Omega^1_K(S/R)$ corepresenting the functor

$$Der_R(S,f_*(-)) : S Mod\to Set : M\mapsto Der_R(S,f_* M)$$

that assigns to every $S$-[[module]] $M$ the [[set]] of [[derivations]] on $S$ with values in the (bi)module $f_* M$, where $f_*:S Mod\to R Mod$ is the restriction of scalars. 

In other words,  $Der_R(S,f_*M)\cong Hom_S(\Omega^1_K(S/R),M)$. In a diagram: for every $R$-derivation $X\colon S \to M$ there is a unique morphism (of $S$-modules) $\mu\colon \Omega^1_K(S/R) \to M$ making the following diagram commute:

$$
\array{
S&\overset{X}\to     & M\\
 & \underset{d}\searr&\uparrow \mu\\
 &                   & \Omega^1_K(S/R)
}
$$

This framework also gives another construction of the module of K&#228;hler differentials, instead of the generators and relations definition given above.

Let $I$ be the [[augmentation ideal]], i.e. the [[kernel]] of the multiplication map

$$ I := Ker(m:S\otimes_R S\to S)$$

Then $\Omega^1_K_{S/R}= I/I^2$ and there is a canonical induced map $d: S\to \Omega^1_{S/R}$
given by $d s = [1\otimes s - s\otimes 1]$. 

#### Higher degree K&#228;hler forms

Furthermore, if $R$ is in characteristic zero, one may introduce **K&#228;hler $p$-forms** , which are elements of the $p$-th [[exterior power]] $\Omega^p_K_{S/R}:=\Lambda_R^p \Omega^1_K_{S/R}$. The [[module]] of K&#228;hler differentials readily generalizes as a [[sheaf]] of K&#228;hler differentials for a separated morphism $f:X\to Y$ of (commutative) [[schemes]], namely it is the [[pullback]] along the embedding of the ideal sheaf of the [[diagonal subobject|diagonal subscheme]] $X\hookrightarrow X\times_Y X$.

Compare the role of [[universal differential envelope]] and [[Amitsur complex]] for  analogous constructions in the noncommutative case. The appropriate extension of the module of relative K&#228;hler differentials to the derived setting is the [[cotangent complex]] of Grothendieck--Illusie. 

#### Relation to Hochschild homology

The module of K&#228;hler differentials on $R$ is isomorphic to the first [[Hochschild homology]] of $R$

$$
  \Omega_K^1(R) \simeq HH_1(R,R)
  \,.
$$

Under mild conditions the analogous statement is true for higher K&#228;hler differentials and higher Hochschild homology: this is the [[Hochschild-Kostant-Rosenberg theorem]].


### Over smooth rings regarded as ordinary rings {#SmoothOrPlain}

We have seen that we define K&#228;hler differentials $\Omega^1_K(A)$ for any [[commutative algebra]] $A$.  

The following special case deserves special attention:

The algebra $A = C^\infty(X)$ of smooth functions on some smooth space $X$ (a [[smooth manifold]] or a [[generalized smooth space]]) is in particular a commutative algebra. So one might think that its K&#228;hler differentials form the ordinary [[differential form]]s on $X$ -- in analogy to the case when $A$ consists of the algebraic functions on an affine [[algebraic variety]] in which case K&#228;hler differentials are often taken as a _definition_ of 1-forms.  


#### The problem and its solution

However, when $A = C^\infty(X)$ consists of smooth functions on a manifold, the _ring theoretic_ K&#228;hler differentials do _not_ agree with the ordinary smooth [[differential form|1-form]]s on this manifold! (Unless $X$ is, for instance, the [[point]], of course). 
However, there is a canonical map from the K&#228;hler differentials to the ordinary 1-forms.

But there is a solution to this, and an explanation for why something goes wrong:

Smooth spaces such as [[manifold]]s are _not_ modeled on the category $C =$ [[CRing]]${}^{op}$, as [[varieties]] are. Instead, they are modeled on the category $C = \mathbb{L}$ of [[smooth loci]], which is $= C^\infty Ring^{op}$ the opposite of the category of [[generalized smooth algebra|C-infinity rings]].

In particular, the algebra $A = C^\infty(X)$ of smooth functions on a [[manifold]] carries naturally the structure of such a $C^\infty$-ring. This does have "underlying" it the ordinary commutative ring of functions that forget the $C^\infty$-ring structure, but forgetting this structure is precisely what makes the definition of K&#228;hler differentials fail to reproduce that of ordinary smooth 1-forms.

If we do regard $C^\infty(X)$ as a [[generalized smooth algebra|C-infinity ring]], the its K&#228;hler differentials do agree with ordinary 1-forms on $X$.


#### Detailed comparison

We discuss how K&#228;hler differential forms relate to the ordinary notion of [[differential form]]s.

Since there are only finite sums in the module of K&#228;hler differentials, the usual $d f=f' d t$ works only if $f$ is a finite polynomial in $t$, say, if $A$ is $C^\infty(\mathbb{R})$ ([[smooth map|smooth maps]]) or $\mathbb{R}[\![t]\!]$ ([[power series]]). For example, let $f = t^n$ then

$$\begin{aligned}
d f &= 
d(t^n)  \\
&= t^{n-1} d t  + t(d t^{n-1}) \\
&= 2 t^{n-1} d t + t^2 d(t^{n-2}) \\
&= r t^{n-1} d t + t^r d(t^{n-r}) \\
&= n t^{n-1} d t \\
&= f' d t.
\end{aligned}$$


However, we have

$$d e^t \ne e^t d t$$

as K&#228;hler differentials.  Intuitively, the reason is that $d$ cannot pass through the infinite sum

$$d e^t = d\left(\sum_{n=0}^{\infty} \frac{t^n}{n!}\right) \ne \sum_{n=0}^{\infty} \frac{d(t^n)}{n!} = e^t d t.$$

However, the only proof we know that $d e^t \ne e^t d t$ is quite tricky: in fact it uses the Axiom of Choice!

* David Speyer, K&#228;hler differentials and ordinary differentials.  ([Math Overflow](http://mathoverflow.net/questions/6074/kahler-differentials-and-ordinary-differentials/9723#9723))

It would be  desirable to either find a proof that avoids the Axiom of Choice, or show that axioms beyond ZF are necessary for this result.

To avoid this annoying property of K&#228;hler differentials we can proceed as follows.  Given a commutative algebra $A$, let $Der(A)$ be the $A$-bimodule of derivations.  

Define $\Omega^1(A)$ to be the dual of $Der(A)$:

$$ \Omega^1(A) = Der(A)^* $$

in other words, the set of $A$-module maps $\omega : Der(A) \to A$, made into an $A$-module in the usual way.   There is a derivation

$$ d : A \to \Omega^1(A) $$

given by 

$$ d f (X) = X(f)$$

for $X \in Der(A)$.

Now, suppose  $A=C^\infty(M)$ where $M$ is any smooth manifold.  Then elements of $\Omega^1(A)$ can be identified with ordinary smooth 1-forms on $M$:

from the [[Hadamard lemma]] it follows that $Der(C^\infty(M)) = \Gamma(T M)$ is precisely the $C^\infty(X)$-module of [[vector field]]s on $X$, and [[differential form|1-forms]] are the $C^\infty(X)$-linear duals of vector fields, by definition.

And in this case, one can show that any [[derivation]] $X: A \to M$ factors through $\Omega^1(A)$ when $M$ is free, and in particular if $M=A$. 

We can expand on this remark as follows.  Quite generally, for any commutative algebra $A$ over a field $k$, we have

$$ Der(A) \cong \Omega^1_K(A)^* $$

by the universal property of K&#228;hler differentials, which identifies derivations $A \to A$ with $A$-module morphisms $\Omega^1_K(A) \to A$.

Using the definition 

$$\Omega^1(A) = Der(A)^* $$

(of ordinary smooth 1-forms in the case that $A = C^\infty(M)$) we have that these are the linear bidual of the K&#228;hler differentials:

$$\Omega^1(A) \cong \Omega^1_K(A)^{**} $$

There is always a homomorphism from a module to its double dual, so we have a morphism

$$ j: \Omega^1_K(A) \to \Omega^1(A) $$

In the case when $A = C^\infty(M)$ this map is onto but typically not one-to-one, as witnessed by the fact that
$d e^t = e^t d t$ in the ordinary 1-forms $\Omega^1(A)$
but not in the K&#228;hler differentials $\Omega^1_K(A)$.  However, one can show that when $M$ is a free $A$-module, any derivation $X: A \to M$ not only factors through $\Omega^1_K(A)$ (as guaranteed by the universal property of
K&#228;hler differentials), but also $\Omega^1(A)$.
More generally this is true for torsionless $M$, i.e. $A$-modules that inject into their double duals, since $\Omega^1(A)$ is torsionless. So $\Omega^1_K(A)$ is the universal differential module for all modules, while $\Omega^1(A)$ is the universal differential module for torsionless $A$-modules.

+-- {: .query}
[[Martin Gisser]] Couldn't resist the above uncredentialed drive-by edit...
Is it torsionlessness
that ultimately discerns differential geometry from algebraic geometry?
(Need to fill in more dots between torsionless modules and "geometric modules"
in the sense of Jet Nestruev.)

------------------
[[Eric]]: Does this universal property mean that there is some diagram in some category for which the K&#228;hler differentials can be thought of as a (co)limit?

[[John Baez]]: Yeah, take the category all $A$ modules $M$ equipped with a derivation $X : A \to M$, and take the diagram which consists of every object in this category and every morphism, and take the colimit of that, and you'll get $\Omega^1_K(A)$.  

But this is just a cutesy way to say that $\Omega^1_K(A)$ is the [[initial object]] of this category.  

And _this_, in turn, is just a cutesy way to say that there is a derivation 

$$d : A \to \Omega^1_K(A), $$

such that if $X:A\to M$ is also a derivation, then there exists a unique $A$-module morphism 

$$\mu_X:\Omega_K^1(A)\to M$$

such that the following diagram commutes:

$$
\array{
A&\overset{X}\to     & M\\
 & \underset{d}\searr&\uparrow \mu_X\\
 &                   & \Omega_K^1{A}
}
$$

All this is general abstract nonsense, nothing special to this example!  Any universal property involving maps out of an object says that object is initial in some category --- and that, in turn, is equivalent to saying that object is the colimit of the enormous diagram consisting of all objects of the same kind!  There's a lot less here than meets the eye.

[[Eric]]: Thank you! That actually makes a little sense to me. As trivial as it may seem, the fact that I was even able to ask this question represents tremendous progress :)

[[Herman Stel]]: Dear Eric and Prof. Baez. There is a mistake in the explanation by John Baez here. The two latter properties (both being that the derivation $d : A \to \Omega^1_K(A)$ is initial) are correct. The first one is not, though. If $\Omega^1_K(A)$ were the colimit of the huge diagram then for every derivation there would be a morphism from that derivation to the universal derivation, which is not true. Instead, note that an initial object is the vertex of a colimit of the empty diagram in any category (use that $\forall x\in X P(x)$ is true if $X$ is empty).

=--






### Over smooth rings {#CooCase}

A _$C^\infty$-ring_ (see [[generalized smooth algebra]]) is a ring that remembers that it carries extra smooth structure akin to the smooth structure carried by a ring of smooth functions on a smooth [[manifold]].

If we take a smooth function ring $C^\infty(X)$, regard it as a $C^\infty$-ring and then determine its module of K&#228;hler differentials with respect to the category $C = \mathbb{L} = C^\infty Ring^{op}$, we do recover the ordinary notion of smooth [[differential form]]s.

For the moment, this case is described in detail
in the entry on [[Fermat theory]].


### Over general monoids 

An ordinary (commutative) [[ring]] is precisely a comutative  [[monoid]] in the [[category]] $Ab$ of abelian [[group]]s. 
The case of K&#228;hler differentials over ordinary rings discussed [above](#OrdinaryRings) may therefore be thought of as the case where the category of test objects is taken to be

$$
  C = (CMon(Ab))^{op}
  \,.
$$

This has an evident generalization: we may replace here $Ab$ with _any_ category $K$ and consider

$$
  C = (CMon(K))^{op}
  \,.
$$

In practice $K$ is usually required to be an [[abelian category]], but our definitions so far are general enough not to be concerned about this:

for any such $K$ fixed we follow the [general definition](#AbstractDef), consider the [[functor]]

$$
  p : Mod := Ab([I,CMon(K)^{op}]) \to CMon(K)^{op}
$$

and define the assignment of **K&#228;hler differentials**

$$
  \Omega_K : CMon(K)^{op} \to Ab([I,CMon(K)^{op}])
$$

to be the [[left adjoint]] of this functor.

For this to make good sense, everything here should be regarded as taking place in [[(∞,1)-categories]], typically [[model category|modeled]] by the [[simplicial ring|model structure on simplicial rings]].

Then one finds that for $C = sCRing^{op}$ the corresponding 
notion of module [[(∞,1)-category]] reproduces the 
[[derived category]] of ordinary ring modules.
This is Example 8.6. in

* [[Jacob Lurie]], _Stable $\infty$-categories_ .



#### Over simplicial rings

If in the above setup we choose $K = sAb = [\Delta^{op}, Ab]$ the category of abelian [[simplicial group]]s, then $Mon(K)$ is the category of [[simplicial ring]]s. The category $Mon(K)^{op}$, regarded as a higher category, is the site used in [[higher geometry]] in place of $CRing^{}$

## Related concepts

* [[canonical bundle]]

* [[cotangent complex]], [[André-Quillen homology]], [[topological André-Quillen homology]]

## References


### On smooth rings regarded as ordinary rings

For a proof that every derivation of $A = C^\infty(\mathbb{R})$ comes from a smooth vector field on the real line, and an extensive discussion of K&#228;hler differentials versus ordinary 1-forms, see:

* This Week's Finds in Mathematical Physics ([Week 287](http://math.ucr.edu/home/baez/week287.html))

See also the discussion at the $n$-Caf&#233;:

*  Blog discussion of Week 287.  ([Summary](http://golem.ph.utexas.edu/category/2009/12/this_weeks_finds_in_mathematic_48.html#c030626))

* [The module of K&#228;hler differentials](http://ocw.mit.edu/NR/rdonlyres/Mathematics/18-726Spring-2009/8C4F62C5-7AE2-482B-9643-890EE76499F5/0/MIT18_726s09_lec13_differentials.pdf), MIT OpenCourseWare: 18.726 Algebraic Geometry, Spring 2009.

### On the fully general case

A detailed discussion of K&#228;hler differentials and their generalization from [[algebra]] to [[higher algebra]] is in 

* [[Jacob Lurie]], _[[Deformation Theory]]_


### For a categorical approach, ### 

introducing a setting in which Kahler differentials live quite naturally (but not yet in as much generality as possibly one might hope), see

* [[R. Blute]], [[J.R.B. Cockett]], [[T. Porter]], [[R.A.G.Seely]],  _K&#228;hler categories_,  Cahiers Top. 
G&#233;om. Diff. cat., 52 (2011) 253 &#8211; 268 ([pdf](http://www.math.mcgill.ca/rags/difftl/kahlercahiers.pdf))

####Abstract####
This paper establishes a relation between the recently introduced notion of differential category and the more classic theory of K&#228;hler differentials in commutative algebra. A codifferential category is an additive symmetric monoidal category with a monad, which is furthermore an algebra modality. An algebra modality for a monad T is a natural assignment of an associative algebra structure to each object of the form T(M). In a (co)differential category, one should imagine the morphisms in the base category as being linear maps and the morphisms in the (co)Kleisli category as being infinitely differentiable. Finally, a differential category comes equipped with a differential combinator satisfying typical differentiation axioms, expressed coalgebraically.

The traditional notion of K&#228;hler differentials defines the notion of a module of A-differential forms with respect to A, where A is a commutative k-algebra. This module is equipped with a universal A-derivation. With this in mind, a K&#228;hler category is an additive monoidal category with an algebra modality and an object of differential forms associated to every object. This object of differential forms satisfies a universal property with respect to derivations. Surprisingly, we are able to show that, under some natural conditions, codifferential categories are K&#228;hler. 


[[!redirects Kahler differential]]
[[!redirects Kahler differentials]]
[[!redirects Kähler differentials]]

[[!redirects Kaehler differential]]
[[!redirects Kaehler differentials]]

[[!redirects Kahler differential form]]
[[!redirects Kahler differential forms]]
[[!redirects Kähler differential form]]
[[!redirects Kähler differential forms]]