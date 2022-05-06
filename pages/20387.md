
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Trigonometry
+-- {: .hide}
[[!include trigonometry -- contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

An inverse trigonometric function is a [[right inverse]] to one of the six standard [[trigonometric functions]], or more precisely a [[continuous function|continuous]] right inverse to the [[epimorphism]] part of the [[(epi, mono) factorization]] of a trigonometric function. 

Inverse functions are often named using the prefix "arc", so that for example "[[arcsine]]" is another name for the inverse [[sine]]. This naming arises because the values of an inverse trigonometric function are considered as [[arc lengths]], just as trigonometric functions themselves are defined in terms of arc length parametrizations. Another possible reason for using the *arc-* prefix is to avoid a notational confusion, where for example $\cos^{-1}$ might easily be confused with the [[reciprocal]] of the [[cosine]] function, inasmuch as the notation $\cos^n$ is commonly used to denote an $n^{th}$ power of the cosine. 

Since many such right inverses are possible, the choice of right inverse is a matter or convention. For the [[arcsine]] and [[arctangent]], the choice is dictated by having $0$ as a [[fixed point]]. This leads to convenient [[power series]] representations in [[neighborhoods]] of the origin, for example 

$$\arctan(x) = x - \frac{x^3}{3} + \frac{x^5}{5} - \ldots$$ 

For other inverse trigonometric functions, the choice is dictated by convenient formulas such as 

$$\arccos(x) = \frac{\pi}{2} - \arcsin(x), \qquad \arccot(x) = \frac{\pi}{2} - \arctan(x)$$ 

while we also have 

$$\arcsec(x) = \arccos(\frac1{x}), \qquad \arccsc(x) = \arcsin(\frac1{x}).$$ 

## Example

* [[arccos]]

* [[arcsin]]

* [[arctan]]


[[!redirects inverse trigonometric functions]]
