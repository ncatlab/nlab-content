
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--

#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The term "local system" originally meant and means a _local system of coefficients for [[cohomology]]_. In that context a local system is a connective [[spectrum]] or some other coefficient [[topological space]] $A$ equipped with an [[action]] of the first [[fundamental group]] $\pi_1(X)$ of a given connected base space  $X$. The corresponding [[fibration sequence]] $A \to A//\pi_1(X) \to \mathbf{B}\pi_1(X)$ together with the canonical $\pi_1(X)$-cocycle $c : X \to \mathbf{B}\pi_1(X)$ on $X$ that classified the [[universal cover]] of $X$ define a notion of [[twisted cohomology]] with twist $[c]$. This is the "$A$-cohomology with local coefficients" for the given action. See [[twisted cohomology]] for details.

The term "local system" has developed a bit of life of its own independent of this application in [[twisted cohomology]]. Many authors understand under a local system just the representation of the [[fundamental groupoid]] of some space on some object. This is described in the following.

[[schreiber:Differential Nonabelian Cohomology|Recall]] that for $X$ a [[manifold]] and $P_1(X)$ its [[path groupoid]] (morphisms are thin-homotopy classes of smooth paths in $X$) and [[Vect]] the category of vector spaces, a suitably well-behaved [[functor]]

$$
  tra_\nabla : P_1(X) \to Vect
$$

is the same thing as a vector bundle $E \to X$ bundle with connection $\nabla$: the functor sends each point of $X$ to the fiber $E_x$ of $E$ over $x$, and sends each path $x \stackrel{\gamma}{\to} y$ to the _parallel transport_ 
$tra_\nabla(\gamma) : E_x \to E_y$
induced by the connection along the path.




Precisely when the connection $\nabla$ is _flat_ does the functor $tra_\nabla$ factor through 

$$
  h : P_1(X) \to \Pi_1(X)
$$

where $\Pi_1(X)$ is the [[fundamental groupoid]] of $X$, and where $h$ sends each smooth path to its homotopy class relative its endpoints.

Accordingly, vector bundles with _flat_ connection on $X$ are equivalent to functors from the [[fundamental groupoid]] to $Vect$

$$
  tra : \Pi_1(X) \to Vect
  \,.
$$

This notion now makes sense whether $X$ is equipped with a smooth structure or not. Moreover, the concept obviously generalizes to any other coefficient category $A$ replacing $Vect$. A functor

$$
  tra : \Pi_1(X) \to A
$$

may hence be thought of as defining an "$A$-bundle" with flat connection. And this is precisely what is called a _local system with coefficnets in $A$_.

If $I$ is some special object of $A$, such as a [[terminal object]], or a [[generator]] or a tensor unit if $A$ is [[monoidal category|monoidal]], then it makes sense to think of natural transformations

$$
  \sigma : const_I \to tra
$$

as a _flat section_ (or flat $I$-section) of the flat bundle given by $tra$.

In general there are few or none such sections on $X$, but for each subset $u \hookrightarrow X$ there is an obvious inclusion functor $i_U : \Pi_1(U) \hookrightarrow \Pi_1(X)$ and the pulled back functor $tra \circ i_U : \Pi(U) \to Vect$ in general has a nontrivial collection of sections when $U$ is small enough (in particular when $U$ is contractible).

This way  a functor $tra : \Pi_1(X) \to A$ induces a [[sheaf]] of flat $I$-sections on $X$

$$
  \Gamma_I(tra) : Op(X)^{op} \to C
  \,,
$$
where $C$ is the category over which $A$ is [[enriched category|enriched]],
and under mild conditions the functor $tra$ may be reconstructed up to isomorphism from its sheaf of $I$-flat sections.

The sheaves that arise this way from flat parallel transport functors are rather special, in particular they are locally constant. In large parts of the literature a _local system_ is defined to be such a locally constant sheaf, with some further condition on its stalks: if $A = Vect$ then flat sections form themselves a vector space and so do the stalks of the sheaf of flat section. In the sheaf theoretic literature a _local system_ is therefore usually assumed to have this property.

There are more or less obvious and straightforward generalizations of the notion of flat bundles and of local systems to much more general context. Notably the concept of a functor on the fundamental groupoid wants to generalize to that of an $\infty$-functor on a [[fundamental infinity-groupoid]] $\Pi(X) = \Pi_\infty(X)$.

For $A$ a suitable [[infinity-category]] therefore an $\infty$-functor

