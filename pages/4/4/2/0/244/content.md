
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

However, a subcategory of $SymmMonCat$ whose objects are [[permutative categories]] and maps are symmetric strict monoidal functors, denoted by $Perm$  has a model category structure  which is transferred from the natural model category structure on $Cat$, see [Sharma](#Sharma). This model category structure is combinatorial, left-proper and a $Cat$-model category structure. It is referred to as the natural model category structure on $Perm$. The [[coherence theorem]] for symmetric monoidal categories states that each symmetric monoidal category is equivalent to a [[permutative category]].

### Relation to $\Gamma$-categories

The aforementioned natural model category of permutative categories is NOT a symmetric monoidal closed model category. This shortcoming was overcome in [Sharma] by constructing a Quillen equivalent [[model category]] which is symmetric monoidal closed.
A (unnormalized) $\Gamma$-category is a functor from $\Gamma^{op}$ to $Cat$, where $\Gamma^{op}$ is a skeletal category of finite based sets and based maps.
The category of $\Gamma$-categories and natural transformations, denoted by $\Gamma$$Cat$, is a symmetric monoidal closed category under the [[Day convolution]] product. The aforementioned symmetric monoidal closed model category is constructed in [Sharma](#Sharma) as a left-Bousfield localization of the projective model category structure on $\Gamma$$Cat$. A $\Gamma$-category is fibrant in this model category if it satisfies the Segal's condition in which case it is referred to as a coherently commutative monoidal category. The main result of [Sharma](#Sharma) is that an unnormalized version of the classical Segal's nerve functor is the right [[Quillen functor]] of a [[Quillen equivalence]] between the natural model category of permutative categories and the symmetric monoidal closed model category of coherently commutative monoidal categories.


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

### Permutations

For every $n \ge 2$ and $\sigma \in \mathfrak{S}_{n}$, there is a [[natural transformation]] 
$$\sigma_{A_{1},...,A_{n}}: A_{1} \otimes ... \otimes A_{n} \rightarrow A_{\sigma^{-1}(1)} \otimes ... \otimes A_{\sigma^{-1}(n)}$$
that is defined by the decomposition of a [[permutation]] in a product of adjacent [[transpositions]] and generalizes the [[braiding]] 
$$
B:A_{1} \otimes A_{2} \rightarrow A_{2} \otimes A_{1}
$$

We recall that an adjacent transposition $[1,n] \rightarrow [1,n]$ where $n \ge 2$ is a permutation $t:[1,n] \rightarrow [1,n]$ such that there exists a $1 \le i \le n-1$ such that: 
$$
t(1)=1,..., t(i-1)=i-1, t(i) = i+1, t(i+1) = i, t(i+2)=i+2,.... ,t(n)=n
$$
This $i$ is then unique, and for every $1 \le i \le n-1$, we note $t_{i}$ the associated adjacent transposition.

For $n \ge 2$, every permutation $\sigma \in \mathfrak{S}_{n}$ admits at least a decomposition under the form $\sigma = t_{i_{1}}; ...;t_{i_{q}}$
where $q \ge 0$, and $1 \le i_{1},....,i_{q} \le n-1$. 

In every symmetric monoidal category, for $n \ge 2$ and $1 \le i \le n-1$, we have a natural transformation 
$$t_{i}:A_{1} \otimes .... \otimes A_{n} \rightarrow A_{1} \otimes ... \otimes A_{i-1} \otimes A_{i+1} \otimes A_{i} \otimes A_{i+2} \otimes .... \otimes A_{n}$$ 
defined by: 
$$t_{i} = 1_{A_{1}} \otimes ... \otimes 1_{A_{i-1}} \otimes \B_{A_{i},A_{i+1}} \otimes 1_{A_{i+2}} \otimes ... \otimes 1_{A_{n}}$$

Given a $\sigma \in \mathfrak{S}_{n}$, the associated natural transformation is then defined as $t_{i_{1}};....;t_{i_{q}}$ for any such decomposition of $\sigma$. The fact that the result doesn't depend on the particular decomposition is a consequence of the [[coherence theorem for symmetric monoidal categories]].
 
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

  * [[symmetric monoidal dagger category]]

* [[closed monoidal category]] ,  [[closed monoidal (∞,1)-category]]

* [[symmetric monoidal closed category]]

* [[equivariant symmetric monoidal category]]

* [[symmetric bicategory]]

* [[symmetric monoidal groupoid]]

  * [[symmetric 2-group]], [[abelian ∞-group]]

* [[supply in a monoidal category]]

* [[commutative monoidal category]]

## References

Original references:

* {#MacLane} [[Saunders Mac Lane]], _Natural Associativity and Commutativity_ , Rice University Studies **49** (1963) 28-46 &lbrack;[rice:1911/62865](https://scholarship.rice.edu/handle/1911/62865)&rbrack;

* [[Jean Bénabou]], _Algèbre élémentaire dans les catégories_ (1964), C. R. Acad. Sci. Paris **258** (1964) 771-774 &lbrack;[ark:12148/bpt6k40102/f817](https://gallica.bnf.fr/ark:/12148/bpt6k40102/f817)&rbrack;

* {#EilenbergKelly65} [[Samuel Eilenberg]], [[G. Max Kelly]],  Part III of: *Closed Categories*, [[Samuel Eilenberg|S. Eilenberg]], [[D. K. Harrison]], [[S. MacLane]], [[H. Röhrl]] (eds.): *[[Proceedings of the Conference on Categorical Algebra - La Jolla 1965]]*, Springer (1966) 421-562 &lbrack;[doi:10.1007/978-3-642-99902-4](https://doi.org/10.1007/978-3-642-99902-4)&rbrack;



Textbook accounts:

* {#Borceux94} [[Francis Borceux]], Section 6.1 of: *Handbook of Categorical Algebra* Vol. 2: *Categories and Structures* $[$[doi:10.1017/CBO9780511525865](https://doi.org/10.1017/CBO9780511525865)$]$, Encyclopedia of Mathematics and its Applications **50**, Cambridge University Press (1994)

* [[Saunders MacLane]], Ch. XI of: *[[Categories for the Working Mathematician]]*, Graduate Texts in Mathematics **5** Springer (second ed. 1997) &lbrack;[doi:10.1007/978-1-4757-4721-8](https://link.springer.com/book/10.1007/978-1-4757-4721-8)&rbrack;

* {#EGNO15} [[Pavel Etingof]], [[Shlomo Gelaki]], [[Dmitri Nikshych]], [[Victor Ostrik]], *Tensor Categories*, AMS Mathematical Surveys and Monographs **205** (2015) $[$[ISBN:978-1-4704-3441-0](https://bookstore.ams.org/surv-205), [pdf](http://www-math.mit.edu/~etingof/egnobookfinal.pdf)$]$

  > (focused on [[tensor categories]])

* {#Perrone24} [[Paolo Perrone]], Chapter 6 of: *Starting Category Theory*, World Scientific (2024) \[<a href="https://doi.org/10.1142/13670">doi:10.1142/13670</a>, [arXiv:1912.10642](http://arxiv.org/abs/1912.10642)\]

Exposition of basics of [[monoidal categories]] and [[categorical algebra]]:

* _[[geometry of physics -- categories and toposes]]_, Section 2: _[Basic notions of categorical algebra](geometry+of+physics+--+categories+and+toposes#BasicNotionsOfCategoricalAlgebra)_


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

* Amit Sharma, _Symmetric monoidal categories and $\Gamma$-categories_
Theory and applications of Categories, Vol. 35, No. 14, (2020) pp. 417-512
 {#Sharma}

* Stefano Kasangian and Fabio Rossi. _Some remarks on symmetry for a monoidal category_. Bulletin of the Australian Mathematical Society 23.2 (1981): 209-214.

* J. M. Egger. _On involutive monoidal categories_. Theory and Applications of Categories 25.14 (2011): 368-393.

[[!redirects symmetric monoidal categories]]
[[!redirects symmetric monoidal structure]]
[[!redirects symmetric monoidal structures]]

[[!redirects symmetric monoidal]]
