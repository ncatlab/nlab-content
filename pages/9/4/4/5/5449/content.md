
> This needs to be merged with _[[filtered chain complex]]_


### Idea

It's easy to say what chain complex and homology mean (that is, these notions are definable); where things get tricky is, when calculating them, to figure out what the modules and differentials, kernels and images actually _are_.  Sometimes there's extra structure, e.g. a further hierarchy beyond the usual grading, that lets us figure these things out one layer at a time.  Then we have to glue the layers back together, and that's one place a [[spectral sequence]] is handy

### Definition

For a [[poset]] $I$ and an [[abelian category]] $A$, an $I$-**filtered complex** is a functor $F:I\to Mon(Ch(A))$, from $I$ to monomorphisms of chain complexes in $A$.  Roughly, this boils down to 

* A Complex $d:C\to C$, $d^2=0$
* with a submodules $F_i \lt C$ for $i$ an object of $I$
* such that $F_i \lt F_{j} $ for $i\lt j$ in $I$
* such that $ d F_i \lt F_i $.

(You may have noticed this isn't the usual notation for functors.  It's traditional.)

The most frequent examples have $I=\mathbb{N}\cup\{\infty\}$, $I=-\mathbb{N}$, or $I=\mathbb{Z}\cup\{\infty\}$, with their usual total orderings; in this connection see [[spectral sequence of a filtered complex]]

Usually $C$ is a _graded_ complex, with $d_j:C_j\to C_{j-1}$, and in this case we ask
$$d_j:F_i\cap C_j \to F_i\cap C_{j-1}.$$
(If you prefer cohomology differentials, read $+$ for $-$.)

### Associated Graded complex

In the special case of a discrete totally-ordered filtration, one defines the associated graded complex $G_i(F) = F_{i+1}/F_i$ with differential induced by $d[x] = [d x]$; again, if $(C,d)$ is graded, we have a bigraded complex with components $G_i\cap C_j$ and differential of bidegree $(\pm 1, 0)$.

### References

Any book introducing spectral sequences.