$$
  tra : \Pi(X) \to A
$$

may be regarded as a flat $\infty$-bundle on $X$. Examples are for instance higher gerbes with flat connection (see [[Deligne cohomology]] and more generally [[schreiber:Differential Nonabelian Cohomology|differential nonabelian cohomology]]).

Moreover, the space $X$ may itself be replaced by a [[motivation for sheaves, cohomology and higher stacks|generalized space]]: an [[infinity-stack]] (which may be a [[derived stack]]). Under mild assumptions there is still a notion of [[fundamental infinity-groupoid]] $\Pi(X)$ in the context of $\infty$-stacks and hence for $A$ any coefficient object in the relevant [[(infinity,1)-topos]], the $\infty$-category

$$
  [\Pi(X), A]
$$

maybe addressed as a derived category of local systems, or the like. More on this is at [[geometric infinity-function theory]] (under "basic ideas related to $\infty$-stacks") and at [[schreiber:Differential Nonabelian Cohomology|differential nonabelian cohomology]].

## Definitions

The notion of *local system* exists in several different forms, each trying to capture some basic intuition in an appropriate language  for the applications that are being considered. For the moment we will not enquire too deeply as to the exact relationships between them 


We start with a 'geometric' definition and then give the [[sheaf]]-theoretic one.

### Geometric definition ##

A **local system** on a topological space $X$ with coefficients in a category $A$ is a [[functor]]

$$
  tra : \Pi_1(X) \to A
$$

from the [[fundamental groupoid]] $\Pi_1(X)$ of $X$ to $A$. 
The category of local systems on $X$ with coefficients in $A$ is the [[functor category]]

$$
  [\Pi_1(X), A]
  \,.
$$

### History ##

In a paper

* Steenrod: _Homology with local coefficients_, Annals 44 (1943) pp. 610 - 627,

 an early version of this notion was given. 

