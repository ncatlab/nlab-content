
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea 

A _symmetric monoidal category_ is a category with a product operation -- a [[monoidal category]] -- for which the product is _as commutative as possible_.

The point is that there are different degrees to which higher categorical products may be commutative. While a bare [[monoid]] is either commutative or not, a [[monoidal category]] may be a [[braided monoidal category]] -- which already means that the order of products may be reversed up to some [[isomorphism]] -- without being _symmetric_ monoidal -- which means that changing the order of a product twice, from $a \otimes b$ to $b \otimes a$ back to $a \otimes b$, indeed does yield a result [[equality|equal]] to the original.

For higher monoidal categories there are accordingly ever more shades of the notion of "commutativity" of the monoidal product. This is described in detail at [[k-tuply monoidal n-category]]. 

In general, the term _symmetric monoidal_ is used for the maximally commutative case. See for instance [[symmetric monoidal (∞,1)-category]]. Notably, a symmetric monoidal [[∞-groupoid]] is, under the [[homotopy hypothesis]], the same as a [[spectrum|connective spectrum]].

A symmetric monoidal category is a special case of the notion of [[symmetric pseudomonoid]] in a [[sylleptic monoidal 2-category]].

## Definition

+-- {: .num_defn} 
###### Definition


A **symmetric monoidal category** is a [[braided monoidal category]] for which the [[braiding]] 

$$ 
   B_{x,y} \colon x \otimes y \to y \otimes x 
$$

satisfies the condition:

$$ 
  B_{y,x} \circ B_{x,y} = 1_{x \otimes y}  
$$

for all objects $x, y$

=--

Intuitively this says that switching things twice _in the same direction_ has no effect.

Expanding this out a bit: a  **symmetric monoidal category** is, to begin with a [[category]] $M$ equipped with a [[functor]]
$$ \otimes : M \times M \to M $$
called the **tensor product**, an object
$$ 1 \in M $$
called the **unit object**, a natural isomorphism
$$ a_{x,y,z} : (x \otimes y) \otimes z \to x \otimes (y \otimes z) $$
called the **associator**, a natural isomorphism
$$ \lambda_x : 1 \otimes x \to x $$
called the **left unitor**, a natural isomorphism 
$$  \rho_x : x \otimes 1 \to x $$
called the **right unitor**, and a natural isomorphism
$$ B_{x,y} : x \otimes y \to y \otimes x $$
called the **braiding**.  We then demand that the associator obey the **pentagon identity**, which says this diagram commutes:

+--{: style="text-align:center"}
[[!include monoidal category > pentagon]]
=--


We demand that the associator and unitors  obey the **triangle identity**, which says this diagram commutes:

$$
  \array{
     & (x \otimes 1) \otimes y &\stackrel{a_{x,1,y}}{\longrightarrow} & x \otimes (1 \otimes y)
      \\
      
      & {}_{\rho_x \otimes 1_y}\searrow
       
       && \swarrow_{1_x \otimes \lambda_y}
      & 
     \\
     &&
     x \otimes y
     &&
     
  }
$$

We demand that the braiding and associator obey the first **hexagon identity**:

$$
  \array{
   (x \otimes y) \otimes z 
   &\stackrel{a_{x,y,z}}{\to}&
   x \otimes (y \otimes z)
   &\stackrel{B_{x,y \otimes z}}{\to}&
   (y \otimes z) \otimes x
   \\
   \downarrow^{B_{x,y}\otimes 1_z}
   &&&&
   \downarrow^{a_{y,z,x}}
   \\
   (y \otimes x) \otimes z
   &\stackrel{a_{y,x,z}}{\to}&
   y \otimes (x \otimes z)
   &\stackrel{1_y \otimes B_{x,z}}{\to}&
   y \otimes (z \otimes x)
  }
$$

And lastly, we demand that
$$ B_{y,x} B_{x,y} = 1_{x \otimes y} . $$
(The definition of [[braided monoidal category]] has _two_ hexagon identities, but either one implies the other given this equation.)


## Properties

### The 2-category of symmetric monoidal categories

There is a [[strict 2-category]] $SymmMonCat$ with:

