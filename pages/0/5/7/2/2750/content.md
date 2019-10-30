
# Ordered pairs
* table of contents
{: toc}

## Idea

Given any things $a$ and $b$, the __ordered pair__ of $a$ and $b$ is a thing, usually written $(a,b)$, sometimes $[a,b]$ or $\langle{a,b}\rangle$.  The important property is
\[ \label{basic} (a,b) = (c,d) \;\Leftrightarrow\; a = c,\; b = d .\]
The things $a$ and $b$ are called the __components__ of the ordered pair $(a,b)$.  Given any two sets $X$ and $Y$, their [[Cartesian product]] is a set $X \times Y$ whose [[elements]] are precisely the ordered pairs whose components are respectively elements of $X$ and elements of $Y$.

Note that nothing is __ordered__ in an ordered pair other than how it is written out, so sometimes just the word __pair__ is used for this concept. 

In terms of [[category theory]] an ordered pair is an element in a [[Cartesian product]].

The concept of  "pair" meaning a set containing just one or two members as in the [[axiom of pairing]] of [[ZFC|Zermelo–Frankel Set Theory]] is now usually distinguished as an __[[unordered pair]]__. A pair in which the components are ordered is basically an arrow between the components, which is sometimes called or analyzed as an [[interval object|interval]] within a larger context.


## Formalisations

One may wish to declare ordered pairs to exist by fiat, which was done, for example, by both [[Bourbaki]] and [[Bill Lawvere]].  In Bourbaki\'s foundational [[set theory]], $\langle{-,-}\rangle$ is a fundamental binary operation on mathematical objects satisfying two axioms: \eqref{basic} and the existence (as a set) of the Cartesian product of any two sets.  In Lawvere\'s foundational set theory, [[ETCS]], one axiom is the existence of [[products]] in the category of sets; when applied to [[global elements]], this gives their ordered pair (with the product itself being the Cartesian product), and \eqref{basic} can be proved.  Other [[structural set theories]] should contain an axiom similar to Lawvere\'s axiom of products.

+-- {: .query}
I need to check that I remembered Bourbaki correctly; it varies with the edition.  ---Toby
=--

Instead, one may construct ordered pairs out of some more basic operation.  In a [[material set theory]], one may use _[[Kuratowski pairs]]_

$$ (a,b) \coloneqq \big\{\,\{a\},\{a,b\}\,\big\} ;$$

it is straightforward (using the [[axiom of extensionality]]) to prove that \eqref{basic} holds.  Sometimes one sees the alternative
$$ (a,b) \coloneqq \big\{a, \{a,b\}\,\big\} ;$$
but now the [[axiom of foundation]] is also needed to prove \eqref{basic}, so the first form is usually preferred.  To prove that the cartesian product of two sets is a set, one may use the axiom of separation ([[bounded separation]] is enough) to construct $X \times Y$ as a [[subset]] of the [[power set]] of the power set of the [[union]] of $X$ and $Y$, or else use the axiom of replacement ([[restricted replacement]] is enough) to construct it directly, since its elements are indexed by the sets $X$ and $Y$. 

+-- {: .num_remark #class} 
###### Remark 
Again in the context of material set theory, there are other options for defining ordered pairs that may offer technical advantages. For example, assuming we have the natural numbers $\mathbb{N}$, and given a set $x$, let $\varphi(x)$ be the set $(x \setminus \mathbb{N}) \cup \{n+1: n \in x \cap \mathbb{N}\}$. Then define 

$$(A, B) \coloneqq \{\varphi(a): a \in A\} \cup \{\varphi(b) \cup \{0\}: b \in B\}$$ 

and observe that the first entry $A$ may be retrieved as the set of elements of $(A, B)$ that do not contain $0$, and $B$ as the set of elements that do. One advantage is that even for classes $A, B$ (defined in ZFC as formulas), we may define a class $(A, B)$ as another formula patterned on this construction. This solves a technical exercise posed by Andrej Bauer in this [MO post](https://mathoverflow.net/a/63268/2926); compare [class functions](https://ncatlab.org/nlab/show/function#for_classes). Thus, a function between classes $f: A \to B$ may be defined as an ordered triple $(A, f, B)$ where $f$ is a class of pairs $(a, b)$ defined by a formula that is [[entire relation|entire]] and [[functional relation|functional]]. 
=-- 

In a foundational [[type theory]], ordered pairs are usually also given by fiat, but \eqref{basic} may not hold, depending on the type theory used.  Now Bourbaki\'s binary operation of pairing becomes a typed operation; given $a$ of type $X$ and $b$ of type $Y$, the ordered pair $(x,y)$ has type $A \times B$.  There are also two typed operations (either basic or definable, depending on the style of type theory used) $\pi\colon X \times Y \to X$ and $\rho\colon X \times Y \to Y$, satisfying the [[beta-rule]]s $\pi(x,y) = x$ and $\rho(x,y) = y$.  Then we can either add the [[eta-rule]] $z = (\pi z,\rho z)$, which will allow \eqref{basic} to be proved; or else take \eqref{basic} as the *definition* of equality on the product type $X \times Y$, which will then allow the eta-rule to be proved.  (Or you can do neither, and then \eqref{basic} and the eta-rule will fail.)


## Generalisations

* [[tuples]]

* [[families]]

* [[pairings]]

* [[dependent sums]]


[[!redirects ordered pair]]
[[!redirects ordered pairs]]
