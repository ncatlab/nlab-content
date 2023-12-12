
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

# Strict epimorphisms
* table of contents
{: toc}

## Definition

A **strict epimorphism** in a [[category]] is a [[morphism]] which is the joint [[coequalizer]] of all pairs of [[parallel morphisms]] that it coequalizes.  In other words, $f \colon B\to C$ is a strict epimorphism if it is the [[colimit]] of the (possibly [[large category|large]]) [[diagram]] consisting of all [[parallel morphisms|parallel pairs]] $g,h \colon A \;\rightrightarrows\; B$ such that $f g = f h$.  

Although this definition does not include this explicitly, it follows that $f$ is an [[epimorphism]].

A __strict monomorphism__ is a morphism such that its dual is strict epimorphism in the dual category.


## Relation to other epimorphism classes

If $f$ has a [[kernel pair]] $r,s \,\colon\,ker(f) \;\rightrightarrows\; B$ (such as if the ambient category has [[pullbacks]]), then any such pair $g,h$ factor uniquely through the kernel pair, which is itself such a pair (that is, $f r = f s$).  Thus, for any $k \colon B\to D$, we have $k g = k h$ for all $g,h$ with $f g = f h$ if and only if $k r = k s$.  Therefore, $f$ is strict epi if and only if it is the coequalizer of its kernel pair, hence if and only if it is an [[effective epimorphism]] and therefore a [[regular epimorphism]].

For this reason, some sources define "regular epimorphism" in a category without pullbacks to mean what we have called a "strict epimorphism."

It is easy to see that in *any* category, any regular epimorphism is strict.  In a category without pullbacks, it seems that not every strict epimorphism need be regular.  However, every strict epimorphism is [[strong epimorphism|strong]], and hence [[extremal epimorphism|extremal]], for the same reason that any regular epimorphism is.


## Properties
If for an epimorphism $f$, the composition $g \circ f$ is a strict epimorphism then $g$ is a strict epimorphism.

## References

* [[Alexander Grothendieck]], Definition 2.2, p. 304 in:  *Technique de descente et théorèmes d'existence en géométrie algébrique. I. Généralités. Descente par morphismes fidèlement plats* ([[FGA]]), Séminaire Bourbaki, no. 5 (1960) &lbrack;[numdam:SB_1958-1960__5__299_0](http://www.numdam.org/item/SB_1958-1960__5__299_0)&rbrack;

See also Definition 2.1 in 

* [[Eduardo J. Dubuc]], _From Yoneda to Topoi morphisms_, [arXiv](https://arxiv.org/abs/2312.04716).


Textbook accounts:

* [[Ion Bucur]], [[Aristide Deleanu]], _Introduction to the theory of categories and functors_, Wiley, 1968.  

* [[Masaki Kashiwara]], [[Pierre Schapira]], p. 115-116 in: _[[Categories and Sheaves]]_ 


[[!redirects strict epimorphisms]]
[[!redirects strict epi]]
[[!redirects strict epis]]

[[!redirects strict monomorphism]]
[[!redirects strict monomorphisms]]
[[!redirects strict mono]]
[[!redirects strict monos]]
