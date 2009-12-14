* toc
{:toc}

# Idea

**Dinatural transformations** are a generalization of ordinary *natural transformations* and also of *extranatural transformations*.  The differences can be summarized thusly:

* In an ordinary [[natural transformation]] $F\to G$, both $F$ and $G$ involved depend on some variable $x$ with the same variance (covariant or contravariant).
* In an [[extranatural transformation]] $F\to G$, either $F$ depends on $x$ both covariantly *and* contravariantly and $G$ does not depend on $x$ at all, or vice versa.
* In a **dinatural transformation** $F\to G$, both $F$ and $G$ can depend on $x$ both covariantly and contravariantly.

If the dependence of $F$ or $G$ on $x$ in a dinatural transformation is trivial, it reduces to an extranatural one.  Similarly, if the contravariant (or, dually, the covariant) dependence of $F$ and $G$ on $x$ are trivial, it reduces to an ordinary natural one.

Arguably, most dinatural transformations which arise in practice are extranatural.


# Formalization

Let $F, G: C^{op} \times C \to D$ be functors. A __dinatural transformation__ from $F$ to $G$, sometimes written 

$$\alpha: F \stackrel{\bullet}{\to} G,$$ 

consists of a collection of morphisms 

$$\alpha_{c}: F(c, c) \to G(c, c)$$ 

such that for every morphism $f: c \to c'$ in $C$, 

$$G(c, f)\alpha_c F(f, c) = G(f, c')\alpha_{c'}F(c', f): F(c', c) \to G(c, c') \qquad (3)$$ 

This "hexagon identity" gives the "domain" version of extranaturality when $G$ is constant, and the "codomain" version when $F$ is constant. The domain version involves a commutative square of the form 

$$\alpha_c F(f, c) = \alpha_{c'} F(c', f): F(c', c) \to G \qquad (4)$$

where $G$ is constant with respect to the argument $c$, and the codomain version a commutative square of the form 

$$G(c, f) \alpha_c = G(f, c')\alpha_{c'}: F \to G(c, c') \qquad (5)$$

when $F$ is constant with respect to the argument $c$. 

# Dinaturality versus extranaturality

Many people who encounter the notion of dinaturality through the general definition (as in equation (3)) have subsequent difficulty grokking it.  It is the opinion of at least one author of this article ([[Todd Trimble]]), and it was certainly the opinion of Max Kelly, that this "efficient" definition is not the most useful or intuitive one.  Rather, one may be better off grokking the separate squares (4) and (5) -- that is, the notion of [[extranaturality]] -- and how they arise in practice. 

One could try to argue against that by pointing to dinatural transformations which do not reduce to extranatural ones. Here perhaps the most well known example is where $F = \hom: Set^{op} \times Set \to Set$, where we have a class of dinatural transformations

$$\hom(x, x) \stackrel{\alpha_n}{\to} \hom(x, x)$$ 

defined by the rule $alpha_n(f) = f^{(n)}$ ("Church numerals"). But these examples can be "bent" into domain extranaturality by defining 

$$Set^{op} \times Set \stackrel{G}{\to} Set: (x, y) \mapsto \hom(x, y)^{\hom(y, x)}$$ 

and considering extranatural transformations from the constant $1$ (the terminal set) to $G$. Such tricks support the counterargument that the extra generality of the traditional definition is largely spurious, and not particularly helpful in terms of comprehension.

# References

Here is a blog post inspired by the above discussion:

* Dan Piponi, [Dinatural transformations and coends](http://blog.sigfpe.com/2009/03/dinatural-transformations-and-coends.html).

It discusses these concepts in the context of the programming language Haskell.
