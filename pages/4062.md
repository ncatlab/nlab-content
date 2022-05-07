
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--




#Contents#
* table of contents
{:toc}

## Definition
 {#Definition}

+-- {: .num_prop #MateBijection}
###### Proposition

Given a [[2-category]] $K$, [[adjunction|adjoint pairs]] $(\eta,\epsilon) \colon f \dashv u \colon b \to a$ and $(\eta',\epsilon') \colon f' \dashv u' \colon b' \to a'$ , and [[1-morphisms|1-cells]] $x \colon a \to a'$ and $y \colon b \to b'$, there is a [[bijection]]
$$ K(a,b')(f' x,y f) \cong K(b,a')(x u,u' y) $$
given by [[pasting]] with the [[unit of an adjunction|unit]] of one adjunction and the [[counit of an adjunction|counit]] of the other, i.e.

$$
  \array{
    a & \overset{x}{\to} & a' 
    \\
    \mathllap{f} \downarrow & \mathllap{\lambda} \Downarrow & \downarrow     \mathrlap{f'} 
    \\
    b & \underset{y}{\to} & b'
  }
  \;\;\;\;\;
    \mapsto
  \;\;\;\;\;
  \array{
    b & \overset{u}{\to} & a & \overset{x}{\to} 
    & a' &   \overset{1}{\to} &     a' 
   \\
    \mathllap{1} \downarrow & \mathllap{\epsilon} \Downarrow & \mathllap{f} \downarrow &  
    \mathllap{\lambda}      \Downarrow     & \downarrow \mathrlap{f'} & \Downarrow \mathrlap{\eta'} 
    & \downarrow \mathrlap{1} \\
    b & \underset{1}{\to} & b & \underset{y}{\to} 
    & b' & \underset{u'}{\to}    & a'
  }
$$

and

$$
  \array{
    b & \overset{y}{\to} & b' \\ 
    \mathllap{u} \downarrow & \mathllap{\mu} \Uparrow & \downarrow \mathrlap{u'} \\
    a & \underset{x}{\to} & a'
  }
  \;\;\;\;\;
    \mapsto 
  \;\;\;\;\;
  \array{
    a & \overset{f}{\to} & b & \overset{y}{\to} & b' 
    & \overset{1}{\to} &     b' \\
    \mathllap{1} \downarrow & \mathllap{\eta} \Uparrow & \mathllap{u} \downarrow 
    & \mathllap{\mu} \Uparrow & \downarrow \mathrlap{u'} & \Uparrow \mathrlap{\epsilon'} & \downarrow \mathrlap{1} \\
    a & \underset{1}{\to} & a & \underset{x}{\to} & a' & \underset{f'}{\to} &     b'
  }
$$

=--

+-- {: .proof}
###### Proof

That this is a bijection follows easily from the [[triangle identities]].  

=--

+-- {: .num_defn}
###### Definition

The 2-cells $\lambda$ and $\mu$ in prop. \ref{MateBijection} are called **mates** (or sometimes **conjugates**) with respect to the adjunctions $f \dashv u$ and $f' \dashv u'$ (and to the 1-cells $x$ and $y$).

=--

## Properties

### General

+-- {: .num_prop}
###### Proposition

Strict [[2-functors]] preserve adjunctions and [[pasting diagrams]], so that if $F \colon K \to J$ is a 2-functor and if $\lambda$ and $\mu$ are mates wrt $f \dashv u$ and $f' \dashv u'$ in $K$, then $F \lambda$ and $F \mu$ are mates wrt $F f \dashv F u$ and $F f' \dashv F u'$ in $J$.

=--

+-- {: .num_prop}
###### Proposition

If $\alpha \colon F \Rightarrow G$ is a [[2-natural transformation]], then the naturality identities $\alpha_b \circ F f = G f \circ \alpha_a$ and $\alpha_a \circ F u = G u \circ \alpha_b$ are mates wrt $F f \dashv F u$ and $G f \dashv G u$.

=--

### Naturality

There are two [[double categories]] with objects those of $K$, vertical arrows [[adjoint pairs]] in $K$ and horizontal arrows 1-cells of $K$.  In one the 2-cells are those of the form $\lambda$ above, while in the other they are those of the form $\mu$.  It is easily shown, as in Kelly--Street, that the triangle identities and the definition of composition of adjoints make these two double categories isomorphic.  So for any $K$ there is a double category $Adj(K)$, defined up to isomorphism as above but with mate-pairs in $K$ as 2-cells.

What this means is that, for example, the mate of a square coming from a [[pasting diagram]] is given by pasting the mates of the individual 2-cells (whenever this makes sense).

In the double category $Adj(K)$, every vertical arrow has both a [[companion]] (the left adjoint) and a [[conjoint]] (the right adjoint).  (In fact, in some sense it is the universal double category cosntructed from $K$ with this property.)  Therefore, it is equivalent to a [[2-category equipped with proarrows]].  More explicitly, there is a forgetful functor $L \colon Adj_V(K) \to K$ from the 2-category of objects, adjunctions and mate-pairs in $K$ to $K$ that sends an adjunction $f \dashv u$ to $f$.  It is [[locally fully faithful 2-functor|locally fully faithful]], and moreover every $L f$ has a right adjoint in $K$ by definition; this gives the more traditional definition of a proarrow equipment.

## Examples
 {#Examples}

+-- {: .num_example}
###### Example

Let $F \dashv U \colon D \to C$ be an [[adjunction]] in the [[2-category]] [[Cat]], i.e. a pair of [[adjoint functors]], and $A \colon * \to C$ and $X \colon * \to D$ be objects of $C$ and $D$ considered as [[functors]] out of the [[terminal category]] $*$.  Then taking mates with respect to $1 \dashv 1 \colon * \to *$ and $F \dashv U$ yields the [hom-isomorphism](adjoint+functor#InTermsOfHomIsomorphism)
$$ 
  D(F A,X) \;\cong\; C(A,U X) 
$$
and the pasting operations as above yield the usual definition of the isomorphism of adjunction by means of [[unit of an adjunction|unit]] and [[counit of an adjunction|counit]].  Moreover, the naturality of the mate correspondence yields [[natural isomorphism|naturality]] of the bijection.

=--

+-- {: .num_example}
###### Example

If the ambient [[2-category]] $K$ is the [[delooping]] of a [[monoidal category]] $(\mathcal{C}, \otimes)$ in that

$$
  K \simeq \mathbf{B}_\otimes \mathcal{C}
$$

then an [[adjunction]] in $K$ is a pair of [[dual objects]] and the mate-construction is the construction of [[dual morphisms]] between [[dualizable objects]].

=--

+-- {: .num_example}
###### Example


Suppose given a [[commutative square]] (up to [[isomorphism]]) of [[functor]]s:
$$\array{ & \overset{f^*}{\to} & \\
  ^{g^*}\downarrow && \downarrow^{k^*}\\
  & \underset{h^*}{\to} & }$$
in which $f^*$ and $h^*$ have [[left adjoint]]s $f_!$ and $h_!$, respectively. (The classical example is a [[Wirthmüller context]].)  Then the [[natural isomorphism]] that makes the square commute 

$$
  k^* f^* \to h^* g^*
$$

has a mate

$$ 
  h_! k^* \to g^* f_! 
$$

defined as the composite

$$ 
  h_! k^* \overset{\eta}{\to} h_! k^* f^* f_! \overset{\cong}{\to} h_! h^* g^* f_! \overset{\epsilon}{\to} g^* f_!   
  \,.
$$

Ones says that the original square satisfies the **[[Beck-Chevalley condition]]** if this mate is an [[equivalence]].

=--

## Multi-variable mates

There is a version of the mate correspondence that applies to [[two-variable adjunctions]] and $n$-variable adjunctions; see [Cheng-Gurski-Riehl](#CGR).

The relationship between two of the adjoints in a multivariable adjunction can be described as a **parametrized adjunction**: fixing the variables in each of the categories that appear in the domains of both adjoints, the pair of functors define an adjunction between the remaining two categories. Relative to the parametrized adjunctions that define a multivariable adjunction, the multivariable mates can be understood as [parametrized mates](https://golem.ph.utexas.edu/category/2012/11/parametrized_mates_and_multiva.html). 

## References

* [[Max Kelly]], [[Ross Street]], _Review of the elements of 2-categories_, in Kelly (ed.), Category Seminar, LNM 420.

* [[Tom Leinster]], _Higher operads, higher categories_, [math.CT/0305049](http://arxiv.org/abs/math/0305049), Section 6.1

* {#CGR} [[Eugenia Cheng]], [[Nick Gurski]], [[Emily Riehl]], "Multivariable adjunctions and mates", [arXiv:1208.4520](http://arxiv.org/abs/1208.4520), (to appear: Journal of K-Theory).

* "Parametrized mates and multivariable adjunctions" [blog post](https://golem.ph.utexas.edu/category/2012/11/parametrized_mates_and_multiva.html)

{#ReferencesGeneralizationtoBicategories} Generalization to [[bicategories]] is discussed in

* [[Aaron Lauda]], &#167;3 of _Frobenius algebras and ambidextrous adjunctions_, Theory and Applications of Categories, 16:84&#8211;122, 2006. 52

* [[Richard Garner]], [[Michael Shulman]], around 13.7 of _Enriched categories as a free cocompletion_ ([arXiv:1301.3191](https://arxiv.org/abs/1301.3191))

[[!redirects mates]]
[[!redirects mate correspondence]]
[[!redirects mates correspondence]]
