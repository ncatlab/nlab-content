
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include algebra - contents]]
=--
#### Higher algebra
+-- {: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


# The characteristic of a field (etc)
* table of contents
{: toc}

## Idea

It is well known that you cannot divide by [[zero]], lest you be doomed to [[trivial ring|triviality]].  Conversely, in a [[field]], you *can* divide by anything *except* zero.  But this rule can be misleading, since it\'s possible that (even) an ordinary number can be zero when you don\'t expect it!  The _characteristic_ of a field states when (if ever) this happens.

It is straightforward to generalise from fields to other [[rings]], and even [[rigs]]. See also [[characteristic zero]].

## Definition

### For rings

Let $K$ be a [[rig]] (possibly a [[ring]], possibly a [[commutative ring]], possibly even a [[field]]).  Then there exists a unique [[homomorphism]] $\phi_K\colon \mathbb{N} \to K$ to $K$ from the [[initial object|initial]] rig, which is the rig $\mathbb{N}$ of [[natural numbers]].  The [[kernel]] of $\phi_K$ is an [[ideal]] of $\mathbb{N}$, which (by a well-known property of $\mathbb{N}$) is a [[principal ideal]] with a unique generator.  This generator is the __characteristic__ of $K$, denoted $\char K$.

If $K$ is a ring, then we may use $\phi_K\colon \mathbb{Z} \to K$ instead, where $\mathbb{Z}$ is the ring of [[integers]].  However, in this case, the kernel will usually have two generators, in which case we pick the positive one to get the same result as above.

### For $E_\infty$-rings

The concept of the characteristic has been generalized to [[E-∞ rings]] ([Szymik 12](#Szymik12), [Szymik 13](#Szymik13), [Baker 14](#Baker14)).



## Properties

If $n$ is a [[natural number]], then we suppress mention of $\phi_K$ to think of $n$ as an element of $K$.  If $K$ is a ring, then we do the same for a negative [[integer]] $n$.  We then have that $n = 0$ in $K$ if and only if $n$ is a multiple of $\char K$.

The characteristic of a field must be either [[zero]] or a [[prime number]]. Basically, this is because the kernel of $\phi_K$, for $K$ a field, must be a [[prime ideal]]. Similarly, the characteristic of an [[integral domain]] must be either zero or a prime number. 

Every rig with positive characteristic is in fact a ring, since we have $\char K - 1 = -1$.  In other words, any rig other than a ring must have characteristic zero (although many rings also have that characteristic).

If there is any [[homomorphism]] at all between two fields, then they have the same characterstic. In other words, any [[field extension|extension]] of a field keeps the same characteristic. 

## Examples

If $n$ is a positive natural number, then the characteristic of $\mathbb{N}/n = \mathbb{Z}/n$ is $n$.  This ring is always a [[commutative ring]], and it is a [[field]] if and only if $n$ is prime, in which case it is the [[prime field]] $\mathbb{F}_n$.  More generally, every [[finite field]] has positive prime characteristic.

For $n = 0$, $\mathbb{N}/0 = \mathbb{N}$, $\mathbb{Z}/0 = \mathbb{Z}$, and the prime field $\mathbb{F}_0 = \mathbb{Q}$ (the field of [[rational numbers]]) are no longer all the same, but they still all have characteristic $0$.  Every [[ordered field]] has characteristic $0$.  The [[real numbers]] and [[complex numbers]] each form fields of characteristic $0$.




## Related concepts

* [[freshman's dream]]

* [[characteristic zero]], [[positive characteristic]]

## References

Discussion for [[E-∞ rings]]:

* {#Szymik12} [[Markus Szymik]], _Commutative S-algebras of prime characteristics and applications to unoriented bordism_ ([arXiv:1211.3239](http://arxiv.org/abs/1211.3239))

* {#Szymik13} [[Markus Szymik]],  _String bordism and chromatic characteristics_ ([arXiv:1312.4658](http://arxiv.org/abs/1312.4658))

* {#Baker14} [[Andrew Baker]], _Characteristics for $E_\infty$ ring spectra_ ([arXiv:1405.3695](http://arxiv.org/abs/1405.3695))


[[!redirects characteristic]]
[[!redirects characteristics]]
[[!redirects characteristic of a field]]
[[!redirects characteristics of fields]]
[[!redirects characteristic of a ring]]
[[!redirects characteristics of rings]]
[[!redirects characteristic of a rig]]
[[!redirects characteristics of rigs]]