## Idea

An idempotent semifield is an [[idempotent semiring]] that has a zero and in which every non-zero element is invertible. Or, in other words, a [[skewfield]] in which an element may not have a negative but is always idempotent with respect to addition.

## Definition

An __idempotent semifield__ $K$ is [[idempotent semiring]] that has a zero $0$ and in which for every non-zero element $x$ there is an element $y$ such that $x \cdot y = 1$. It is said to be __commutative__ if the multiplication is [[commutative magma|commutative]].

## Properties as a lattice

As in the case of an [[idempotent semiring#Properties|idempotent semiring]] there is a partial order given by

$$ x \leq y \;\;{:\!\!\Longleftrightarrow}\;\; x + y = y $$

which has a [[join]] given by addition. In case of an idempotent semifield this partial order also has a [[meet]]. To each semifield there is a dual semifield $K^*$ given on the same set of elements as $K$ and with the same zero, identity, and multiplication but with addition given by interchanging join and meet, i.e. the meet becomes the new addition on non-zero elements and the zero element behaves neutral.

## Equations in semifields

A version of the fundamental theorem of algebra can be formulated for semifields:
A semifield is said to be __algebraically closed__ if the equation $x^n = y$ has a solution for all $x\in K$ and $n=1,2,\ldots$.

+-- {: .num_theorem #fundamentalThm}
###### Theorem

In an algebraically closed commutative idempotent semifield $ K $ with $ 0 \cdot a = 0 $ for all $ a \in K $ the equation
$$
  p_0 + p_1 \cdot x^1 + p_2 \cdot x^2 + \ldots + p_n x^n = y
$$

with $y,p_0, \ldots, p_n \in K$ and $n=1,2,\ldots$ has a solution in $K$ if and only if $y \geq p_0$. If $p_0 = 0$, then the solution is unique and can be expressed in terms of the coefficients with help of [[radical|radicals]], multiplication, inverse and meet (i.e. a polynomial in the radicals of $y, p_0, \ldots, p_n$ over the dual semifield).

=--

## Examples

* The [[max-plus algebra]] $[-\infty, +\infty)$ with addition given by maximum and multiplication given by ordinary addition.

* The two element semifield $ \{ 0, 1 \} $ with $ 0 \leq 1 $
 and $ + = \cdot = \vee $ is commutative and algebraically closed but does not fulfill the assumptions of theorem \ref{fundamentalThm}. Indeed, the equation $ 1 \cdot x = 1 $ does not have a unique solution.

## Related concepts

* [[rig]]

* [[rng]] ([[nonunital ring]])

* [[ring]], [[near-ring]]

* [[tropical geometry]]

* [[tropical semiring]]

* [[idempotent semiring]]

## References

In the reference the assumption that $0 \cdot a = 0$ is not explicit (otherwise the base step in the induction in the proof of Proposition 2 therein doesn't work).

* Shpiz, _Solution of algebraic equations in idempotent semifields_, Communications of the Moscow Mathematical Society (1960), [russian](http://www.mathnet.ru/php/archive.phtml?wshow=paper&jrnid=rm&paperid=331&option_lang=eng) [english](https://iopscience.iop.org/article/10.1070/RM2000v055n05ABEH000331/meta)