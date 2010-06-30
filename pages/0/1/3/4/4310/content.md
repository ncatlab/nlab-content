A **biring** is a [[commutative ring]] $R$ equipped with ring [[homomorphisms]] called **coaddition**:

$$ R \to R \otimes R $$

**cozero**:

$$ R \to \mathbb{Z} $$

**co-additive inverse**:

$$ R \to R $$

**comultiplication**:

$$ R \to R \otimes R $$

and the **multiplicative counit**:

$$ R \to \mathbb{Z} $$

satisfying the usual axioms of a commutative ring, but 'turned around'.  

More tersely, and also more precisely, a biring is a [[internalization|commutative ring object]] in the [[opposite category|opposite]] of the category of commutative rings (also known as the category of [[affine schemes]]).  

Equivalently, a biring is a commutative ring $R$ equipped with a lift of the functor 

$$ hom(R, -) : CommRing \to Set $$

to a functor

$$ hom(R, -) : CommRing \to CommRing $$

Birings form a [[monoidal category]] thanks to the fact that functors of this form are closed under composition.  A [[monoid object]] in this monoidal category is called a [[plethory]].  A plethory is an example of a [[Tall–Wraith monoid]].

The most important example of a biring is $\Lambda$, the ring of [[symmetric polynomials]].  This is actually a plethory.


## References

* D. Tall and [[Gavin Wraith|G. Wraith]], Representable functors and operations on rings, _Proc. London Math. Soc._ **3** (1970), 619--643.
