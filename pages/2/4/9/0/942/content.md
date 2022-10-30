
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

### Profinite completion of a group

The **profinite completion** $\hat{G}$ of a ([[discrete group|discrete]]) [[group]] $G$ is the [[limit]] (in the [[category]] of [[topological groups]]) over the [[diagram]] with [[objects]] the [[quotient groups]] $G/N_{fin}$ where $N_{fin}$ is a [[normal subgroup]] of $G$ with [[finite number|finite]] [[index of a subgroup|index]], and [[morphisms]] induced from the [[lattice]] of [[subgroups]] of $G$. 

Note that the profinite completion actually is a [[profinite group]], and there is a canonical homomorphism $G \to \hat{G}$.

+-- {: .query}
[[Tim Porter|Tim]]:  Three points: (i) I suggest a hat $\hat{G}$ as notation for completion, (ii) in taking limits you have to specify in what category your are living at that instant!  Here it is not the limit in the category of groups that has to be taken but withing the category of topological groups, so you have to consider each finte group as a discrete topological group.  Because of this (iii) the actual entry on [[profinite group]] takes one to be a [[pro-object]] in the category of finite groups. (The way to handle this may need to be discussed to get consensus on which we all like best.)

I am not sure what name the [[SGA1]] type fundamental group should be called. I do not particularly like the one you use below.

[[David Roberts]]: This was a knock-together job, I must admit. Actually I think the SGA1 fundamental group is called the algebraic fundamental group - in the case of schemes its also called the etale fundamental group, but I personally think 'algebraic' would fit better in this example - it is changed!

