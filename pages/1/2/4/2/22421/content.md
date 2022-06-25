
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A *finitely generated group* is a ([[discrete group|discrete]]) [[group]] (equipped) with a [[finite set]] of [[generators]], hence of [[elements]] such that any other element can be written as a product of these.

## Properties

### Relation to Cayley graphs

Associated with a set of generators on a group is the corresponding [[Cayley graph]], whose [[vertices]] are the group elements which are connected by an [[edge]] if they differ by (left, say) multiplication with one of the generators.

The corresponding [[graph distance]] equips the group with a [[metric]] (the *[[word metric]]*) and thus makes it an object of [[geometric group theory]].

## Examples

\begin{example}
**([[symmetric group]])**
\linebreak
The [[symmetric group]] $Sym(n)$ of [[permutations]] of $n \in \mathbb{N}$ [[elements]] may be [[finitely generated group|generated]] from: 

* all [[transposition permutations]] -- the corresponding Cayley [[graph distance]] is the original *[[Cayley distance]]*;

* the *adjacent* [[transpositions]] -- the corresponding Cayley [[graph distance]] is known as the *[[Kendall tau distance]]*.

\end{example}

\begin{example}\label{BraidGroupExample}
**([[braid group]])**
\linebreak
The [[braid group]] $Br(n)$ on $n \in \mathrm{N}$ strands is finitely generated via the *[Artin presentation](braid+group#ArtinPresentation)*.
\end{example}


## Related concepts

* [[finite group]], [[profinite group]]

* [[generators and relations]]

* [[finitely generated object]]

  * [[finitely generated algebra]]

  * [[finitely generated group]]

  * [[finitely generated module]], [[finitely presented module]]


## References

Textbooks:

* [[Cornelia Druţu]], [[Michael Kapovich]], Chapter 7 of: *Geometric group theory*, Colloquium Publications **63**, AMS 2018 ([ISBN:978-1-4704-1104-6](https://bookstore.ams.org/coll-63/), [pdf](https://courses.maths.ox.ac.uk/node/view_material/35649))

See also 

* Wikipedia, *[Finitely generated group](https://en.wikipedia.org/wiki/Finitely_generated_group)*

Discussion in [[homotopy type theory]]/[[univalent foundations of mathematics]]:

* [[Marc Bezem]], [[Ulrik Buchholtz]], [[Pierre Cagne]], [[Bjørn Ian Dundas]], [[Daniel R. Grayson]]: Chapter 6 of: *[[Symmetry]]* (2021) $[$[pdf](https://unimath.github.io/SymmetryBook/book.pdf)$]$

