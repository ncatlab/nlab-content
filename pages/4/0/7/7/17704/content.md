#Contents#
* table of contents
{:toc}

##Idea

In [[computer science]], **applicative functors** (also known as **idioms**) are the programming equivalent of [[lax monoidal functors]] with a [[tensorial strength]] in category theory.

A [[strong monad]] gives rise to an applicative functor, but not all applicative functors result from monads. Unlike monads, applicative functors are closed under composition.

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
  fs <*> xs = zipWith ($) fs xs

instance Monoidal List where
  unit = repeat ()
  as ⊗ bs = zip as bs
```

with the canonical strength being defined as follows:

```
strength :: Functor f => (a, f b) -> f (a, b)
strength (a, fb) = fmap (a,) fb
```

##Related concepts

* [[arrow (in computer science)]]

##References

* Conor Mcbride, Ross Paterson, _Applicative programming with effects_, Journal of Functional Programming. 18 (01): 1&#8211;13. ([doi:10.1017/S0956796807006326](https://doi.org/10.1017/S0956796807006326); [author’s version](http://www.staff.city.ac.uk/~ross/papers/Applicative.html))

* Ross Paterson, _Constructing Applicative Functors_, in Mathematics of Program Construction, Madrid, 2012, Lecture Notes in Computer Science vol. 7342, pp. 300-323, Springer, 2012. ([paper](http://www.staff.city.ac.uk/~ross/papers/Constructors.html))

[[!redirects applicative functors]]