#Idea#

[[schreiber:Differential Nonabelian Cohomology|Recall]] that for $X$ a manifold and $P_1(X)$ its [[path groupoid]] (moprhisms are thin-homotopy classes of smooth paths in $X$) and [[Vect]] the category of vector spaces, a suitably well-behaved [[functor]]

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

If $I$ is some special object of $A$, such as a [[terminal object]], or a [[generator]] or a tensor unit if $A$ is [[monoidal]], then it makes sense to think of natural transformations

$$
  \sigma : const_I \to tra
$$

as a _flat section_ of the flat bundle given by $tra$.


(need to interrupt for a second...)


#Definitions and characterizations#

A __local system__ is a locally constant [[sheaf]] on a topological space $X$ (or manifold, analytic manifold, or algebraic variety) whose stalk is a finite-dimensional vector space. On a connected topological space this is the same as a sheaf of sections of a finite-dimensional vector space equipped with flat connection; and it also corresponds to the representations of the [[fundamental group]] $\pi_1(X,x_0)$ in the typical stalk. On an analytic manifold or a variety, there is an equivalence between the category of non-singular coherent $D_X$-[[D-module|modules]] and local systems on $X$.

+-- {: .query}

  [[Urs Schreiber|Urs]]: I am hoping that maybe David Speyer, whose expositional blog entry is linked to below, or maybe somebody else would enjoy filling in some material here.

 [[Bruce Bartlett|Bruce]]: Could it perhaps be "On a  topological space (why do we need _connected_?) this is the same as a sheaf of _flat_ sections of a finite-dimensional vector _bundle_ equipped with flat connection;". I guess by "flat connection" in this general topological context we would mean simply a functor from the homotopy groupoid to the category of vector spaces?

[[Zoran Škoda]]: connected because otherwise you do not have 
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
=--

#Examples#

...

#Related entries#

* [[D-module]]

* [[abelian sheaf cohomology]]

#References#

There is a starting thread (still little info) at

* David Speyer: _Three ways of looking at a local system_

  * [Introduction and connection to cohomology theories](http://sbseminar.wordpress.com/2009/04/20/three-ways-of-looking-at-a-local-system-introduction-and-connection-to-cohomology-theories/)


  * [Local systems: the path groupoid approach](http://sbseminar.wordpress.com/2009/04/21/local-systems-the-path-groupoid-approach/)


A categorification of local systems to (a bit nontrivial) notion of locally constant stacks is given in 

* P. Polesselo, I. Waschkies, Higher monodromy, Homology, Homotopy and Applications, Vol. 7(2005), No. 1, pp. 109-150;
[arXiv](http://arxiv.org/abs/math/0407507)

There is an another direction of categorifications of local systems (where roughly speaking the base is categorified) considered by M. Hopkins (unpublished). 