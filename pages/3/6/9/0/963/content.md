A **quantale** is a [[closed monoidal category|closed monoidal]] [[suplattice]].  This means it is a poset having all [[join]]s and an associative, unital tensor product $\otimes$ which distributes over joins (the internal-homs then come automatically by the [[adjoint functor theorem]]).  The internal-homs in a quantale are sometimes called _residuations_ and written $x\backslash y$ and $y/x$.

Additional conditions often imposed on a quantale include:

* Commutativity: $x\otimes y = y\otimes x$
* Idempotence: $x\otimes x = x$
* The unit for $\otimes$ is the top element: $1=\top$.

If all three of commutativity, idempotence, and $1=\top$ are assumed, they force $\otimes$ to be the [[meet]] and therefore the quantale to be a [[frame]].  General quantales are sometimes considered to be a "noncommutative" version of a frame, whose [[opposite category]] would be a category of "noncommutative [[locale]]s" (hence the name, a [portmanteau](
http://en.wikipedia.org/wiki/Portmanteau) of "quantum" and "locale").

+--{: .query}
Now, if you really thought of quantales as quantum locales, then you would define a morphism of quantales to go backwards.  What does the literature say about that?  ---Toby

[[Mike Shulman|Mike]]: I think that whatever the origins of the name, quantales are generally treated in the literature as more like "quantum frames" than "quantum locales."  Note, though, that in the past, it was common to use the word "locale" for what we now call a "frame" and simply distinguish between "locale homomorphisms" and "continuous maps."

_Toby_:  That explains it then, thanks.
=--
