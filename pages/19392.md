# Contents
* table of contents
{:toc}

## Idea

Call-by-push-value is a type theory and programming language which contains full embeddings of [[call-by-value]] and [[call-by-name]], including their operational semantics and equational theories.

Its semantics decomposes the semantics of effectful languages using a [[strong monad]] into a [[strong adjunction]]. Then the embeddings of call-by-value and call-by-name correspond to the construction of [[Kleisli category|Kleisli and co-Kleisli categories]] from an adjunction.

## Related

* The linear term judgment in [[linear-non-linear logic]] can be seen as extending the call-by-push-value stack judgment to allow for "multi-hole" stacks.

## References

* [[Paul-Blain Levy]], [_Call-by-Push-Value: A Subsuming Paradigm_, TLCA 1999](https://link.springer.com/chapter/10.1007/3-540-48959-2_17)

* [[Paul-Blain Levy]], [Adjunction Models for Call-by-push-value with Stacks_, CTCS 2003](https://www.cs.bham.ac.uk/~pbl/papers/ctcs02journal.pdf)