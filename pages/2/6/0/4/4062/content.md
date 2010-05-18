## Definition

Given a [[2-category]] $K$, [[adjunction|adjoint pairs]] $(\eta,\epsilon) \colon f \dashv u \colon b \to a$ and $(\eta',\epsilon') \colon f' \dashv u' \colon b' \to a'$ , and 1-cells $x \colon a \to a'$ and $y \colon b \to b'$, there is a bijection
$$ K(a,b')(f' x,y f) \cong K(b,a')(x u,u' y) $$
given by pasting with the unit of one adjunction and the counit of the other, i.e.
$$
\array{
  \array{
    a & \overset{x}{\to} & a' \\

    f \downarrow & \lambda \Downarrow & \downarrow f' \\

    b & \underset{y} & b'
  }

  & \mapsto &

  \array{
    b & \overset{u}{\to} & a & \overset{x}{\to} & a' &             \overset{1}{\to} &     a' \\

    1 \downarrow & \epsilon \Downarrow & f \downarrow &  \lambda             \Downarrow     & \downarrow f' & \Downarrow \eta' & \downarrow 1 \\

    b & \underset{1}{\to} & b & \underset{y} & b' & \underset{u'}{\to}                     & a'
  }
}
$$
and
$$
\array{
  \array{
    b & \overset{y}{\to} & b' \\
 
    u \downarrow & \mu \Uparrow & \downarrow u' \\

    a & \underset{x} & a'
  }

  & \mapsto &

  \array{

    a & \overset{f}{\to} & b & \overset{y}{\to} & b' & \overset{1}{\to} &     b' \\

    1 \downarrow & \eta \Uparrow & u \downarrow & \mu \Uparrow &     \downarrow u' & \Uparrow \epsilon' & \downarrow 1 \\

    a & \underset{1}{\to} & a & \underset{x} & a' & \underset{f'}{\to} &     b'
  }
}
$$
That this is a bijection follows easily from the triangle identities.  The 2-cells $\lambda$ and $\mu$ are called **mates** with respect to the adjunctions $f \dashv u$ and $f' \dashv u'$ (and to the 1-cells $x$ and $y$).

## Example

Let $F \dashv U \colon D \to C$ be an adjunction in the 2-category $Cat$, i.e. a pair of [[adjoint functors]], and $A \colon * \to C$ and $X \colon * \to D$ be objects of $C$ and $D$ considered as functors out of the terminal category $*$.  Then taking mates with respect to $1 \dashv 1 \colon * \to *$ and $F \dashv U$ yields the familiar bijection
$$ D(F A,X) \cong C(A,U X) $$
and the pasting operations as above yield the usual definition of the isomorphism of adjunction by means of unit and counit.

## References

Kelly, G. M., Street, R., _Review of the elements of 2-categories_, in Kelly (ed.), Category Seminar, LNM 420.