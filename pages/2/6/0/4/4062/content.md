
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
* automatic table of contents goes here
{:toc}

## Definition

Given a [[2-category]] $K$, [[adjunction|adjoint pairs]] $(\eta,\epsilon) \colon f \dashv u \colon b \to a$ and $(\eta',\epsilon') \colon f' \dashv u' \colon b' \to a'$ , and 1-cells $x \colon a \to a'$ and $y \colon b \to b'$, there is a bijection
$$ K(a,b')(f' x,y f) \cong K(b,a')(x u,u' y) $$
given by [[pasting]] with the unit of one adjunction and the counit of the other, i.e.

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

That this is a bijection follows easily from the [[triangle identities]].  The 2-cells $\lambda$ and $\mu$ are called **mates** (or sometimes **conjugates**) with respect to the adjunctions $f \dashv u$ and $f' \dashv u'$ (and to the 1-cells $x$ and $y$).

## Properties

Strict [[2-functors]] preserve adjunctions and pasting diagrams, so that if $F \colon K \to J$ is a 2-functor and if $\lambda$ and $\mu$ are mates wrt $f \dashv u$ and $f' \dashv u'$ in $K$, then $F \lambda$ and $F \mu$ are mates wrt $F f \dashv F u$ and $F f' \dashv F u'$ in $J$.

If $\alpha \colon F \Rightarrow G$ is a [[2-natural transformation]], then the naturality identities $\alpha_b \circ F f = G f \circ \alpha_a$ and $\alpha_a \circ F u = G u \circ \alpha_b$ are mates wrt $F f \dashv F u$ and $G f \dashv G u$.

### Naturality

There are two [[double categories]] with objects those of $K$, vertical arrows [[adjoint pairs]] in $K$ and horizontal arrows 1-cells of $K$.  In one the 2-cells are those of the form $\lambda$ above, while in the other they are those of the form $\mu$.  It is easily shown, as in Kelly--Street, that the triangle identities and the definition of composition of adjoints make these two double categories isomorphic.  So for any $K$ there is a double category $Adj(K)$, defined up to isomorphism as above but with mate-pairs in $K$ as 2-cells.

What this means is that, for example, the mate of a square coming from a [[pasting diagram]] is given by pasting the mates of the individual 2-cells (whenever this makes sense).

In fact, there is a forgetful functor $L \colon Adj_V(K) \to K$ from the 2-category of objects, adjunctions and mate-pairs in $K$ to $K$ that sends an adjunction $f \dashv u$ to $f$.  It is locally fully faithful, and moreover every $L f$ has a right adjoint in $K$ by definition.  So $L$ makes $Adj(K)$ into a [[2-category equipped with proarrows]].

## Example

Let $F \dashv U \colon D \to C$ be an adjunction in the 2-category $Cat$, i.e. a pair of [[adjoint functors]], and $A \colon * \to C$ and $X \colon * \to D$ be objects of $C$ and $D$ considered as functors out of the terminal category $*$.  Then taking mates with respect to $1 \dashv 1 \colon * \to *$ and $F \dashv U$ yields the familiar bijection
$$ D(F A,X) \cong C(A,U X) $$
and the pasting operations as above yield the usual definition of the isomorphism of adjunction by means of unit and counit.  Moreover, the naturality of the mate correspondence yields naturality of the bijection.

## References

* [[Max Kelly]], [[Ross Street]], _Review of the elements of 2-categories_, in Kelly (ed.), Category Seminar, LNM 420.

* Tom Leinster, _Higher operads, higher categories_, [math.CT/0305049](http://arxiv.org/abs/math/0305049), Section 6.1

[[!redirects mates]]
[[!redirects mate correspondence]]
