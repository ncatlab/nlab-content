Let $C$ be a category, and $f: c \to d$ be a morphism. The **image** of $f$ is the smallest [[subobject]] $s \subseteq d$ through which $f$ factors (if it exists). There is a [[duality|dual]] notion of _co-image_: the largest [[quotient object|quotient]] of $c$ through which $f$ factors. 

Alternatively, let $C/d$ be the [[over category|slice category]] over $d$, and let $Mono(C)/d$ be the full subcategory whose objects are monos into $d$. Assuming images exist in $C$, taking the image of a map $f: c \to d$ provides a [[adjoint functor|left adjoint]] 

$$C/d \to Mono(C)/d$$ 

to the inclusion $Mono(C)/d \hookrightarrow C/d$. 

If $C$ admits equalizers, and if $i: k \to d$ represents the image of $f: c \to d$, then the unique map $q: c \to k$ such that $f = i q$ is an epimorphism. Thus, in a finitely complete category in which every morphism admits an image, one obtains in this way an epi-mono factorization, but the factorization may not have particularly good properties (in particular, the factorization through the image might not be stable with respect to pulling back). 

The notion of [[regular category]] formalizes a sense in which image factorizations do behave well: factorizations into a [[regular epimorphism]] followed by a mono which are stable under pullback. 
