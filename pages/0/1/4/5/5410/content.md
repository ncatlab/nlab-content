
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### 2-category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--

* table of contents
{:toc}

## Two-sided fibrations

### Idea

Recall that a [[functor]] $E \to B$ is called a *[[fibration]]* if its [[fibres]] $E_b$ vary ([[pseudofunctor|pseudo-]])[[functor|functorially]] in $b$.  Taking here _fibre_ to mean _strict fibre_ results in the notion of [[Grothendieck fibration]], while taking it to mean [[essential fibre]] gives the notion of [[Street fibration]].

Similarly, a *two-sided fibration* $A \leftarrow E \to B$ is a [[span]] of functors whose joint fibres $E(a,b)$ vary functorially in both $a$ and $b$ ([[contravariant functor|contravariantly]] in one and [[covariant functor|covariantly]] in the other).

This notion should not be confused with a [[bifibration]], which is a functor that is both a [[fibration]] and a [[cofibration]].

### Definition

Let $K$ be a [[bicategory]] with finite [[2-limits]], and recall that [[fibration in a 2-category|fibrations]] in $K$ may be defined in any of several ways.  Each of these has an analogous version for two-sided fibrations.


#### In terms of 2-monads

Recall that (cloven) fibrations $E \to B$ in $K$ are the (pseudo)algebras for a (pseudo) 2-monad $L$ on $K/B$.  For a morphism $p \colon E \to A$ in $K$, $L p$ is given by composing the [[span]] $A \overset{p}{\leftarrow} E \to 1$ with the canonical span $\Phi A = A \overset{dom}{\leftarrow} A^{\mathbf{2}} \overset{cod}{\to} A$, so that $L p \colon E/p \to A$ is the canonical projection.  This can equivalently be described as the [[comma object]] $(1_A/p)$.  This 2-monad is [[lax-idempotent 2-monad|lax-idempotent]], so that $p\colon E\to B$ is a fibration if and only if the unit $p\to L p$ has a left adjoint with invertible counit.

More generally, the same construction gives a 2-monad $L$ on $Span K(B,A)$, whose algebras we call **left fibrations**.  In [[Cat]], a span $C \overset{p}{\leftarrow} H \overset{q}{\to} D$ is a left fibration if $p$ is a cloven fibration whose chosen cartesian lifts are $q$-vertical.  (Since we are working bicategorically, "$q$-vertical" means that they map to isomorphisms under $q$.)

Dually, there is a colax-idempotent 2-monad $R$ on each $Span K(B,A)$ whose algebras
are called **right fibrations**, the special case of $Span Cat(D,1)$ yielding cloven opfibrations.

There is then a composite 2-monad $M$ that takes a span $E$ from $B$ to $A$ to $M E = \Phi A \circ E \circ \Phi B$, and $M$-algebras are called **two-sided fibrations**.  Although $M$ is neither lax- nor colax-idempotent, it is still [[property-like 2-monad|property-like]].

