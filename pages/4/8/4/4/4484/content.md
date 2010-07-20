
## Idea

For a category $C$ with a single isomorphism class of objects, and a given object $a$, one can ask (assuming Choice) for a map $\lambda:Obj(C) \to Mor(C)$ which picks out an isomorphism $\lambda_b:a \to b$ for all other objects $b$ of $C$. This is essentially a section of the restriction of the target map $t:s^{-1}(a) \to Obj(C)$. 

For an [[internal category]], this is not always possible. But if one has a notion of local sections, such as given by a Grothendieck pretopology, say, then we can ask when this can be done locally. Indeed, one can relax the condition on the isomorphism classes, and look at finding sections for each isomorphism class. 

In the case of topological categories (perhaps only groupoids), the existence of such local sections forces the space of isomorphism classes to be discrete.


## Definition

Let $(S,J)$ be a concrete [[site]] with [[pretopology]] $J$.

> Copy details below to here, rewriting for arbitrary concrete site.

## Special case of topological groupoids


For a topological (resp. Lie) category $X$, let $X_1^{iso}$ denote the subspace (resp. submanifold) of invertible arrows . (This always exists, by general abstract nonsense - I should look up the reference, it's in Bunge-Pare I think - [[David Roberts|DR]])

+-- {: .un_defn}
###### Definition 
A topological groupoid $X_1 \rightrightarrows X_0$ is **locally trivial** if for every point $p\in X_0$ there is a neighbourhood $U$ of $p$ and a lift of the inclusion $\{p\} \times U \hookrightarrow X_0 \times X_0$ through $(s,t):X_1^{iso}\to X_0 \times X_0$. 
=--

Clearly for a Lie groupoid $X_1^{iso} = X_1$. It is simple to show from the definition that for a transitive Lie groupoid, $(s,t)$ has local sections. Ehresmann goes on to show a link between smooth [[principal bundles]] and transitive, locally trivial Lie groupoids.

>Details of this...

## Alternate characterisations

A locally discrete topological groupoid is weakly equivalent (as in chapter 1 of [[Fundamental Bigroupoids and 2-Covering Spaces]] to one with a discrete space of objects. There is in fact a canonical such space, the discrete space on the underlying set of the given space of objects.

> To be expanded...
