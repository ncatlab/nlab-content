
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--


# Effective epimorphisms
* table of contents
{:toc}

## Idea

An _effective epimorphism_ is a [[morphism]] $c\to d$ in a [[category]] which behaves in the way that a [[covering]] is expected to behave, in the sense that "$d$ is the union of the parts of $c$, identified with each other in some specified way".



## Definition 

\begin{definition}
An **effective epimorphism** in a [[category]] $C$ is a [[morphism]] $f \colon c \to d$ that has a [[kernel pair]] $c \times_d c$ and is the [[quotient object]] of this kernel pair, in that 

$$
  c \times_d c \;\rightrightarrows\; c \overset{f}{\to} d
$$

is a [[colimit]] diagram (a [[coequalizer]]).
\end{definition}

In other words, this says that $f : c \to d$ is effective if $d$ is the [[coimage]] of $f$.

Sometimes we say that such morphism $f$ is an [[effective quotient]].

The [[formal duality|dual]] concept is that of [[effective monomorphism]].

\begin{remark}
A morphism with a [[kernel pair]] (such as any morphism in a category with [[pullbacks]]) is an effective epimorphism if and only if it is a [[regular epimorphism]] (see [there](regular+epimorphism#MorphismsWithKernelPairsAreRegularIffEffective)) and a [[strict epimorphism]].  For morphisms without kernel pairs, the notion of effective epimorphism is of questionable usefulness.
\end{remark}


## Properties

### Relation to other notions of epimorphism

Every effective epimorphism is, of course, a [[regular epimorphism]] and hence a [[strict epimorphism]].  Conversely, a strict epimorphism which *has* a kernel pair is necessarily an effective epimorphism.  (This is a special case of the theory of [[generalized kernels]].)  For this reason, some writers use "effective epimorphism" in general to mean what is here called a [[strict epimorphism]].


## Examples

* In [[Set|the category of sets]], every [[epimorphism]] is effective.  Thus, it can be hard to know, when generalising concepts from $\Set$ to other categories, what kind of epimorphism to use.  In particular, one may define a [[projective object]] (and hence the [[axiom of choice]]) using effective epimorphisms.

* More generally, in any [[pretopos]], hence in particular in every [[topos]], every [[epimorphism]] is an effective epimorphism.  See, for instance, ([MacLane & Moerdijk 1992, Thm IV.7.8](#MacLaneMoerdijk), [Borceux 1994III, Prop. 3.4.13, 3.4.15](#Borceux94III)).

* In an [[(∞,1)-topos]] the bare notion of epimorphism disappears, and [[effective epimorphism in an (∞,1)-category]] becomes the default notion of epiness. A morphism in an $(\infty,1)$-topos is effective epi precisely if its [[n-truncated object in an (∞,1)-category|0-truncation]] is an epimorphism (hence an effective epimorphism) in the underlying 1-topos. This is Proposition 7.2.1.14 in Higher Topos Theory.

* In [[Top|the category of topological spaces]], open covers provide an example of effective epimorphisms. Suppose $X = \bigcup_{i \in I} U_i$ for $U_i \subset X$ open subsets. Then the gluing/pasting lemma states that continuous maps $f : X \to Y$ naturally correspond to families of continuous maps $f_i : U_i \to Y$ that agree on the intersections, so $f_i |_{U_i \cap U_j} = f_j |_{U_i \cap U_j}$. But this is precisely the statement that the induced morphism $\coprod_{i \in I} U_i \to X$ (induced by the inclusion maps $U_i \to X$) is an effective epi! Of course, arbitrary categories may not have arbitrary coproducts, hence why this definition uses a single object.

## Related concepts

* [[epimorphism]], [[regular epimorphism]], **effective epimorphism**

* [[effective epimorphism in an (∞,1)-category]]

## References

Original articles:

* {#Grothendieck61} [[Alexander Grothendieck]], p. 101 (4 of 21) in: _Techniques de construction et théorèmes d'existence en géométrie algébrique III: préschémas quotients_, Séminaire Bourbaki: années 1960/61, exposés 205-222, Séminaire Bourbaki, no. 6 (1961), Exposé no. 212,   ([numdam:SB_1960-1961__6__99_0](http://www.numdam.org/item/?id=SB_1960-1961__6__99_0), [pdf](http://www.numdam.org/item/SB_1960-1961__6__99_0.pdf))

Textbook accounts:

* [[Francis Borceux]], Def. 2.5.3 in: *[[Handbook of Categorical Algebra]]*, Vol. 2: *Categories and Structures*, Encyclopedia of Mathematics and its Applications **50**, Cambridge University Press (1994) ([doi:10.1017/CBO9780511525865](https://doi.org/10.1017/CBO9780511525865))


Exposition and examples:

* [[Qiaochu Yuan]], *[Regular and effective monomorphisms and epimorphisms](https://qchu.wordpress.com/2012/11/03/regular-and-effective-monomorphisms-and-epimorphisms/)*, 2012

Discussion in [[toposes]]:

* {#MacLaneMoerdijk} [[Saunders MacLane]], [[Ieke Moerdijk]], section IV.7  of _[[Sheaves in Geometry and Logic]]_

* {#Borceux94III} [[Francis Borceux]], Section 3.3.4 of: *[[Handbook of Categorical Algebra]]*. Vol. 3. *Categories of Sheaves*, Encyclopedia of Mathematics and its Applications **50** Cambridge University Press (1994) &lbrack;[doi:10.1017/CBO9780511525872](https://doi.org/10.1017/CBO9780511525872)&rbrack;
 

Discussion in [[homotopy type theory]] is in 

* [[Univalent Foundations Project]], section 7.6 of _[[Homotopy Type Theory -- Univalent Foundations of Mathematics]]_



[[!redirects effective epi]]
[[!redirects effective epimorphism]]
[[!redirects effective epimorphisms]]
