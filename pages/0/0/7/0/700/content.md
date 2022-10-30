An [[object]] $A$ in a [[category]] is a **retract** of an object $B$ if there are [[morphism]]s $i:A\to B$ and $r:B\to A$ such that $r i = 1_A$.

In this situation, $r$ is a [[split epimorphism]] and $i$ is a [[split monomorphism]].  Sometimes $r$ is called a **retraction** and $i$ is called a **section**.  Also $A$ is a splitting of the [[idempotent]] $i r$ on $B$.

### Retracts of arrows ###

In the theory of [[weak factorization system]]s and [[model category|model categories]], an important role is played by retracts in the category $C^{\mathbf{2}}$ of arrows in $C$.  Explicitly spelled out in terms of the original category $C$, a morphism $f:X\to Y$ is a retract of a morphism $g:Z\to W$ if we have commutative squares
$$\array{X & \to & Z & \to & X\\
  f \downarrow  & & g \downarrow & & \downarrow f\\
  Y & \to & W & \to & Y}$$
such that the top and bottom rows compose to identities.