+-- {: .num_prop #TwoSidedFibrationsInCat}
###### Proposition

A two-sided Street fibration from $B$ to $A$ in $Cat$ is given by a span $p \colon E \to A$, $q \colon E \to B$ such that

1. each $i \colon a \to p x$ in $A$ has a $p$-[[cartesian morphism|cartesian]] lift $\kappa_i \colon i^* x \to x$ in $E$ that is $q$-vertical (that is, $E$ is a left fibration)

1. each $j \colon q x \to b$ in $B$ has a $q$-opcartesian lift $\kappa^j \colon x \to j_! x$ in $E$ that is $p$-vertical ($E$ is a right fibration)

1. for every cartesian--opcartesian composite $i^* x \to x \to j_! x$ in $E$, the canonical morphism $j_! i^* x \to i^* j_! x$ is an [[isomorphism]].
=--

+-- {: .proof}
###### Proof

By the usual theory of [[distributive laws]], an $M$-algebra $m \colon M E \to E$ gives rise to $L$- and $R$-algebras $m \cdot (\Phi A \circ \eta^R_E)$ and $m \cdot (\eta^L_E \circ \Phi B)$, and conversely an $L$-algebra $\ell$ and an $R$-algebra $r$ underlie an $M$-algebra if and only if there is an isomorphism $r \cdot (\ell \circ \Phi B) \cong \ell \cdot (\Phi A \circ r)$ that makes $r$ a morphism of $L$-algebras.

Now given $\ell$ and $r$, because $L$ is [[colax-idempotent]], there is a unique 2-cell $\bar r \colon r \cdot (\ell \circ \Phi B) \Rightarrow \ell \cdot (\Phi A \circ r)$ that makes $r$ a colax morphism of $L$-algebras.  So we want to show that in the case of $Cat$, the components of this natural transformation are the canonical morphisms of (3).

The 2-cell $\bar r$ is given by $\ell \cdot (\Phi A \circ r) \cdot (\epsilon \circ \Phi B)$, where $\epsilon$ is the counit of the adjunction $\eta^L_E \dashv \ell$.  Its components are thus given, for each $i \colon a \to p x$ in $A$ and $j \colon p x \to b$ in $B$, by first factoring $\kappa^j \kappa_i$ through the opcartesian $i^* x \to j_! i^* x$ and then factoring the result through the cartesian $i^* j_! x  \to j_! x$, to obtain exactly the canonical morphism $j_! i^* x \to i^* j_! x$.

=--

If $A \overset{p}{\leftarrow} E \overset{q}{\to} B$ is a two-sided fibration, then the operation sending $(a,b)$ to the corresponding (essential) fiber of $(p,q)$ defines a pseudofunctor $A^{op}\times B \to Cat$.  The third condition in Proposition \ref{TwoSidedFibrationsInCat} corresponds to the "interchange" equality $(\alpha,1)(1,\beta) = (1,\beta)(\alpha,1)$ in $A^{op}\times B$.  We write $Fib(B,A)$ for the 2-category of two-sided fibrations from $B$ to $A$.


#### A representable definition

Another definition of internal fibration is that a (cloven) fibration in $K$ is a morphism $p\colon E\to B$ such that $K(X,p)\colon K(X,E)\to K(X,B)$ is a (cloven) fibration in $Cat$, for any $X\in K$, and for any $X\to Y$ the corresponding square is a morphism of fibrations in $Cat$.  To adapt this definition to two-sided fibrations, we therefore need only to say what is a two-sided fibration in $Cat$.  For this we can use the characterization of Proposition \ref{TwoSidedFibrationsInCat}.


#### As iterated fibrations

Let $Fib(A) = Fib_K(A)$ denote the 2-category of fibrations over $A\in K$.  It is a well-known fact (apparently due to Benabou) that a morphism in $Fib(A)$ is a fibration in $Fib(A)$ if and only if its underlying morphism in $K$ is a fibration.  See [[fibration in a 2-category]].  Thus, for any fibration $r\colon C\to A$, we have $Fib_{Fib_K(A)}(r) \simeq Fib_K(C)$.

Of course there is a dual result for opfibrations: for any opfibration $r\colon C\to A$ we have $Opf_{Opf_K(A)}(r) \simeq Opf_K(C)$.  When we combine variance of iteration, however, we obtain two-sided fibrations.

+--{: .un_theorem}
###### Theorem
A span $A \overset{p}{\leftarrow} E \overset{q}{\to} B$ is a two-sided fibration from $B$ to $A$ if and only if

1. $p\colon E\to A$ is a fibration and

1. $(p,q)\colon E\to A\times B$ is an opfibration in $Fib(A)$.
=--

+--{: .proof}
###### Proof
Recall that the projection $A\times B \to A$ is a fibration (and also an opfibration, although that is irrelevant here), and the cartesian 2-cells are precisely those whose component in $B$ is an isomorphism.  Therefore, saying that $(p,q)$ is a _morphism_ in $Fib(A)$, i.e. that it preserves cartesian 2-cells, says precisely that $q$ takes $p$-cartesian 2-cells to isomorphisms.

Now $q$ is an opfibration in $K$ iff $E\to (q/1_B)$ has a left adjoint with invertible counit in $K/B$, and $(p,q)$ is an opfibration in $Fib(A)$ iff $E\to ((p,q)/1_{A\times B})$ has a left adjoint with invertible counit in $Fib(A)/(A\times B)$.  Of crucial importance is that here $((p,q)/1_{A\times B})$ denotes the comma object calculated _in the 2-category $Fib(A)$_, or equivalently in $K/A$ (since monadic forgetful functors create limits), and it is easy to check that this is in fact _equivalent_ to the comma object $(q/1_B)$ calculated in $K$.

Therefore, $(p,q)$ is an opfibration in $Fib(A)$ iff $q$ is an opfibration in $K$ and the left adjoint of $E\to (q/1_B)$ is a morphism in $Fib(A)$.  It is then easy to check that this left adjoint is a morphism in $K/A$ iff $p$ inverts $q$-opcartesian arrows, and that it is a morphism of fibrations iff the final condition in Proposition \ref{TwoSidedFibrationsInCat} is satisfied.
=--

In particular, we have $Fib(B,A) \simeq Opf_{Fib(A)}(A\times B)$.  By duality, $Fib(B,A) \simeq Fib_{Opf(B)}(A\times B)$, and therefore $Fib_{Opf(B)}(A\times B) \simeq Opf_{Fib(A)}(A\times B)$, a commutation result that is not immediately obvious.

This result appears in [Bourn--Penon](#BournPenon); it was noticed independently and recorded here by [[Mike Shulman]].


## Two-sided discrete fibrations

### Definition

A two-sided fibration $A \leftarrow E \to B$ in $K$ is **discrete** if it is [[discrete object|discrete]] as an object of $K/A \times B$.  Since discreteness is a limit construction, it is created by monadic forgetful functors; hence this is equivalent to being discrete as an object of the 2-category $Fib(A,B)$ of two-sided fibrations.

For Grothendieck fibrations in [[Cat]], this means the following.

+-- {: .un_defn}
###### Definition

A **two-sided discrete fibration** is a [[span]] $q \colon E \to A$, $p \colon E \to B$ of [[categories]] and [[functors]] such that
 
1. each $b \to p(e)$ in $B$ has a unique lift in $E$ that has codomain $e$ and is in the fiber over $q(e)$
1. each $q(e) \to a$ in $A$ has a unique lift in $E$ that has domain $e$ and is in the fiber over $p(e)$
1. for each $f\colon e \to e'$ in $E$, the codomain of the lift of $q(f)$ equals the domain of the lift of $p(f)$ and their composite is $f$.

=--

We write 

$$
  DFib(A,B) \subset Span(A,B)
$$ 

for the full [[subcategory]] on the 2-category $Span K(A,B)$ of [[span]]s on the 2-sided discrete fibrations.  Since a morphism of spans between discrete fibrations is automatically a morphism of fibrations, this is also the full sub-2-category of the 2-category of two-sided fibrations $Fib(A,B)$.  And since they are discrete objects, this 2-category is actually (equivalent to) a 1-category.

Note, though, that the two legs of a two-sided discrete fibration are not necessarily individually discrete as a fibration and an opfibration.


### Properties

#### Profunctors and collages

+-- {: .un_defn}
###### Definition

Given a profunctor $F : B^{op} \times A \to Set$,
its [[collage]] is the category $K_F$ over the [[interval category]] 

$$
  p : K_F \to \Delta[1]
$$ 

With $p^{-1}(0) = B$, $p^{-1}(1) = A$, $K_F(b,a) = F(b,a)$ 
and $K_F(a,b) = \emptyset$ for all $b \in B$, $a \in A$, where 

* the composite of $b \stackrel{e}{\to} a$ with $a \stackrel{f}{\to} a'$ is given by $F(b,f)(e)$;

* the composite of $b \stackrel{g}{\to} b'$ with $b' \stackrel{e'}{\to} a'$ is given by $F(g, a')(e')$.


=--


+-- {: .un_prop #EquivDFibWithProf}
###### Proposition

There is an [[equivalence of categories]]

$$
  [B^{op} \times A, Set]
    \stackrel{\simeq}{\to}
  DFib(A,B) 
$$

$$
  F \mapsto E_F
  \,,
$$

[[pseudo-natural transformation|pseudo-natural]] in $A, B \in Cat$, between [[profunctor]]s in [[Set]] and two-sided discrete fibrations from $A$ to $B$, where $E_F$ is the category whose

* objects are [[section]]s $\sigma : \Delta[1] \to K_F$ of the [[collage]]
  $p : K_F \to \Delta[1]$

* morphisms are [[natural transformation]]s between such sections;

* the two projections $A \leftarrow E_F \to B$ are the two functors induced
  by restriction along $\{0\} \to \Delta[1] \leftarrow \{1\}$.

=--


+-- {: .proof}
###### Proof

First we write out $E_F$ in detail. In the following $b, b', \cdots \in B$
and $a,a', \dots \in A$.

The objects of $E_F$ are morphisms

$$
  \array{
    b 
    \\
    {}^{\mathllap{e}}\downarrow
    \\
    a
  }
$$

in $K_F$, hence triples $(b \in B, a \in A, e \in F(b,a))$.

Morphisms are [[commuting diagram]]s

$$
  \array{
    b &\stackrel{g}{\to}& b'
    \\
    {}^{\mathllap{e}}\downarrow && \downarrow^{\mathrlap{e'}}
    \\
    a &\stackrel{f}{\to}& a'
  }
$$

in $K_F$. We may identify these with pairs $((b \stackrel{g}{\to}b') \in B,(a \stackrel{f}{\to} a') \in A)$ such that 

$$
  F(g,a')(e') = F(b,f)(e)
  \,.
$$ 

We check that this construction yields a two-sided fibration. The three conditions are

1. For
  
   $$
     \array{
        b 
        \\
        {}^{\mathllap{e}}\downarrow
        \\
        a
     }
   $$

   an object of $E_F$ and $a \stackrel{f}{\to} a'$ a morphism in $A$,
   we have that

   $$
     \array{
        b &\stackrel{Id}{\to}& b
        \\
        {}^{\mathllap{e}}\downarrow 
        & & 
        \downarrow^{\mathrlap{f e}}
        \\
        a &\underset{f}{\to}& a'
     }
   $$

   is the unique lift to a morphism in $E$ that maps to $Id_b$.

1. Analogously, for
  
   $$
     \array{
        b' 
        \\
        {}^{\mathllap{e'}}\downarrow
        \\
        a'
     }
   $$

   an object of $E_F$ and $b \stackrel{g}{\to} b'$ a morphism in $B$,
   we have that

   $$
     \array{
        b &\stackrel{g}{\to}& b'
        \\
        {}^{\mathllap{e' g}}\downarrow 
        & & 
        \downarrow^{\mathrlap{e'}}
        \\
        a' &\underset{id}{\to}& a'
     }
   $$

   is the unique lift to a morphism in $E$ that maps to $Id_{a'}$.

1. For 
   
   $$
     \array{
        b &\stackrel{g}{\to}& b'
        \\
        {}^{\mathllap{e}}\downarrow && 
        \downarrow^{\mathrlap{e'}}
        \\
        a &\underset{f}{\to}& a'
     }
   $$

   an arbitrary morphism in $E_F$, these two unique lifts of its $A$- and its
   $B$-projection, respectively, are

   $$
     \array{
        b &\stackrel{Id}{\to}& b
        \\
        {}^{\mathllap{e}}\downarrow 
        & & 
        \downarrow^{\mathrlap{f e}}
        \\
        a &\underset{f}{\to}& a'
     }
   $$

   and

   $$
     \array{
        b &\stackrel{g}{\to}& b'
        \\
        {}^{\mathllap{e' g}}\downarrow & & 
        \downarrow^{\mathrlap{e'}}
        \\
        a' &\underset{Id}{\to}& a'
     }
     \,.
   $$

   The codomain and domain do match, since $f e = e' g$   by the 
   existence of the original morphism, and their composite is the original 
   morphism

   $$
     \array{
        b &\stackrel{Id}{\to}& b &\stackrel{g}{\to}& b
        \\
        {}^{\mathllap{e}}\downarrow 
        & & 
        {}^{\mathllap{f e}}\downarrow^{\mathrlap{e' g}}
         &&
         \downarrow^{\mathrlap{e'}}
        \\
        a &\underset{f}{\to}& a' &\stackrel{Id}{\to}& a'
     }    
     \,.
   $$

To see that this construction indeed yields an equivalence of categories, define a functor $(A\leftarrow E \to B) \mapsto (F_E : B^{op} \times A \to Set)$ by setting

* $F_E(b,a) := E_{b,a}$;

* for a morphism $b \stackrel{g}{\to} b'$ let $F_E(g,a') : F_E(b',a') \to F_E(b,a')$ be the function that sends $b' \stackrel{e'}{\to} a'$ to the domain of the unique lift of $b \stackrel{g}{\to} b'$ with this codomain and mapping to $Id_{a'}$;

* for a morphism $a \stackrel{f}{\to} a'$ let $F_E(b,f) : F_E(b,a) \to F_E(b,a')$ be the function that sends $b \stackrel{e}{\to} a$ to the codomain of the unique lift of $a \stackrel{f}{\to} a'$ with this domain and mapping to $Id_{b}$;.

One checks that this yields an equivalence of categories. 

=--

\begin{remark}
The category $E_F$ is equivalently characterized as being the [[comma category]] of the diagram $B \to K_F \leftarrow A$.
\end{remark}

Note that profunctors can also be characterized by their collages, these being the two-sided [[codiscrete cofibrations]]; and the collage corresponding to a two-sided fibration is its [[cocomma object]].


### Relation to distributive laws

Fibrations and opfibrations on a category $C$ (or more generally an object of a suitable 2-category) are the algebras for a pair of pseudomonads.  If $C$ has pullbacks, there is a [[pseudo-distributive law]] between these pseudomonads, whose joint algebras are the two-sided fibrations satisfying the [[Beck-Chevalley condition]]; see [von Glehn (2015)](#vonGlehn).


## Related concepts

* [[Grothendieck fibration]], 

 * [[Street fibration]], 

* [[discrete fibration]], 

*  [[fibration in a 2-category]], 

*  **two-sided fibration**, 

*  [[Conduche functor]]

* [[Cartesian fibration]]

## References

An early reference is the notion of "regular span" on page 535 of:

* [[Nobuo Yoneda]], *On ext and exact sequences* (PhD thesis), Journal of the Faculty of Science, Section I. **8** University of Tokyo (1960) 507–576 &lbrack;[pdf](http://alpha.math.uga.edu/~lorenz/YonedaExtExactSequences.pdf), [CiNii:naid/500000325773](https://ci.nii.ac.jp/naid/500000325773)&rbrack;

Original discussion:

* [[Ross Street]]. _Fibrations and Yoneda's lemma in a 2-category_. In Category Seminar (Proc. Sem., Sydney, 1972/1973), pages 104  133. Lecture Notes in Math., Vol. 420. Springer, Berlin, 1974.

* [[Ross Street]], _Fibrations in bicategories_. Cahiers Topologie G&#233;om. Diff&#233;rentielle,
21(2):111--160, 1980. (Corrections in 28(1):53--56, 1987)

Further discussion of discrete fibrations 


* {#BournPenon} [[Dominique Bourn]], [[Jacques Penon]],  _2-cat&#233;gories r&#233;ductibles_.  Preprint, University of Amiens Department of Mathematics, 1978.  Reprinted as _TAC Reprints_ no. 19, 2010 ([link](http://www.tac.mta.ca/tac/reprints/articles/19/tr19abs.html)).

Useful reviews are in

* [[Emily Riehl]], _Two-sided discrete fibrations in 2-categories and bicategories_ 2010 ([pdf](https://math.jhu.edu/~eriehl/fibrations.pdf))
{#Riehl}

* [[Fosco Loregian]] and [[Emily Riehl]], _Categorical notions of fibration_, [arxiv](https://arxiv.org/abs/1806.06129)

In relation to [[categorical semantics of dependent types]]:

* {#vonGlehn2015} [[Tamara von Glehn]], *Polynomials and models of type theory*, PhD thesis (2015) &lbrack;[doi10.17863/CAM.16245](https://doi.org/10.17863/CAM.16245)&rbrack;


[[!redirects two-sided fibrations]]
[[!redirects two-sided discrete fibration]]
[[!redirects two-sided discrete fibrations]]


[[!redirects 2-sided fibration]]
[[!redirects 2-sided fibrations]]
[[!redirects 2-sided discrete fibration]]
[[!redirects 2-sided discrete fibrations]]