## Rough Idea: 

Dinatural transformations are what you get when you "bend the rules" for natural transformations. Perhaps the most intuitive approach to them is through string diagrams: every time you bend a string (that represents a component of a natural transformation) into a U-shape or upside-down U-shape, the U-shape represents a component of a dinatural transformation. Thus, the rules for dinatural transformations mirror rules for ordinary transformations, except they are bent into shapes with a covariant part and a contravariant part. (Cf. interactions between particles and their corresponding antiparticles.) 

The best approach is to consider a calculus that studies natural transformations and dinatural transformations together and how they compose. An _extranatural transformation_ is a mixture of both, and the calculus of extranatural transformations is a very simple, perhaps the most basic string diagram calculus. It was first introduced by Eilenberg, Kelly, and Mac Lane in the mid 60's. 

## Examples

Consider the hom-functor $\hom: Set^{op} \times Set \to Set$ (or more generally, the internal hom-functor $\hom: V^{op} \times V \to V$ where $V$ is symmetric monoidal closed). The identity transformation $1: \hom \to \hom$ has components of the form 

$$1_{x, y}: x^y \to x^y$$ 

and this of course is natural in each of the separate arguments $x, y$. String diagrammatically, this naturality would be represented by placing the domain over the codomain and linking the two instances of $x$ with a straight line and the two instances of $y$ with a straight line. Although it's trivial, let's at least record what naturality in say $y$ would mean: it means that for any morphism $g: y \to y'$ we have an equation of the form 

$$1_{x, y} x^g = x^g 1_{x, y'}: x^{y'} \to x^y \qquad (1)$$

Now, the adjunction between (tensor) product and hom allow us to "bend" the transformation into another: 

$$eval_{x, y}: x^y \otimes y \to x$$ 

in which the two instances of $y$ are linked by a U-shape. This gives a transformation which is natural in $x$ but not of course in $y$; rather, in $y$ we have an equation which is companion to (1): 

$$eval_{x, y} (x^g \otimes y) = eval_{x, y'} (x^{y'} \otimes g): x^{y'} \otimes y \to x \qquad (2)$$ 

and we say in this case that $eval_{x, y}$ is _dinatural_ in $y$. Notice how the dinatural variable $y$ in $eval_{x, y}$ appears once covariantly [in the tensor factor] and once contravariantly [in the exponent], but together on the same side of the arrow [here the domain]. (There is a nice string diagram picture for (2) which the reader might like to draw at this point.) 

Thus the transformation $eval_{x, y}$ involves a mixture of naturality and dinaturality; we say it is _extranatural_. 

* The late Max Kelly was fond of saying that really it's all the same basic concept: why proliferate terminology needlessly? Therefore he would simply say $eval$ was "natural" in both arguments. 

The basic idea should now be clear, but let's give a few more examples. Starting with the identity transformation 

$$1_{x, y}: x \otimes y \to x \otimes y$$ 

we can again bend it using the tensor-hom adjunction to form an arrow 

$$coeval_{x, y}: x \to (x \otimes y)^y$$ 

where again $y$ appears once covariantly and once contravariantly, this time on the codomain side. The dinaturality in $y$ is the condition 

$$(x \otimes g)^{y} coeval_{x, y} = (x \otimes y')^g coeval_{x, y'}$$

for every arrow $g: y \to y'$. 

As these examples indicate, instances of naturality are typically transferred into instances of dinaturality by means of adjunctions. Indeed, basic instances of U-shapes or upside-down U-shapes in string diagrams come about through counits and units of adjunctions, 

$$\varepsilon: F U \to 1 \qquad \eta: 1 \to U F$$

## Formalization 

As we have seen, dinaturality can occur either on the domain or the codomain side. We could treat these cases separately, but the traditional definition treats both cases simultaneously as follows: 

Let $F, G: C^{op} \times C \to D$ be functors. A _dinatural transformation_ from $F$ to $G$, sometimes written 

$$\alpha: F \stackrel{\bullet}{\to} G,$$ 

consists of a collection of morphisms 

$$\alpha_{c}: F(c, c) \to G(c, c)$$ 

such that for every morphism $f: c \to c'$ in $C$, 

$$G(c, f)\alpha_c F(f, c) = G(f, c')\alpha_{c'}F(c', f): F(c', c) \to G(c, c') \qquad (3)$$ 

This "hexagon identity" gives the "domain" version of dinaturality when $G$ is constant, and the "codomain" version when $F$ is constant. The domain version involves a commutative square of the form 

$$\alpha_c F(f, c) = alpha_{c'} F(c', f): F(c', c) \to G \qquad (4)$$

where $G$ is constant with respect to the argument $c$, and the codomain version a commutative square of the form 

$$G(c, f) \alpha_c = G(f, c')\alpha_{c'}: F \to G(c, c') \qquad (5)$$

when $F$ is constant with respect to the argument $c$. 

## Commentary

Many people who encounter the notion of dinaturality through the general definition (as in equation (3)) have subsequent difficulty grokking it. It is the opinion of at least one author of this article ([[Todd Trimble]]), and it was certainly the opinion of Max Kelly, that this "efficient" definition is not the most useful or intuitive one -- that one may be better off grokking the separate squares (4) and (5) and how they arise in practice. 

One could try to argue against that by pointing to dinatural transformations which do not reduce to the "domain" or "codomain" form. Here perhaps the most well known example is where $F = \hom: Set^{op} \times Set \to Set$, where we have a class of dinatural transformations 

$$\hom(x, x) \stackrel{\alpha_n}{\to} \hom(x, x)$$ 

defined by the rule $alpha_n(f) = f^{(n)}$ ("Church numerals"). But these examples can be "bent" into a codomain form of dinaturality by defining 

$$Set^{op} \times Set \stackrel{G}{\to} Set: (x, y) \mapsto \hom(x, y)^{\hom(y, x)}$$ 

and considering dinatural transformations from the constant $1$ (the terminal set) to $G$. Such tricks support the counterargument that the extra generality of the traditional definition is largely spurious, and not particularly helpful in terms of comprehension. 

## Extranatural calculus

We set down a few basic lemmas which describe how extranatural transformations compose. These lemmas become very intuitive once one draws string diagrams to accompany them. (Cf. "yanking moves" in the string diagram calculus of adjunctions.) 

Lemma 1 ("stalactites"): Let $F, G$ be functors of the form $C^{op} \times C \to D$. If $\alpha_{x, y}: F(x, y) \to G(x, y)$ is natural in $x, y$ and $\beta_x: G(x, x) \to H$ is dinatural in $x$ (for some object $H$ of $D$), then 

$$\beta_x \alpha_{x, x}: F(x, x) \to H$$ 

is dinatural in $x$. 

Lemma 2 ("stalagmites"): Let $G, H$ be functors of the form $C^{op} \times C \to D$. If $\alpha_x: F \to G(x, x)$ is dinatural in $x$ (for some object $F$ of $D$) and $\beta_{x, y}: G(x, y) \to H(x, y)$ is natural in $x, y$, then 

$$\beta_{x, x} \alpha_x: F \to H(x, x)$$ 

is dinatural in $x$. 

Lemma 3 ("yanking"): Let $F, H$ be functors of the form $C \to D$, and let $G: C \times C^{op} \times C \to D$ be a functor. If $\alpha_{x, y}: F(y) \to G(x, x, y)$ is natural in $y$ and dinatural in $x$, and if $\beta_{x, y}: G(x, y, y) \to H(x)$ is natural in $x$ and dinatural in $y$, then 

$$\beta_{x, x} \alpha_{x, x}: F(x) \to H(x)$$ 

is natural in $x$. 