* symmetric monoidal categories as objects,
* [[symmetric monoidal functor]]s as morphisms, 
* [[symmetric monoidal natural transformation]]s as 2-morphisms.

This 2-category has (weak) 2-[[biproducts]] given by the cartesian product of underlying categories (analogously to how [[Ab]] has biproducts given by the cartesian product of underlying sets).  For a proof, see [Fong-Spivak, Theorem 2.3](#FongSpivak), or for a more abstract version involving [[pseudomonoids]] [Schaeppi, Appendix A](#Schaeppi).

### As models for connective spectra
  {#ModelsForConnectiveSpectra}

The [[group completion]] of the [[nerve]] of a symmetric monoidal category is always an  [[infinite loop space]], hence the degree-0-space of a [[connective spectrum]]. One calls this also the [[K-theory]] spectrum of the symmetric monoidal category:

$$
  \array{
     &&&& Spectra
     \\
      && {}^{\mathllap{K}}\nearrow && \downarrow
    \\
    SymmMonCat &\to& Cat &\underset{N}{\to}& sSet
  }
  \,.
$$

This construction extended to an [[equivalence of categories]] 

$$
  K :  Ho(SymmMonCat)
   \stackrel{\simeq}{\to}
  Ho(Spectra)_{\geq 0}
  \hookrightarrow
  Ho(Spectra)
$$ 

between the [[full subcategory]] of the [[stable homotopy category]] $Ho(Spectra)$ on the [[connective spectra]] and the [[homotopy category]] of $SymmMonCat$, regarded with the [[transferred model structure|transferred structure]] of a [[category with weak equivalences]].

This is due to ([Thomason, 95](#Thomason)). Further discussion is in ([Mandell, 2010](#Mandell)).

Notice that this is _almost_ the complete analog in [[stable homotopy theory]] of the [[Quillen equivalence]] between the [[Thomason model structure]] on [[Cat]] and the standard [[model structure on simplicial sets]]. Only that $SymmMonCat$ cannot carry a [[model category]] structure because it does not have all [[colimit]]s. In some sense the "colimit completion" of $SymmMonCat$ is the category of [[multicategories]]. Once expects that this carries a model structure that refines the above equivalence of homotopy categories to a [[Quillen equivalence]].

(This is currently being investigated by Elmendorf, Nikolaus and maybe others.)

However, a subcategory of $SymmMonCat$ whose objects are Permutative categories and maps are strict symmetric monoidal functors, denoted by $Perm$  has a model category structure  which is transferred from the natural model category structure on $Cat$. The [[coherence theorem]] for symmetric monoidal categories states that each symmetric monoidal category is equivalent to a [[permutative category]].




### As algebras over the little $k$-cubes operad

A symmetric monoidal category is equivalently a category that is equipped with the structure of an [[algebra over an operad|algebra over]] the [[little cubes operad|little k-cubes operad]] for $k \geq 3$

Details are in examples 1.2.3 and 1.2.4 of

* [[Jacob Lurie]], $\mathbb{E}[k]$-[[Ek-Algebras|Algebras]]

### Tannaka duality

[[!include structure on algebras and their module categories - table]]

### Grothendieck ring

The [[Grothendieck group]] of a [[monoidal category]] naturally has the structure of a [[monoid]], of an [[abelian category|abelian]] monoidal category that of a [[ring]], of an abelian [[braided monoidal category]] that of a [[commutative ring]] and, finally, of an abelian symmetric monoidal category that of a _[[Lambda-ring]]_. See there for more.

### Internal logic

The [[internal logic]] of ([[closed monoidal category|closed]]) symmetric monoidal categories is called _[[linear logic]]_. This notably contains [[quantum logic]].


## Examples 

* Every [[cartesian monoidal category]] is necessarily symmetric monoidal, due to the essential uniqueness of the categorical [[product]]. This includes cases such as [[Set]], [[Cat]].

* For $k$ some [[field]], the category [[Vect]] of $k$-vector spaces carries the standard structure of a [[monoidal category]] coming from the [[tensor product]], over $k$, of vector spaces. The standard braiding that identifies $V \otimes W$ with $W \otimes V$ by mapping homogeneous elements $v \otimes w$ to $w \otimes v$ obviously makes [[Vect]] into a symmetric monoidal category.

* The category of $\mathbb{Z}_2$-[[graded vector space]]s, on the other hand, has two different symmetric monoidal extensions of the standard [[tensor product]] monoidal structure. One is the trivial one from above, the other is the one that induces a a sign when two odd-graded vectors $v$ and $w$ are passed past each other : $v \otimes w \mapsto - w \otimes v$. This non-trivial symmetric monoidal structure on $Vect[\mathbb{Z}_2]$ defines the symmetric monoidal category of [[super vector spaces]].

* The monoidal category of [[graded modules]] over a [[commutative ring]] (with the usual [[tensor product of modules|tensor product of graded modules]]) can be made into a braided monoidal category with the braiding 

$$
  \array{
    V \otimes W &\longrightarrow& W \otimes V
    \\
    x \otimes y &\mapsto& y \otimes x
  }
  \,.
$$

The braiding $x \otimes y \mapsto (-1)^{|x| |y|} y \otimes x$ (where $|x|$ and $|y|$ denote the degrees) is also commonly used.

  More generally, for any invertible element $u$ of the base ring, there is the [[braided monoidal category|braiding]] $x \otimes y \mapsto u^{|x| |y|} y \otimes x$, and these braidings are the only possible. The resulting [[braided monoidal category]] is symmetric if and only if $u^2 = 1$.



## Related concepts

* [[monoidal category]], [[monoidal (∞,1)-category]]

* **symmetric monoidal category**, [[symmetric monoidal (∞,1)-category]], [[symmetric monoidal (∞,n)-category]] 

  * [[permutative category]], [[bipermutative category]]

* [[closed monoidal category]] ,  [[closed monoidal (∞,1)-category]]

* [[equivariant symmetric monoidal category]]

## References

Exposition of basics of [[monoidal categories]] and [[categorical algebra]]:

* _[[geometry of physics -- categories and toposes]]_, Section 2: _[Basic notions of categorical algebra](geometry+of+physics+--+categories+and+toposes#BasicNotionsOfCategoricalAlgebra)_


* {#EGNO15} [[nLab:Pavel Etingof]], Shlomo Gelaki, Dmitri Nikshych, [[nLab:Victor Ostrik]], chapter 2 of _Tensor categories_, Mathematical Surveys and Monographs, Volume 205, American Mathematical Society, 2015 ([pdf](http://www-math.mit.edu/~etingof/egnobookfinal.pdf))


A survey of definitions of symmetric monoidal categories, [[symmetric monoidal functor]]s and [[symmetric monoidal natural transformation]]s, is also in

* [[John Baez]], _[Some definitions everyone should know](http://math.ucr.edu/home/baez/qg-fall2004/definitions.pdf)_

For an elementary introduction to symmetric monoidal categories using string diagrams, see:

* [[John Baez]] and [[Mike Stay]], [Physics, topology, logic and computation: a Rosetta Stone](http://math.ucr.edu/home/baez/rosetta.pdf).

The theorem that symmetric monoidal categories model all connective spectra is due to 

* R. Thomason, _Symmetric monoidal categories model all connective spectra_ , Theory and applications of Categories, Vol. 1, No. 5, (1995) pp. 78-118
 {#Thomason}

More discussion is in 

* [[Michael Mandell]], _An Inverse K-Theory Functor_ ([arXiv:1002.3622](http://arxiv.org/abs/1002.3622))
 {#Mandell}

* {#FongSpivak} Brendan Fong and David I, Spivak, *Supplying bells and whistles in symmetric monoidal categories*, [arxiv](https://arxiv.org/abs/1908.02633), 2019

* {#Schaeppi} Daniel Schäppi, *Ind-abelian categories and quasi-coherent sheaves*, [arxiv](https://arxiv.org/abs/1211.3678), 2014

* [[Amit Sharma]], _Symmetric monoidal categories and $\Gamma$-categories_
Theory and applications of Categories, Vol. 35, No. 14, (2020) pp. 417-512
 {#Sharma}

[[!redirects symmetric monoidal categories]]
[[!redirects symmetric monoidal structure]]
[[!redirects symmetric monoidal structures]]

[[!redirects symmetric monoidal]]
