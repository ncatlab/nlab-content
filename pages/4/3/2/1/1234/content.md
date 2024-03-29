
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Motivic cohomology
+--{: .hide}
[[!include motivic cohomology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

[[Grothendieck]]  [[conjecture|conjectured]] that every [[Weil cohomology theory]] factors uniquely through some [[category]], which he called the category of _[[motives]]_.  For [[smooth variety|smooth]] [[projective varieties]] (over some [[field]] $k$) such a category was given by Grothendieck himself, called the category of _pure [[Chow motives]]_.  For general smooth varieties the category is still conjectural, see at _[[mixed motives]]_.

## Construction

Fix some [[adequate equivalence relation]] $\sim$ (e.g. [[rational equivalence]]).  Let $Z^i(X)$ denote the group of $i$-[[codimension|codimensional]] [[algebraic cycles]] and let $A^i_\sim(X)$ denote the [[quotient]] $Z^i(X)/\sim$.

### Category of correspondences  

Let $Corr_\sim(k)$, the category of [[correspondences]], be the [[category]] whose [[objects]] are [[smooth variety|smooth]] [[projective varieties]] and whose [[hom-sets]] are the [[direct sum]]

$$
  Corr_\sim(h(X),h(Y)) = \bigoplus_i A^{n_i}_\sim(X_i \times Y)
  \,,
$$

where $(X_i)$ are the [[irreducible components]] of $X$ and $n_i$ are their respective [[dimensions]].  The [[composition]] of two [[morphisms]] $\alpha \in Corr(X,Y)$ and $\beta \in Corr(Y,Z)$ is given by
$$ p_{XZ,*} (p_{XY}^*(\alpha) . p_{YZ}^*(\beta)) $$
where $p_{XY}$ denotes the [[projection]] $X \times Y \times Z \to X \times Y$ and so on, and $.$ denotes the [[intersection product]] in $X \times Y \times Z$.

There is a canonical [[contravariant functor]] 

$$
  h \colon SmProj(k) \to Corr_\sim(k)
$$ 

from the category of smooth projective varieties over $k$ given by [[mapping]] $X \mapsto X$ and a morphism $f : X \to Y$ to its [[graph of a function|graph]], the [[image]] of its [[graph morphism]] $\Gamma_f : X \to X \times Y$. 

The [[category of correspondences]] is [[symmetric monoidal category|symmetric monoidal]] with $h(X) \otimes h(Y) \coloneqq h(X \times Y)$.

We also define a category $Corr_\sim(k, R)$ of correspondences with [[coefficients]] in some [[commutative ring]] $R$, by [[tensor product|tensoring]] the morphisms with $R$; this is a $R$-[[linear category]] [[additive category|additive]] [[symmetric monoidal category|symmetric monoidal]] category.

### Category of effective pure motives  

The [[Karoubi envelope]] (pseudo-abelianisation) of $Corr_\sim(k, R)$ is called the category of **effective pure motives** (with coefficients in $R$ and with respect to the equivalence relation $\sim$), denoted $Mot^eff_\sim(k, R)$.  

Explicitly its objects are [[pairs]] $(h(X), p)$ with $X$ a smooth projective variety and $p \in Corr(h(X), h(X))$ an [[idempotent]], and [[morphisms]] from $(h(X), p)$ to $(h(Y), q)$ are morphisms $h(X) \to h(Y)$ in $Corr_\sim$ of the form $q \circ \alpha \circ p$ with $\alpha \in Corr_{\sim}(h(X), h(Y))$.

This is still a [[symmetric monoidal category|symmetric monoidal]] category with $(h(X), p) \otimes (h(Y), q) = (h(X \times Y), p \times q)$.  Further it is a [[Karoubian category|Karoubian]], $A$-[[linear category|linear]] and [[additive category|additive]].

The image of $X \in SmProj(k)$ under the above functor 

$$
  h \colon SmProj(k) \to Corr_\sim(k,A) \to Mot^{eff}_\sim(k,R) 
$$

is the **the motive of $X$**.

### Category of pure motives  

There exists a motive $\mathbf{L}$, called the **[[Lefschetz motive]]**, such that the motive of the [[projective line]] decomposes as

$$h(\mathbf{P}^1_k) = h(\Spec(k)) \oplus \mathbf{L}$$

To get a [[rigid category]] we formally invert the Lefschetz motive and get a category 

$$
  Mot_\sim(k, R)
  \coloneqq
  Mot^{eff}_\sim(k,R)[\mathbf{L}^{-1}]
  \,,
$$ 

the **category of pure motives** (with coefficients in $R$ and with respect to $\sim$).  

This is a [[rigid category|rigid]], [[Karoubian category|Karoubian]], [[symmetric monoidal category]].  Its objects are triples $(h(X), p, n)$ with $n \in \mathbf{Z}$.

### Category of pure Chow motives

When the relation $\sim$ is [[rational equivalence]] then $A^*_\sim$ are the [[Chow groups]], and $Mot_\sim(k) = Mot_{rat}(k)$ is called the category of **pure [[Chow motives]]**.  This category has the advantage that it is universal for [[Weil cohomology theory|Weil cohomology theories]]: that is, every Weil cohomology factors uniquely through it.


### Category of pure numerical motives

When the relation $\sim$ is [[numerical equivalence]], then one obtains
_[[numerical motives]]_.  This category has the advantage of being a [[semisimple category|semisimple]] [[abelian category]].  In fact, [[Uwe Jannsen]] proved that numerical equivalence is the only [[adequate equivalence relation]] that gives a semisimple abelian category of pure motives.



## Related concepts

* [[sheaf with transfer]]

* [[motive]]

* [[mixed motive]]

* [[Voevodsky motive]]

* [[noncommutative motive]]



## References 

* [[Daniel Dugger]], *Navigating the Motivic World*.   ([pdf](http://www.stat.ucla.edu/~ywu/wbook.pdf))   A draft of a user-friendly introduction to motives, especially good if you're coming to this topic through algebraic topology.

* [[Uwe Jannsen]], Motives, numerical equivalence, and semi-simplicity, Invent. Math. 107.3 (1992): 447-452.  ([pdf](https://epub.uni-regensburg.de/26642/1/jannsen10.pdf))

*  [[Minhyong Kim]], _Classical Motives: Motivic $L$-functions_ ([pdf](http://www.ucl.ac.uk/~ucahmki/ihes3.pdf))

* [[Bruno Kahn]], [pdf slides](http://www.aimath.org/WWN/motivesdessins/PaloAlto1.pdf) on pure motives

* [[Yuri Manin]], _Correspondences, motifs and monoidal transformations_ , Math. USSR Sb. 6 439, 1968([pdf](http://resources.agssp2012.torsor.org/documents/manin.pdf), [web](http://iopscience.iop.org/0025-5734/6/4/A01))

*  [[James Milne]], _Motives -- Grothendieck's Dream_ ([pdf](http://www.jmilne.org/math/xnotes/MOT.pdf))

* [[Tony Scholl]], _Classical motives_, in Motives, Seattle 1991. Proc Symp. Pure Math 55 (1994), part 1, 163-187 ([pdf](https://www.dpmms.cam.ac.uk/~ajs1005/preprints/classical_motives.pdf))

* R. Sujatha, _Motives from a categorical point of view_,  Lecture notes (2008) ([pdf](http://www.math.tifr.res.in/~sujatha/ihes.pdf))
 {#Sujatha}

Section 8.2 of 

* [[Alain Connes]], [[Matilde Marcolli]], _[[Noncommutative Geometry, Quantum Fields and Motives]]_  ([pdf](http://www.alainconnes.org/docs/bookwebfinal.pdf))



category: algebraic geometry

[[!redirects pure motives]]
[[!redirects category of pure motives]]