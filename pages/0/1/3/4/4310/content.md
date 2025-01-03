
#Contents#
* table of contents
{:toc}

## The idea

Just as a [[bimonoid]] is both a [[monoid]] and a [[comonoid]] in a compatible way, a 'biring' is both a commutative [[ring]] and a commutative [[coring]] in a compatible way.

##Definition##

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

The most important example of a biring is $\Lambda$, the ring of [[symmetric polynomials]].  This is actually a [[plethory]].

## Categorified Birings ##

The biring $\Lambda$ is the [[Grothendieck group]] of the category of [[Schur functors]], which is equivalent to the [[functor category]]

$$[\mathbb{P}, FinDimVect] $$

where $\mathbb{P}$ is the [[permutation groupoid]] and [[FinDimVect]] is the category of [[finite-dimensional vector spaces]] over a [[field]] $k$ of [[characteristic zero]].  $\Lambda$ is also the [[Grothendieck group]] of 

$$[\mathbb{P}, Vect ]$$

where we drop the finite-dimensionality restriction on our vector spaces and work with all of [[Vect]].

This suggests that the biring structure of $\Lambda$ may emerge naturally from a 'categorified biring' structure on $[\mathbb{P}, Vect ]$.  In this section we sketch how such a categorified biring might be constructed, based on the assumption that there is a tensor product of [[cocomplete category|cocomplete]] [[linear categories]] with good universal properties.  

Namely, we assume that given cocomplete linear categories $X$ and $Y$, there is a cocomplete linear category $X \otimes Y$ such that:

* There is a linear functor $i: X \times Y \to X \otimes Y$ which is [[cocontinuous functor|cocontinuous]] in each argument.

* For any cocomplete linear category $Z$, the category of linear functors $X \otimes Y \to Z$ is equivalent to the category of linear functors $X \times Y \to Z$ that are [[cocontinuous functor|cocontinuous]] in each argument, with the equivalence being given by precomposition with $i$.

With any luck these two assumptions will let us show that for any categories $A$ and $B$, 
\[ [A \times Y, Vect] \simeq [A,Vect] \otimes [B, Vect] \label{tensor} \]
where we use $[-,-]$ to denote the [[functor category]].

Assuming all this, we obtain the following operations on the category $[\mathbb{P}, Vect]$:

1. **Addition**: form the composite functor
$$ [\mathbb{P}, Vect] \times  [\mathbb{P}, Vect]  \to [\mathbb{P}, Vect \times Vect] \to  [\mathbb{P}, Vect] $$
where the last arrow comes from postcomposition with 
$$ \oplus : Vect \times Vect \to Vect $$
This composite is our **addition**:
$$ \oplus :  [\mathbb{P}, Vect] \times  [\mathbb{P}, Vect] \to  [\mathbb{P}, Vect] $$
It's really just the coproduct in $[\mathbb{P}, Vect]$.

1. **Multiplication**: first form the composite functor
$$ [\mathbb{P}, Vect] \times  [\mathbb{P}, Vect]  \to [\mathbb{P}, Vect \times Vect] \to  [\mathbb{P}, Vect] $$
where the last arrow comes from postcomposition with 
$$ \otimes : Vect \times Vect \to Vect $$
This composite is our **multiplication**:
$$ \otimes :  [\mathbb{P}, Vect] \times  [\mathbb{P}, Vect] \to  [\mathbb{P}, Vect] $$
Since this product preserves colimits in each argument, if we use the hoped-for universal property of the tensor product of cocomplete linear categories, we can reinterpret this as a cocontinuous functor
$$  \otimes:  [\mathbb{P}, Vect] \otimes  [\mathbb{P}, Vect]  \to  [\mathbb{P}, Vect] $$

1. **Coaddition**: Form the composite functor
$$  [\mathbb{P}, Vect] \to [\mathbb{P} \times \mathbb{P} , Vect] \to [\mathbb{P}, Vect] \otimes [\mathbb{P}, Vect] $$
where the first arrow comes from precomposition with the addition operation on $\mathbb{P}$ (a restriction of [[coproduct]] in [[FinSet]]), and the second comes from our hoped-for relation \eqref{tensor}.  This is our **coaddition**:
$$  coadd: [\mathbb{P}, Vect] \to [\mathbb{P}, Vect] \otimes [\mathbb{P}, Vect] $$

1.  **Comultiplication**: Form the composite functor
$$  [\mathbb{P}, Vect] \to [\mathbb{P} \times \mathbb{P} , Vect] \to [\mathbb{P}, Vect] \otimes [\mathbb{P}, Vect] $$
where the first arrow comes from precomposition with the multiplication operation on $\mathbb{P}$ (a restriction of [[product]] in [[FinSet]]), and the second comes from our hoped-for relation \eqref{tensor}.  This is our **comultiplication**:
$$  comult: [\mathbb{P}, Vect] \to [\mathbb{P}, Vect] \otimes [\mathbb{P}, Vect] $$

The additive and multiplicative unit and counit may be similarly defined.  Note that we are using rather little about $\mathbb{P}$ and $Vect$ here.  For example, the category of ordinary non-linear [[species]], $[\mathbb{P}, Set]$, should also become a categorified biring if there is a tensor product of cocomplete categories with properties analogous to those assumed for cocomplete $k$-linear categories above.  But we could also replace $\mathbb{P}$ by any [[rig category]].  So, 'biring categories', or more precisely 'birig categories', should be fairly common.  

## References

* D. Tall, [[Gavin Wraith]]: *Representable functors and operations on rings*,  Proc. London Math. Soc. **s3-20** 4, (1970) 619-643 &lbrack;[doi:10.1112/plms/s3-20.4.619](http://dx.doi.org/10.1112/plms/s3-20.4.619), [MR265348](http://www.ams.org/mathscinet-getitem?mr=265348)&rbrack;

[[!redirects birings]] 
[[!redirects bi-ring]] 
[[!redirects bi-rings]] 
