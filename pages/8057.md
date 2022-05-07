
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

# Fixed-point combinators
* table of contents
{: toc}

## Idea 

In [[combinatory logic]], in the [[lambda-calculus|$\lambda$-calculus]], or more generally in [[type theory]], a _fixed-point [[combinator]]_ is a [[term]] $Y$ which, when [[function application|applied]] to a term $n$, yields a term $Y n$ that is a fixed-point of $n$:
$$ n (Y n) = Y n .$$
This equality is usually a directed [[beta-reduction]] as follows:
$$ Y n \to_\beta n (Y n) .$$


## Implementing general recursion

When "programming" in any of these systems, a fixed-point combinator serves as a mechanism for implementing general [[recursion]].  When writing a 
[[recursive function]] in a standard [[programming language]], such as the [[factorial]]

    def fact(n:nat) : nat = {
      if (n == 0) {
        return 1
      } else {
        return n * fact(n-1)
      }
    }

one generally calls the function being defined inside of its own body.  This is not possible for a combinator or a lambda-term to do directly, but it can be implemented using a fixed-point combinator.  One first defines a "generator" which takes "the function to call recursively" as an additional argument:

    def genfact(f : nat -> nat)(n:nat) : nat = {
      if (n == 0) {
        return 1
      } else {
        return n * f(n-1)
      }
    }

and then "closes the loop" by applying the fixed-point combinator.  That is, we [[currying|curry]] `genfact` to view it as an [[endofunction]] of `nat -> nat` (an [[operator]]) and then construct its fixed point, 

$$ fact = Y(genfact). $$

The directed $\beta$-reduction version of the fixed-point property of $Y$ then implements the process of calling a function recursively:

$$
\begin{aligned}
  fact(3) &= Y(genfact)(3)\\
  &\to_\beta genfact(Y(genfact))(3)\\
  &\to_\beta 3 * Y(genfact)(2)\\
  &\to_\beta 3 * genfact(Y(genfact))(2)\\
  &\to_\beta 3 * 2 * Y(genfact)(1)\\
  &\to_\beta 3 * 2 * genfact(Y(genfact))(1)\\
  &\to_\beta 3 * 2 * 1 * Y(genfact)(0)\\
  &\to_\beta 3 * 2 * 1 * genfact(Y(genfact))(0)\\
  &\to_\beta 3 * 2 * 1 * 1\\
  &= 6
\end{aligned}
$$

In particular, observe that because general recursion allows the definition of nonterminating functions, so does a fixed-point combinator.  An obvious example is the fixed point of the identity function $I$, which reduces as follows:

$$ Y I \to_\beta I(Y I) \to_\beta Y I \to_\beta I(Y I) \to_\beta Y I \to_\beta \cdots  $$


## Existence

There are many ways of constructing or otherwise obtaining a fixed-point combinator, varying with the formal system in which one works.

### Unityped $\lambda$-calculus

In the unityped [[lambda-calculus|$\lambda$-calculus]], a traditional construction (due to Curry) is

$$ Y = \lambda n. (\lambda s. n (s s)) (\lambda s. n (s s)) $$ 

For a given term $n$, put $t = \lambda s. n (s s)$. We then have $Y n = t t$, and we also have 

$$ \array {
Y n & = & (\lambda s. n (s s)) (\lambda s. n (s s)) \\
 & = & (\lambda s. n (s s)) (t) \\ 
 & = & n (t t) \\ 
 & = & n (Y n)
}$$ 

so that $Y n$ is a fixed point of $n$. Compare [[Lawvere fixed point theorem|Lawvere's proof]] of [[Cantor's theorem]]. 

Another construction is due to ([Klop 07](#Klop07)):

$$Y_K = L L L L L L L L L L L L L L L L L L L L L L L L L L$$

where 

$$L = \lambda a b c d e f g h i j k l m n o p q s t u v w x y z r. r (t  h i s i s a f i x e d p o i n t c o m b i n a t o r)$$

Note that $Y_K$ is $L$ repeated 26 times, and the string
$thisisafixedpointcombinator$ contains 27 characters. Thus 

$$\array { 
Y_K n & = & (\lambda r. r(L L L L L L L L L L L L L L L L L L L L L L L L L L r)) n \\
      & = & (\lambda r. r(Y_K r)) n \\ 
      & = & n (Y_K n)
}$$

### Combinatory logic

In [[combinatory logic]] (based on the combinators $S$, $K$, and $I$), one construction is  


$$
  S(K(S I I)) 
  \big(
    S(S(K S)K)(K(S I I))
  \big) 
$$ 

following the standard formulas $S x y z = (x z)(y z)$, $K x y = x$ and $I x = x$, and where bracketings left unspecified are by convention to the left. For a derivation of this, see the article on [combinatory algebra](http://ncatlab.org/nlab/show/partial+combinatory+algebra#ExamplesOfCombinators). 

### Typed $\lambda$-calculus

In many forms of (multi-) *typed* $\lambda$-calculus (and more general type theory), a fixed-point combinator cannot be constructed, because there is no type whose terms can be applied to themselves.  This is usually intentional, because it avoids the nontermination inherent in the existence of a fixed-point combinator.

However, it is possible to add a fixed-point combinator to typed $\lambda$-calculus by fiat, obtaining a typed system which includes general recursion and hence nontermination.  This is appropriate for some forms of [[domain semantics]], and for modeling some real-world programming languages ([[Haskell]] is a notable example).

## Related pages

* [[Löb's theorem]]

* [[Lawvere fixed point theorem]]

* [[looping combinator]]

## References

* {#Klop07} Jan Willem Klop, _[New Fixed Point Combinators from Old](http://www.cs.ru.nl/barendregt60/essays/klop/)_, in  	
_Reflections on Type Theory, Lambda Calculus, and the Mind: Essays Dedicated to Henk Barendregt on the Occasion of his 60th Birthday_

[[!redirects fixed-point combinator]]
[[!redirects fixed-point combinators]]


