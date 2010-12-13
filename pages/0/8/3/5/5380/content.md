
#Contents#
* table of contents
{:toc}

## Definition

Let $T$ be an abelian [[Lawvere theory]] (one containing the theory of [[abelian group]]s). Write $\mathbb{A}^1$ for its canonical [[line object]] and $\mathbb{G}$ for the corresponding group object.

The **projective space** $\mathbb{P}_n$ of $T$ is the [[quotient]]

$$
  \mathbb{P}_n := (\mathbb{A}^{n+1} - \{0\})/\mathbb{G}
$$

of the $(n+1)$-fold [[product]] of the line with itself by the canonical [[action]] of $\mathbb{G}$.

More generally, for $X$ a space with $\mathbb{G}$-[[action]], the quotient 

$$
 \mathbb{P}(X) :=  X/\mathbb{G}
$$ 

is the corresponding projective space.


### Examples

#### For commutative rings

For $T$ the theory of commutative [[ring]]s, $\mathbb{A}^1$ is the standard [[affine line]]. In this case $\mathbb{P}_n$ is (...)

**Claim**

For $R$ a commutave ring, an [[action]] of $\mathbb{G}$ on $Spec R$ is equivalently a $\mathbb{Z}$-grading on $R$.

Skecth of the proof:

Notice that the product structure on $\mathbb{G}$

$$
  \mathbb{G} \times \mathbb{G} \to \mathbb{G}
$$

is dually the ring homomorphism

$$
  \mathbb{Z}[t_1, t_2] \leftarrow \mathbb{Z}[t]
$$

given by

$$
  t \mapsto t_1 \cdot t_2
  \,.
$$

Let $R$ be a $\mathbb{Z}$-graded commutative ring. Then $X = Spec R$ comes with a $\mathbb{G}$-action given as follows: the action morphism

$$
 \rho :  X \times \mathbb{G} \to X
$$

is dually the ring homomorphism

$$
  R \otimes \mathbb{Z}[t] \leftarrow R
$$

defined on homogeneous elements $r$ of degree $n$ by

$$
  r \mapsto r \cdot t^n
  \,.
$$

The action property

$$
  \array{
     X \times \mathbb{G} \times \mathbb{G} &\stackrel{Id \times \cdot}{\to}& X \times \mathbb{G}
     \\
     {}^{\mathllap{\rho} \times Id}\downarrow && \downarrow^{\mathrlap{\rho}}
     \\
     X \times \mathbb{G} &\to& X
  }
$$

is equivalently the equation

$$
  r (t_1)^n \cdot (t_2)^n = r (t_1 \cdot t_2)^n
  \,.
$$

Similarly the unitality of the action is the equation

$$
  (1)^n = 1
  \,.
$$

Conversely, one finds that for every $R$ equipping $Spec R$ with a $\mathbb{G}$-action is the same as putting a $\mathbb{Z}$-grading on $R$.

## References

An introduction to projective spaces over the theory of ordinary commutative rings is in

* Miles Reid, _Graded rings and varieties in weighted projective space_ ([pdf](http://www.warwick.ac.uk/~masda/surf/more/grad.pdf))

[[!redirects projective spaces]]