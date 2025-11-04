#Contents#
* table of contents
{:toc}

##Idea

In [[computer science]], **applicative functors** (also known as **idioms**) are the programming equivalent of [[lax monoidal functors]] with a [[tensorial strength]] in [[category theory]].

A [[strong monad]] gives rise to an applicative functor, but not all applicative functors result from monads. Unlike monads, applicative functors are closed under composition.

## Equivalence

An applicative functor $F$ in a [[closed monoidal category|closed (symmetric) monoidal category]]
$(\mathcal{C}, {\otimes}, I)$ is given by natural transformations
$\eta_x : x \to F(x)$ and $\phi_{x,y} : F([x, y]) \otimes F(x) \to F(y)$,
satisfying unit and associativity coherence.

```
class (Functor f) => Applicative f where
  pure  :: a -> f a
  (<*>) :: f (a -> b) -> f a -> f b
```

It defines a strong lax monoidal endofunctor as follows:

- $\epsilon = \eta_I : I \to F(I)$,
- $\mu_{x,y} : F(x) \otimes F(y) \xrightarrow{F(\Lambda(\mathrm{id}_{x \otimes y})) \otimes \mathrm{id}_{F(y)}} F([y, x \otimes y]) \otimes F(y) \xrightarrow{\phi_{y,x \otimes y}} F(x \otimes y)$
  where $\Lambda(\mathrm{id}_{x \otimes y}) : x \to [y, x \otimes y]$
  is the [[currying]] of the identity morphism on $x \otimes y$,
- $\mathrm{st}_{x,y} = \mu_{x,y} \circ (\eta_x \otimes \mathrm{id}_{F(y)})$.

Conversely, given such an endofunctor $(F, \epsilon, \mu, \mathrm{st})$,
one can consider the following applicative:

- $\eta_x : x \xrightarrow{\rho_x^{-1}} x \otimes I \xrightarrow{\mathrm{id}_x \otimes \epsilon} x \otimes F(I) \xrightarrow{\mathrm{st}_{x,I}} F(x \otimes I) \xrightarrow{F(\rho_x)} F(x)$,
  where $\rho_x : x \otimes I \to x$ is the right [[unitor]] for $\otimes$,
- $\phi_{x,y} = F(\mathrm{ev}_{x,y}) \circ \mu_{[x,y], x}$.

## Examples

There are two ways to define `List` as an applicative functor
within the category of data types.
In [[Haskell]], the first is the default implementation,
while the second is accessible via the `ZipList` newtype.
They can be presented as an instance of the `Applicative` type class,
or, equivalently, as an instance of the `Monoidal` type class.

```
instance Applicative List where
  pure x = [x]
  fs <*> xs = [ f x | f <- fs, x <- xs ]

instance Monoidal List where
  unit = [()]
  as ⊗ bs = [ (a, b) | a <- as, b <- bs ]
```

and

```
instance Applicative List where
  pure x = repeat x
  fs <*> xs = zipWith (\f x -> f x) fs xs

instance Monoidal List where
  unit = repeat ()
  as ⊗ bs = zip as bs
```

with the canonical strength being defined as follows:

```
strength :: Functor f => (a, f b) -> f (a, b)
strength (a, fb) = fmap (a,) fb
```


## Related concepts

* [[arrow (in computer science)]]

## References

* [[Conor McBride]], Ross Paterson: _Applicative programming with effects_, Journal of Functional Programming **18** 01 (2008) 1-13 &lbrack;[doi:10.1017/S0956796807006326](https://doi.org/10.1017/S0956796807006326); [author’s version](http://www.staff.city.ac.uk/~ross/papers/Applicative.html)&rbrack;

* Ross Paterson: _Constructing Applicative Functors_, in: *Mathematics of Program Construction, Madrid, 2012*, Lecture Notes in Computer Science **7342**, Springer, (2012) 300-323 &lbrack;[doi:10.1007/978-3-642-31113-0_15](https://doi.org/10.1007/978-3-642-31113-0_15), [webpage](http://www.staff.city.ac.uk/~ross/papers/Constructors.html)&rbrack;

[[!redirects applicative functors]]