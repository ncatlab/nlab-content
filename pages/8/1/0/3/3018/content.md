* toc
{: toc}

# Idea

**Extraordinary natural transformations**, or **extranatural transformations**, are what you get when you "bend the rules" for natural transformations.  One intuitive approach to them is through [[string diagrams]]: every time you bend a string (that represents a component of a natural transformation) into a U-shape or upside-down U-shape, the U-shape represents a component of an extranatural transformation.  Thus, the rules for extranatural transformations mirror rules for ordinary [[natural transformations]], except they are bent into shapes with a covariant part and a contravariant part.  (Cf. interactions between particles and their corresponding antiparticles.) 

A transformation can also be ordinary-natural in some variables and extraordinary-natural in other variables.  Sometimes this sort of transformation is called a *generalized natural transformation*.  The late Max Kelly was fond of saying that really it's all the same basic concept, however, so why proliferate terminology needlessly?  So he would simply say a transformation was "natural" in all its arguments, both the "ordinary" and the "extraordinary" ones.

The calculus of natural and extranatural transformations is a very simple string diagram calculus; perhaps the most basic one.  It was first introduced by Eilenberg, Kelly, and Mac Lane in the mid 60's.

There is also a yet more general notion of [[dinatural transformation]].  However, there are few examples of dinatural transformations which are not extranatural.  Also, unlike extranatural transformations, dinatural transformations cannot be generalized to all [[enriched categories]] and do not admit a natural string diagram calculus.

# Examples

Consider the hom-functor $\hom: Set^{op} \times Set \to Set$ (or more generally, the internal hom-functor $\hom: V^{op} \times V \to V$ where $V$ is symmetric monoidal closed). The identity transformation $1: \hom \to \hom$ has components of the form 

$$1_{x, y}: x^y \to x^y$$ 

and this of course is natural in each of the separate arguments $x, y$. String diagrammatically, this naturality would be represented by placing the domain over the codomain and linking the two instances of $x$ with a straight line and the two instances of $y$ with a straight line. Although it's trivial, let's at least record what naturality in say $y$ would mean: it means that for any morphism $g: y \to y'$ we have an equation of the form

$$1_{x, y} x^g = x^g 1_{x, y'}: x^{y'} \to x^y \qquad (1)$$

Now, the adjunction between (tensor) product and hom allow us to "bend" the transformation into another: 

$$eval_{x, y}: x^y \otimes y \to x$$ 

in which the two instances of $y$ are linked by a U-shape. This gives a transformation which is natural in $x$ but not of course in $y$; rather, in $y$ we have an equation which is companion to (1): 

