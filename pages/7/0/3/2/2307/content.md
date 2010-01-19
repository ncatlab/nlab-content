<div class="rightHandSide toc">
[[!include cohomology - contents]]
</div>

#Contents#
* automatic table of contents goes here
{:toc}

## Definition

_Complex cobordism cohomology theory_, denoted $M U$, is a [[generalized (Eilenberg-Steenrod) cohomology]] theory. 

Its representing [[spectrum]], also denoted $M U$
is the [[spectrum]] is in degree $2 n$ given by the [[Thom space]] of the [[vector bundle]] that is  [[associated bundle|associated]] by the defining [[representation]] of the [[unitary group]] $U(n)$ on $\mathbb{C}^n$ to the [[generalized universal bundle|universtal]] $U(n)$-[[principal bundle]]:

$$
  M U(2n) = Thom
  \left(
    standard associated bundle to universal bundle
    \array{
      E U(n) \\ \downarrow \\ B U(n)
    }
  \right)
$$


The _periodic_ complex cobordism theory is given by adding up all the even degree powers of this theory:

$$
  M P = \vee_{n \in \mathbb{Z}} \Sigma^{2 n} M U
$$

There is a canonical [[oriented cohomology theory|orientation]] on this obtained from the map

$$
  \omega : \mathbb{C}P^\infty \stackrel{\simeq}{\to}
  M U(1)
  \;\;\;\;
  M U(\mathbb{C}P^\infty)
$$

this is the universal even periodic cohomology theory with orientation

The [[cohomology ring]] $M P({*})$ is the [[Lazard ring]] which is the universal coefficient ring for [[formal group law]]s.

## Related entries

for further context see the discussion at

* [[A Survey of Elliptic Cohomology - cohomology theories]]

[[!redirects complex cobordism spectrum]]