This is before the formal notion of sheaf was published by Leray.  (Wikipedia's entry on [Sheaf theory](http://en.wikipedia.org/wiki/Sheaf_%28mathematics%29#History) is interesting for its historical perspective on this.)

A definition  in the above form appears in an exercise in 

* E. H. Spanier, 1966, Algebraic Topology , McGraw Hill. (republished by Springer, 1982).

on page 58 : 

>_A local system on a space $X$ is a covariant functor from the fundamental groupoid of $X$ to some category._

Some of the relationships with cohomology and sheaves are explored in various parts of the book.

#### Higher categorical geometric definition

For any notion of [[fundamental ∞-groupoid]] there is a corresponding notion of higher local system.

R. Brown and P. Higgins have discussed local systems for the [[fundamental ∞-groupoid]] $\Pi(X)$ realized as a  [[infinity-groupoid|strict ∞-groupoid]]. Since strict $\infty$-groupoids are equivalent to [[crossed complex]]es, in this context a higher local system 
$\Pi(X) \to A$
may be realized as a morphism of [[crossed complex]]es.

See

* [[Ronnie Brown]], P.J. Higgins, _Crossed complexes and chain complexes with operators_ Math. Proc. Camb. Phil. Soc., 107 (1990) 33-57.

* R. Brown, P.J Higgins, _The classifying space of a crossed
complex_, Math. Proc. Camb. Phil. Soc., 110 (1991) 95-120.

A categorification of local systems to (a bit nontrivial) notion of [[locally constant stack]]s is given in 

* [[Pietro Polesselo]], [[Ingo Waschkies]], Higher monodromy, Homology, Homotopy and Applications, Vol. 7(2005), No. 1, pp. 109-150;
[arXiv:0407507](http://arxiv.org/abs/math/0407507)

There is an another direction of categorifications of local systems (where roughly speaking the base is categorified) considered by M. Hopkins (unpublished). 


+-- {: .query}

  [[Urs Schreiber|Urs]]: I'd be interested in seeing more details of the definition by Hopkins. Does anyone know more?

=--
There is a very close relationship between this notion and sheaf theory. Locally constant sheaves play the role of locally trivial fibre bundles in the algebraic-geometric context, so the term 'local system' is used in this context in the following sense:

### Sheaf-theoretic definition


+-- {: .un_defn}
###### Definition

A **local system** is a [[locally constant sheaf]] on a [[topological space]] $X$ (or manifold, analytic manifold, or algebraic variety) whose stalk is a finite-dimensional vector space. 

=--

> well, in some areas it is assumed to take values in vector spaces, in other not 

+-- {: .un_lemma}
###### Lemma

On a connected topological space this is the same as a sheaf of sections of a finite-dimensional vector bundle equipped with flat connection; and it also corresponds to the [[representations]] of the [[fundamental group]] $\pi_1(X,x_0)$ in the typical stalk. On an analytic manifold or a variety, there is an equivalence between the category of non-singular coherent 
$D_X$-[[D-module|modules]] and local systems on $X$.
=--


##Examples

...

## Related entries

* [[simplicial local system]]: within Sullivan's (1977) theory of _Infinitesimal computations in topology_, he refers to 'local systems' several times. This seems to be simplicial in nature. [[simplicial local system|This]] entry explores some of the uses of that notion based on Halperin's lecture notes on minimal models

  * D. Sullivan, _Infinitesimal computations in topology_ ([pdf](http://archive.numdam.org/ARCHIVE/PMIHES/PMIHES_1977__47_/PMIHES_1977__47__269_0/PMIHES_1977__47__269_0.pdf))

* [[D-module]]

* [[abelian sheaf cohomology]]






## Expositions

A blog exposition of some aspects of local system is developed here:

* David Speyer: _Three ways of looking at a local system_

  * [Introduction and connection to cohomology theories](http://sbseminar.wordpress.com/2009/04/20/three-ways-of-looking-at-a-local-system-introduction-and-connection-to-cohomology-theories/)


  * [the path groupoid approach](http://sbseminar.wordpress.com/2009/04/21/local-systems-the-path-groupoid-approach/)

  * [the infinitesimal perspective](http://sbseminar.wordpress.com/2009/04/30/three-ways-of-looking-at-a-local-system-the-infinitesimal-perspective/)

  * [the infinitesimal site](http://sbseminar.wordpress.com/2009/05/06/the-infinitesimal-site/)

***


## A general picture {#nPOV}

+-- {: .query}

[[Urs Schreiber]]: I find the above entry so far a bit of a mess. It is lacking a good [[nPOV]] elegant global picture from which all the details then drop out automatically. Here is a proposal for what that could be.

=--

We try to give the general abstract [[nPOV]] on local systems.

In the context of a given [[(∞,1)-topos]] $\mathbf{H} = Sh_{(\infty,1)}(X)$ of [[∞-stack]]s on $C$, whose objects we think of as [[space]]s, for every [[object]] $X \in \mathbf{H}$ and [[pointed object]]$(* \to A) \in \mathbf{H}$,  a [[morphism]] $X \to A$ is a [[cocycle]] that [[homotopy fiber|classifies]] an $A$-[[principal ∞-bundle]] $P \to X$ over $X$.

A **local system** is the special case of this where, equivalently, 

* the [[principal ∞-bundle]] $P$ is like a [[covering space]] for $X$;

* the coefficient object $A$ is a [[constant ∞-stack]] on $C$ -- $A = LConst \mathcal{A}$ for some $\mathcal{A} \in \infty Grpd$;

* the [[homotopy fiber|classifying]] [[cocycle]] $X \to A$ exhibits an $\mathcal{A}$-valued [[locally constant ∞-stack]] on $X$.

Here a [[constant ∞-stack]] $A$ is an object in the image of

$$
  LConst : \infty Grpd \simeq PSh_{(\infty,1)}(*)
  \stackrel{const}{\to}
  PSh_{(\infty,1)}(C)
  \stackrel{L}{\to}
  Sh_{(\infty,1)}(X)
  \,,
$$

where $L$ is [[∞-stackification]]. If this has a [[left adjoint]] $\Pi \dashv LConst$ then $\Pi(X)$ is the bare geometric [[schreiber:path ∞-groupoid]] of $X$, and by the [[adjunction]] we have that $(A = LConst \mathcal{A})$-local systems are equivalent to [[(∞,1)-functor|∞-functors]] $\Pi(X) \to \mathcal{A}$:

$$
  Loc(X,A) = \mathbf{H}(X,A) \simeq \infty Grpd(\Pi(X), \mathcal{A})
  \,.
$$

With this the fourth characterization of an $\mathcal{A}$-valued local system on $X$ is:

* a [[representation]] of the [[schreiber:path ∞-groupoid]] $\Pi(X)$ on $\mathcal{A}$.

In the special case that $\mathcal{A} = Core{\infty FinGrpd}$ is the [[core]] of the [[(∞,1)-category]] of finite [[∞-groupoid]]s, $\mathcal{A}$-valued local systems on $X$ are precisely genuine [[locally constant ∞-stack]]s on $X$. Conversely,we may think of a local system as a generalization of a locally constant $\infty$-stack, which may take values in something richer than just finite $\infty$-groupoids.


### References

A comparatively clear-sighted description of the situation along the above lines is that in 

* [[Pietro Polesello]], [[Ingo Waschkies]], Higher monodromy, Homology, Homotopy and Applications, Vol. 7(2005), No. 1, pp. 109-150;
[arXiv:0407507](http://arxiv.org/abs/math/0407507)

for [[locally constant stack]]s on [[topological space]]s. The above formulation is pretty much the evident generalization of this to general [[(∞,1)-topos]]es.

## Discussion


This here is an old discussion on some previous version of the entry.

+-- {: .query}


  [[Urs Schreiber|Urs]]: I am hoping that maybe David Speyer, whose expositional blog entry is linked to below, or maybe somebody else would enjoy filling in some material here.

 [[Bruce Bartlett|Bruce]]: Could it perhaps be "On a  topological space (why do we need _connected_?) this is the same as a sheaf of _flat_ sections of a finite-dimensional vector _bundle_ equipped with flat connection;". I guess by "flat connection" in this general topological context we would mean simply a functor from the homotopy groupoid to the category of vector spaces?

[[Zoran ?koda]]: connected because otherwise you do not have 
even the same dimension of the typical stalk of teh lcoally constant sheaf. Maybe there is a fancy wording with groupoids avoiding this, but when you have a representation on a single space, you need connectedness. 

[[Ronnie Brown]] I do not have time to write more tonight but mention that there is a section of the paper 

* (with P.J.HIGGINS), "The classifying space of a crossed
complex",   Math. Proc. Camb. Phil. Soc. 110 (1991) 95--120.

on local systems, where a module over the fundamental groupoid of a space is regarded as a special case of a crossed complex. This seems convenient for the singular theories but has not been developed in a Cech setting. The homotopy classification theorem 

$$ [X, \mathcal{B}C] \cong [\Pi X_* ,C] $$

where $X_*$ is the skeletal filtration of the CW-complex $X$, $C$ is a crossed complex, and $\mathcal{B}C$ is the classifying space of $C$,  thus includes the local coefficient version of the classical Eilenberg-Mac Lane theory. 

[[Tim Porter|Tim]]:  Quoting an exercise in Spanier (1966) on page 58: 

_A local system on a space $X$ is a covariant functor from the fundamental groupoid of $X$ to some category._

A reference is given to a paper by Steenrod: _Homology with local coefficients_, Annals 44 (1943) pp. 610 - 627.

Perhaps the entry could reflect the origins of the idea. The current one seems to me to be much too restrictive. There are other applications of the idea than the ones at present indicated, although of course those are important at the moment. Reference to vector bundles is not on the horizon in Spanier!!!!.

Local systems with other codomains than vector spaces are used in rational homotopy theory.

[[Urs Schreiber|Urs]]: I am all in favor of emphasizing that "local system" is nothing but a functor from a fundamental groupoid. That's of course right up my alley, compare the discussion with David Ben-Zvi at the "[Journal Club](http://golem.ph.utexas.edu/category/2009/04/journal_club_geometric_infinit.html#c023324)". Whoever finds the time to write something along these lines here should do so (and  in clude in particular the reference Ronnie Brown gives above). 

BUT at the same time it seems to me that many practitioners will by defualt think of the explicitly sheaf-theoretic notion when hearing "local syetem" which the entry currently states. We should emphasize this explicitly, something like: "while in general a local system is to be thought of as a representation of a fundamental groupoid, often the term is understood exclusively in its realization within [[abelian sheaf]] theory as follows ..."

[[Tim Porter|Tim]]: How about wording such as:

In general a local system is defined to be ... (ref. Spanier (1966) and earlier Steenrod (1943).) .... . (Perhaps a classical example would help here.)

 A particularly important case of this is when the functor takes its values in the category of vector spaces or slightly more generally abelian groups.  For instance given a locally constant sheaf
on a manifold then there is naturally a local system that encodes valuable information in a neat way. In this entry we will primarily discuss this latter more restrictive sense, at least to start with. Later we will look at other applications and instances of the more general case.

(I tend to not use the word representation when functor is meant and I would discourage saying that a local system IS a locally constant sheaf of whatever, as they are very different types of stuff (I almost get the 'I spy evil' reaction when I see that!). 

[[Zoran Skoda]]: Keep both definitions, and say when they are equivalent, sheaf theoretic and fundamental group one. 
Why I favour the sheaf theoretic definition as primary is its generality: it works over a site, it is related to combinatorial versions (local system of cohomological coefficients on a simplicial complex or on a poset), as well as local systems on stratified spaces: I do not know how the fundamental group is defined in those cases to yield the same notion; and as aside issue I also do not know if there is a usage of local systems on topological spaces which are not linearly connected. Besides, representations of fundamental group in f.d. vector spaces have also another name: monodromies (monodromy representations).  

[[Urs Schreiber|Urs]]: it seems everybody is waiting for everybody else to make the first step. So I did it now. Please see the above changes and please feel free to improve as you see the need!

[[Tim Porter|Tim]]:  The usual meaning of 'primary' would be relating to time so Steenrod would have it there! Homology and cohomolgy with local coefficients is known from way back and 'local system' I thought was short for 'local system of coefficients'. I understand what you mean about generality but would disagree on your last comment.  Your objection to the version in Spanier seems to be that someone else thought of another name later, yet the sheaf theoretic definition is saying that local system is another name for a locally constant sheaf of f.d. v. spaces so .... . 

Can someone tell me how old the term 'monodromy' is?  I know that Ehresmann used it so perhaps Cartan?  I digress. 

The main aim should be to have a clear description of the idea and a definition or definitions with some discussion of their interrelationships.

[[Zoran Skoda]]: so how will you do the local system on a site ? For a general site with a terminal object it is hard to have a satisfactory notion of fundamental group (though it works for topoi -- with regular epi topology assumed) while locally free sheaf still makes sense: you can use a cover of terminal object. The word monodromy is usually associated to  the case of ordinary differential equations and Riemann-Hilbert problem, so I believe that it existed around 1900, though I may be wrong.  

[[Tim Porter|Tim]]:  My own approach would, I think, be to rephrase things along the line of standard treatments of descent theory from a simplicial viewpoint. I have not thought about this so this may get garbled a bit.  Classically you can do local systems on a triangulation of a manifold without reference to the fundamental group(oid), and again classically open covers of a manifold are linked to triangulations by the Cech nerve, (see [[simplicial local system]]. The analogue for a general topos would be a hypercovering (I suppose) so it should be feasible to adapt the definition to that setting. (This is probably either well known or wrong!) The fundamental group should be nowhere in sight.  Paths are not relevant in this, and, of course, locally constant sheaves or their generalisations _are_ just around the corner. (This is all analytic continuation but does not use paths only (generalisations of) open sets.)

Local system was, as I said earlier, originally short for 'local system of coefficients', I believe, i.e. for cohomology or homology.

My main point is that a local system is **not** the same as a locally constant sheaf.  It is more like a diagram defining such a sheaf, rather than the sheaf itself.  If that terminology is used then it is sloppy terminology.  This does not make it 'wrong', just like so much maths, 'systematic abuse of terminology', and it should only be  indulged in with great care and consideration. 



(Another case which is more serious, I likewise object to U(1)-gerbes being called just gerbes.  This is historically wrong, can confuse a beginning researcher, and also can have a devastating effect on the future of young researchers, when well known 'experts' insist, for instance, that 'nice' gerbes are all abelian,(implying that other types are uninteresting, nasty and unimportant) as that condemns workers in non-Abelian cohomology who study non-Abelian gerbes to lack of grant funding etc. (I know I have been there!!! so my vehemence is well founded.))

Your comment on monodromy reinforced my feeling about it.  I have not got Steenrod's paper, so wonder if it shows that he was aware of the link. His fibre bundles book was still in the future ... interesting historical question there.

[[Zoran Skoda]]: I like your comment and historical remarks (by the way, the present homological algebra books like Methods...by Gelfand-Manin (p.28) distinguishes homology coefficient systems (on simplicial sets) and cohomology coefficient systems (maybe some remark within [[simplicial local system]] is due). As far as using internal nerve of a (hyper)cover in arbitrary site (I emphasise site, not topos)
one can try defining fund. groupoid along such terms, that is implicit in the work of Pataraia on internal cosimplicial objects, which I never studied enough, and includes some conditions; in any case it does not look elementary to me.
As far as historical info we should keep looking for it (including original usage of "monodromy"); it is instructive and shows some curious geometrical insights in old papers. 
=--

[[!redirects local systems]]