I'll also leave off the description of this object to its own page. Sometime I'll also get around to writing about [[Grothendieck's Galois theory]].

[[Mike Shulman|Mike]]: Of course, it would be more consistent to use the same definition of profinite group here as at [[profinite group]].  As I said there, I prefer the cofiltered-system definition since it is more "basic"  and explains why you have to consider topological groups if you want to actually take the limit.  Would you object if we defined $\hat{G}$ to be the cofiltered diagram consisting of all finite quotients of $G$, and then observed that, just as always for a profinite group, we could instead take the limit as a topological group?

[[Tim Porter|Tim]]:  That was what I was hinting at in (iii).  I think also that the universal property is not yet in its optimal form as it mixes topological ond non-topological things too much. I may try to put together a categorical formulation as a 'gloss' on this.
=-- {: .query}


More formally, we note that for any group $G$, the family of its normal finite index subgroups forms a [[filtered category|cofiltered category]] under inclusion. (Denote it by $\Omega_G$.)  The assignment of $G/N$ to $N$ gives a functor from  $\Omega_G^{op}$ to the category of finite groups. It is thus a [[profinite group]] in the sense given in that entry, i.e. a [[pro-object]] in the category of finite groups. This pro-object is the profinite completion of $G$.  

The above topological version of this, with which we started, is obtained by means of the equivalence between the category of pro-(finite groups) and that of the groups internal to profinite spaces  that is by taking the limit in the category of topological groups of the diagram of (discrete) finite groups that the above construction gives one.


+-- {: .num_remark}
###### Remark


The inclusion [[functor]] $inc$ from the category, $FinGrps$, of finite groups, into that of groups does not have a [[left adjoint]].  It does have a left *pro-adjoint*, that is to say, it induces a functor on [[procategories]]

$$
  pro\!-\!inc : pro\!-\! FinGrps\to pro\!-\Grps
$$

and that functor _does_ have a left adjoint. If we restrict that 'pro-adjoint' to the subcategory of $pro\!-\! FinGrps$ given by the 'constant' pro-objects, then the result is the pro-finite completion construction that is given above. Because of this, if we think of the natural functor $C\to pro\!-\! C$ to be an inclusion, i.e. think of an object as a pro-object indexed by the one arrow category, we can give a [[universal property]] for the pro-finite completion of a group $G$. This universal property gives a universal cone from $G$  to finite groups, and just encodes the obvious fact that any homomorphism from $G$ to a finite group factors through one of its finite quotient groups. If we write $\hat{G}$ for the pro-finite completion, the universal cone is a map $G\to \hat{G}$ in $pro\!-\! FinGrps$.


=--

### Pro-$\mathcal{C}$ completion of a group

Let $\mathcal{C}$ be any class of [[finite groups]] that is closed under the formation of [[subgroups]], homomorphic [[images]] and [[group extensions]].


+-- {: .num_defn}
###### Definition

A _pro-$\mathcal{C}$ group_ is an [[inverse limit]] of an inverse system of groups in the class $\mathcal{C}$ or alternatively a [[pro-object]] in the full subcategory $\mathcal{C}$ determined by the class $\mathcal{C}$.

=--

 
The subcategory of $pro\!-\!FinGrps$ consisting of the pro-$\mathcal{C}$ groups and the continuous homomorphisms between them will be denoted $pro\!-\!\mathcal{C}$. 

This notation now has two definitions, but, as the corresponding categories are equivalent, this causes no problem.  

The categories of the form $pro\!-\!\mathcal{C}$ form [[varieties]] in $prof-FinGrps$.  Recall that a [[variety]] in any algebraic context means a subcategory of 'algebras' closed under products, subobjects and quotients.  We note the condition on $\mathcal{C}$ implies the closure of $\mathcal{C}$ under finite products, so $\mathcal{C}$ is what is called a _pseudovariety_.  The category $pro\!-\!FinGrps$ is [[monadic]] over the category of spaces. This means that free objects exist in all the $pro\!-\!\mathcal{C}$.  A good reference for this is Gildenhuys and Kennison, (1971), see below.




## Examples

+-- {: .num_example}
###### Example

Consider the profinite completion of the 
[[fundamental group]] of an complex [[projective variety]] $X$. Since $X$ has an underlying [[topological space]], its [[fundamental group]] of loops $\pi_1^{top}(X)$ can be defined in the usual way. But one can also define the [[algebraic fundamental group]] $\pi_1^{alg}(X)$. This is a profinite group, which is isomorphic to the profinite completion of $\pi_1^{top}(X)$.

=--

+-- {: .num_example}
###### Example

The profinite completion of the [[integers]] is

$$
  \widehat {\mathbb{Z}} \coloneqq \underset{\leftarrow}{\lim}_n \mathbb{Z}/n\mathbb{Z}
  \,.
$$

This is [[isomorphism|isomorphic]] to the [[product]] of the [[p-adic integers]] for all $p$

$$
  \widehat{\mathbb{Z}} \simeq \underset{p}{\prod} \mathbb{Z}_p
  \,.
$$

For more on this see at _[[p-adic integers]]_, at _[[adele]]_ and _[[idele]]_.

=--





## Related concepts

### Profinite completion of spaces

* [[profinite completion of a space|Profinite completion of a space]].

(Beware there are two possible interpretations of this term. One is handled in the section above, being profinite completion of the homotopy type of a space.  The entry linked to here treats another more  purely topological concept.)

### Equational or monadic completions

Profinite completion of groups is a special case of a general process that 'completes' a category together with a 'forgetful functor' to some 'base' category, replacing it by a category which is equational/monadic over the base.

*  D. Gildenhuys and J. Kennison, _Equational completions, model induced 
triples and pro-objects_, J. Pure Applied Alg., 4, (1971), 317&#8211;346.

### Pro-finite completions of homotopy types.

Artin and Mazur in their lecture note on &#233;tale homotopy introduced a process of profinite completion, generalising that for groups in as much as the profinite completion of an Eilenberg-Mac Lane space having $G$ as fundamental group has the profinite completion og $G$ as _its_ fundamental group. (WARNING: This needs a bit more detail to make it true! so this part of the entry needs more work.) 



## References

*  L. Ribes and P. Zalesskii, 2000, _Profinite groups_ , volume 40 of _Ergebnisse der Mathematik und ihrer Grenzgebiete_. 3. Folge , Springer-Verlag, Berlin. 

* J. Dixon, M. du Sautoy, A. Mann and D. Segal, 1999, _Analytic pro-p groups_, volume 61 of Cambridge Studies in Advanced Mathematics , Cambridge Univ. Press. 





[[!redirects profinite completion]]