$$eval_{x, y} (x^g \otimes y) = eval_{x, y'} (x^{y'} \otimes g): x^{y'} \otimes y \to x \qquad (2)$$ 

and we say in this case that $eval_{x, y}$ is **extranatural** in $y$. Notice how the extranatural variable $y$ in $eval_{x, y}$ appears once covariantly [in the tensor factor] and once contravariantly [in the exponent], but together on the same side of the arrow [here the domain]. (There is a nice string diagram picture for (2) which the reader might like to draw at this point.) 

Thus we already see that $eval_{x, y}$ is a "generalized natural" transformation, involving a mixture of naturality (in $x$) and extranaturality (in $y$).

The basic idea should now be clear, but let's give a few more examples. Starting with the identity transformation 

$$1_{x, y}: x \otimes y \to x \otimes y$$ 

we can again bend it using the tensor-hom adjunction to form an arrow 

$$coeval_{x, y}: x \to (x \otimes y)^y$$ 

where again $y$ appears once covariantly and once contravariantly, this time on the codomain side. The extranaturality in $y$ is the condition

$$(x \otimes g)^{y} coeval_{x, y} = (x \otimes y')^g coeval_{x, y'}$$

for every arrow $g: y \to y'$. 

As these examples indicate, instances of ordinary naturality are typically transferred into instances of extranaturality by means of adjunctions. Indeed, basic instances of U-shapes or upside-down U-shapes in string diagrams come about through counits and units of adjunctions, 

$$\varepsilon: F U \to 1 \qquad \eta: 1 \to U F$$

# Formalization 

Let $F\colon A\times B^{op}\times B \to D$ and $G\colon A\times C^{op}\times C\to D$ be functors.  A family of morphisms
$$ \alpha_{a,b,c}\colon F(a,b,b) \to G(a,c,c) $$
for $a\in A$, $b\in B$, and $c\in C$ is said to be **natural**, or more precisely *ordinary-natural in $a$ and extranatural in $b$ and $c$*, if the following hold.

* For all $f\colon a\to a'$ in $A$ and all $b\in B$ and $c\in C$, the following square commutes (ordinary naturality in $a$):
  $$\array{&F(a,b,b) & \overset{F(f,1,1)}{\to} & F(a',b,b) &\\
  ^{\alpha_{a,b,c}} &\downarrow && \downarrow & ^{\alpha_{a',b,c}}\\
  &G(a,c,c)& \underset{G(f,1,1)}{\to} & G(a',c,c) &}$$
* For all $g\colon b\to b'$ in $B$ and all $a\in A$ and $c\in C$, the following square commutes (extranaturality in $b$):
  $$\array{&F(a,b,b') & \overset{F(1,1,g)}{\to} & F(a,b,b) &\\
  ^{F(1,g,1)} &\downarrow && \downarrow & ^{\alpha_{a,b,c}}\\
  &F(a,b',b')& \underset{\alpha_{a,b',c}}{\to} & G(a,c,c) &}$$
* For all $h\colon c\to c'$ in $C$ and all $a\in A$ and $b\in B$, the following square commutes (extranaturality in $c$):
  $$\array{&F(a,b,b) & \overset{\alpha_{a,b,c}}{\to} & G(a,c,c) &\\
  ^{\alpha_{a,b,c'}} &\downarrow && \downarrow & ^{G(1,h,1)}\\
  & G(a,c',c') & \underset{G(1,1,h)}{\to} & G(a,c',c) &}$$


# Extranatural calculus

We set down a few basic lemmas which describe how extranatural transformations compose. These lemmas become very intuitive once one draws string diagrams to accompany them. (Cf. "yanking moves" in the string diagram calculus of adjunctions.) 

+-- {: .un_lemma}
###### Lemma 1 ("stalactites")

Let $F, G$ be functors of the form $C^{op} \times C \to D$. If $\alpha_{x, y}: F(x, y) \to G(x, y)$ is natural in $x, y$ and $\beta_x: G(x, x) \to H$ is extranatural in $x$ (for some object $H$ of $D$), then 
$$\beta_x \alpha_{x, x}: F(x, x) \to H$$ 
is extranatural in $x$.
=--

+-- {: .un_lemma}
###### Lemma 2 ("stalagmites")

Let $G, H$ be functors of the form $C^{op} \times C \to D$. If $\alpha_x: F \to G(x, x)$ is extranatural in $x$ (for some object $F$ of $D$) and $\beta_{x, y}: G(x, y) \to H(x, y)$ is natural in $x, y$, then 
$$\beta_{x, x} \alpha_x: F \to H(x, x)$$ 
is extranatural in $x$. 
=--

+-- {: .un_lemma}
###### Lemma 3 ("yanking")

Let $F, H$ be functors of the form $C \to D$, and let $G: C \times C^{op} \times C \to D$ be a functor. If $\alpha_{x, y}: F(y) \to G(x, x, y)$ is natural in $y$ and extranatural in $x$, and if $\beta_{x, y}: G(x, y, y) \to H(x)$ is natural in $x$ and extranatural in $y$, then 
$$\beta_{x, x} \alpha_{x, x}: F(x) \to H(x)$$ 
is natural in $x$. 
=--

# Profunctors

Extranatural transformations can be understood in the abstract setting of an [[autonomous category|autonomous]] monoidal [[bicategory]] or [[proarrow equipment]].

(more goes here...)


[[!redirects extranatural transformations]]
[[!redirects extraordinary natural transformation]]
[[!redirects extraordinary natural transformations]]
[[!redirects extranaturality]]
[[!redirects extraordinary naturality]]
