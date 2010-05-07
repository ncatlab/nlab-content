## Idea

A *lax-idempotent* 2-monad is, roughly, one whose algebras over any given object are essentially unique if they exist.  The archetypal examples are given by 2-monads on $Cat$ that take a category $C$ to the free cocompletion of $C$ under a given class of colimits -- then an algebra is a category with all such colimits, which by universality are essentially unique.


## Definition

A [[2-monad]] $T$ on a [[2-category]] $K$ is called *lax-idempotent* if given any two (strict) $T$-algebras $a \colon T A \to A$, $b \colon T B \to B$ and a morphism $f \colon A \to B$, there exists a unique 2-cell $\bar f \colon b \circ T f \Rightarrow f \circ a$ making $(f,\bar f)$ a lax morphism of $T$-algebras.

### Equivalent conditions

A 2-monad $T$ as above is lax-idempotent iff

* for any $T$-algebra $a \colon T A \to A$ there is a 2-cell $\theta \colon 1 \Rightarrow \eta A \circ a$ such that $(\theta,1_{1_A})$ are the unit and counit of an [[adjunction]] $a \dashv \eta A$.

  Since $T$'s multiplication $\mu$ makes $T$ itself into a (generalized) $T$-algebra, this implies (and in fact is implied by) the requirement that there exist a [[modification]] $\ell \colon 1_{T^2} \to \eta T \circ \mu$ making $(\ell,1_{1_T}) \colon \mu \dashv \eta T$.

* there is a modification $d \colon T \eta \to \eta T$ such that $d \eta = 1$ and $\mu d = 1$.


## References

* Kelly--Lack, _On property-like structures_, TAC 3(9), 1997