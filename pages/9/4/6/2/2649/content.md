
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context###
#### Compact objects
+-- {: .hide}
[[!include compact object - contents]]
=--
=--
=--

# Contents
* automatic table of contents goes here
{:toc}

## Idea

A connected object is a generalisation of the concept of [[connected space]] from [[Top]] to an arbitrary [[category]].


## Definitions

Let $C$ be an [[extensive category]].

Then an [[object]] $X$ of $C$ is **connected** if the [[representable functor]]
$$ hom(X, -): C \to Set $$
preserves all [[coproducts]]. 

By this definition, the [[initial object]] of $C$ is *not* connected (except for degenerate cases of $C$); it is [[too simple to be simple]].  This matches the notion that the [[empty space]] should not be considered connected, discussed at [[connected space]].

(It\'s actually enough to require that it preserves *binary* coproducts, if $C$ is infinitary extensive.  By definition, $hom(X,-)$ preserves binary coproducts if the canonically defined map
$$ hom(X,Y) + hom(X,Z) \to hom(X,Y + Z) ,$$
is always a [[bijection]]. See the following section.) 

### Reduction to binary coproducts 

+-- {: .un_thm}
######Theorem 
Let $C$ be infinitary extensive. Then an object $X$ of $C$ is connected if and only if $\hom(X, -): C \to Set$ preserves binary coproducts. 
=-- 

+-- {: .proof}
######Proof 
The "only if" is clear, so we just prove the "if". 

We first show that $\hom(X, -)$ preserves the [[initial object]] $0$. Indeed, if $\hom(X, -)$ preserves the binary product $X + 0 = X$, then the canonical map $\hom(X, X) + \hom(X, 0) \to \hom(X, X)$  
is a bijection of sets, where the restriction to $\hom(X, X)$ is also a bijection of sets $id: \hom(X, X) \to \hom(X, X)$. This forces the set $\hom(X, 0)$ to be empty. 

Now let $\{Y_\alpha: \alpha \in A\}$ be a set of objects of $C$. We are required to show that each map 
$$f: X \to \sum_\alpha Y_\alpha$$ 
factors through a unique inclusion $i_\alpha: Y_\alpha \to \sum_\alpha Y_\alpha$. By infinite extensivity, each pullback $U_\alpha \coloneqq f^\ast (Y_\alpha)$ exists and the canonical map $\sum_\alpha U_\alpha \to X$ is an isomorphism. We will treat it as the identity. 

Now all we need is to prove the following. 

* Claim: $X = U_\alpha$ for exactly one $\alpha$. For the others, $U_\beta = 0$. 

Indeed, for each $\alpha$, the identity map factors through one of the two summands in 

$$id: X \to U_\alpha + \sum_{\beta \neq \alpha} U_\beta$$ 

because $\hom(X, -)$ preserves binary coproducts. In others words, either $X = U_\alpha$ or $X = \sum_{\beta \neq \alpha} U_\beta$ (and the other is $0$). We cannot have $U_\alpha = 0$ for every $\alpha$, for then $X = \sum_\alpha U_\alpha$ would be $0$, contradicting the fact that $\hom(X, 0) = 0$. So $X = U_\alpha$ for at least one $\alpha$. And no more than one $\alpha$, since we have $U_\alpha \cap U_\beta = 0$ whenever $\alpha \neq \beta$. 
=--

+-- {: .query}
[[Mike Shulman]]: It's not obvious to me that preserving binary coproducts is enough to ensure preservation of infinitary coproducts.  Unless you meant "preserves all finite coproducts"?

_Toby_:  I just copied what was at [[connected space]].  It\'s true that homming out of a connected space preserves all coproducts, but it\'s not clear to me whether that is a theorem at this level either.  Maybe we need to distinguish finitarily connected objects of finitarily extensive categories from infinitarily connected objects of infinitarily extensive categories?
=--


## Examples

* Connected objects in [[Top]] are precisely [[connected topological space]]s. 

* For a [[group]] $G$, connected objects in the category $G Set$ of [[permutation representation]]s are precisely the ([[inhabited set|inhabited]]) transitive $G$-sets. 

* Objects in a [[locally connected topos]] such as $G$-$Set$ are [[coproduct]]s of connected objects. 


## Related concepts

* [[n-connected object in an (∞,1)-topos]]



[[!redirects connected object]]
[[!redirects connected objects]]

[[!redirects connected]]
