#Definition#

The **category algebra** $k[C]$ over a ground field $k$ of a small [[category]] $C$ is as a vector space spanned by the morphisms of $C$, 

$$k[C] = span_k(C_1)
\,,
$$ 

where the product of two morphisms $f$ and $g$ is defined to be their composite if composable, and 0 otherwise

$$
  f \cdot g := \left\lbrace
    \array{
      g \circ f & if composable
      \\
      0 & otherwise
    }
  \right.
 \,.
$$ 

#Remarks#

If the category $C = \mathbf{B}G$ is a [[groupoid]] with a single object, which is canonically identified with a group $G$, then the category algebra coincides with the familiar [[group algebra]], 

$$
 k[\mathbf{B}G] = k[G]
  \,.
$$


+--{.query}

I think that the nLab presents a fantastic opportunity to define familiar concepts _arrow theoretically_. Is there a more arrow theoretic way to define a category algebra? - [[Eric Forgy|Eric]]

Yes. There is a bigger story hidden here. I have added 
more material below. --[[Urs Schreiber|Urs]]

=--

#Arrow-theoretic interpretation#

The category algebra of a category $C$ is a special case of a general [[arrow theory|arrow-theoretic]] construction that appears in [[quantization]] and in the theory of [[bi-brane]]s. 

In order not to get discracted by inessential technicalities, consider the case of a finite [[category]] $C$, i.e. a category [[internalization|internal to]] $FiniteSets$. This is a [[span]]

$$
  \array{
     && C_1
      \\
      & {}^{s}\swarrow
      && \searrow^{t}
     \\
     C_0
     &&&&
     C_0
  }
$$

equipped with a composition operation: a morphism
of spans from the composite span 

$$
  \array{
     &&&&
     C_1 \times_{t,s} C_1
     \\
     &&& \swarrow && \searrow
     \\
     && C_1
     &&&& C_1
      \\
      & {}^{s}\swarrow
      && \searrow^{t}
      && {}^{s}\swarrow
      && \searrow^{t}
     \\
     C_0
     &&&&
     C_0
     &&&&
     C_0
  }
$$

to the original one, i.e. a morphism 

$$
  comp : C_1 \times_{t,s} C_1 \to C_1
$$ 

which respects source and target morphisms. 

Given this, consider the trivial vector bundle on the set of objects $C_0$. This is nothing but an assignment

$I : C_0 \to Vect_k$

of the ground field $k$ to each element of $C_0$. There are two different ways to pull this vector bundle on objects back to a vector bundle on morphisms, once along the source, once along the target map. 

Then notice that the set of natural transformations between these two vector bundles

$$
  Hom_{[Sets,Vect_k]}(s^* I , t^* I)
$$

whose elements are 2-arrows of the form

$$
  \array{
     && C_1
      \\
      & {}^{s}\swarrow
      && \searrow^{t}
     \\
     C_0
     &&\stackrel{f}{\Rightarrow}&&
     C_0
     \\
     & {}_I \searrow && \swarrow_I
     \\
     &&
     Vect_k
  }
$$

are canonically in bijection with $k$-calued functions on $C_1$, hence with the vector space spanned by $C_1$, hence with the vector space underlying the category algebra

$$
  Hom_{[Sets,Vect_k]}(s^* I , t^* I)
  \simeq
  k[C]
  \,.
$$

The algebra structure on $k[C]$ is similarly encoded in the diagrammatics: given two elements

$$
  \array{
     && C_1
      \\
      & {}^{s}\swarrow
      && \searrow^{t}
     \\
     C_0
     &&\stackrel{f}{\Rightarrow}&&
     C_0
     \\
     & {}_I \searrow && \swarrow_I
     \\
     &&
     Vect_k
  }

  \;\;\;\; 
  and
  \;\;\;\;

  \array{
     && C_1
      \\
      & {}^{s}\swarrow
      && \searrow^{t}
     \\
     C_0
     &&\stackrel{g}{\Rightarrow}&&
     C_0
     \\
     & {}_I \searrow && \swarrow_I
     \\
     &&
     Vect_k
  }
$$

their pre-composite is the diagram

$$
  \array{
     &&&&
     C_1 \times_{t,s} C_1
     \\
     &&& \swarrow && \searrow
     \\
     && C_1
     &&&& C_1
      \\
      & {}^{s}\swarrow
      && \searrow^{t}
      && {}^{s}\swarrow
      && \searrow^{t}
     \\
     C_0
     &&\stackrel{f}{\Rightarrow}&&
     C_0
     &&\stackrel{g}{\Rightarrow}&&
     C_0
     \\
     & \searrow &&& 
     \downarrow &&& \swarrow
     \\
     && \to &&Vect_k&& \leftarrow  
  }
  \,.
$$

This is a composite transformation between three trivial vector bundles on the set $C_1 \times_{t,s} C_1$ of composable morphisms in $C$. As such, it is a function, which on the element consisting of the composable pair $\stackrel{r}{\to}\stackrel{s}{\to}$ takes the value $f(r)\cdot g(s)$.

In order to get back a transformation between vector bundles on $C_1$, hence a transformation between vector bundles on $C_1$, we _push forward_ along the composition map $comp: C_1 \times_{t,s} C_1 \to C_1$. This just means that we add up the values on the fibers of this map.

The result is the [[convolution product]]

$$
  (f\star g) : t \mapsto \sum_{s\circ r = t}
  f(r)\cdot g(s)
  \,.
$$

This is indeed the product in the category algebra.

##References on this arrow-theoretic picture##

The claim is that this way of looking at category algebras realizes them as a puny sepcial case of a bigger story which involves [[bi-brane]]s as morphisms between $n$-bundles/$(n-1)$-gerbes which live on spaces connected by correspondence spaces. This is related to a bunch of things,  such as T-duality, Fourier-Mukai transformations and other issues of quantization. I am hoping in the not too far future we can provide a somewhat comprehensive account of all this. For the moment I just point to some blog entries which deal with facets of this story

* John Baez, [_Quantization and Cohomology (Week 17)_](http://golem.ph.utexas.edu/category/2007/03/quantization_and_cohomology_we_16.html)

* Urs Schreiber, [_QFT of Charged n-Particle: T-Duality_](http://golem.ph.utexas.edu/category/2007/02/qft_of_charged_nparticle_tdual.html)

I expect that there is in addition nice formulation of these issues in the context of  [[enriched category theory]] using the [[Day convolution]] product. But I am not sure yet. 