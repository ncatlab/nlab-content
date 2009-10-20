#Contents#
* automatic table of contents goes here
{:toc}

#Definition#

A _D-module_ is a [[abelian sheaf|sheaf]] of [[modules]] over the [[sheaf]] $D_X$ of [[regular differential operators]] on a 'variety' $X$ (the latter notion depends on whether we work over a [[scheme]], [[manifold]], analytic complex manifold etc.). As $O_X$ is a subsheaf of $D_X$ consisting of the zeroth-order differential operators (multiplications by the sections of structure sheaf), every $D_X$-module is an $O_X$-module.  Moreover, the (quasi)coherence of $D_X$-modules implies the (quasi)coherence of a $D_X$-module regarded as an $O_X$-module (but not vice versa). 

#Meaning and usage#

$D$-modules are useful as a means of applying the methods of [[homological algebra]] and [[Categories and Sheaves|sheaf theory]] to the study of analytic systems of partial differential equations.

Insofar as an $O$-module on a [[ringed site]] $(X, O)$ can be interpreted as a generalization of the [[sheaf]] of sections of a vector bundle on $X$, a D$-$module can be interpreted as a generalization of the [[sheaf]] of sections of a vector bundle on $X$ _with flat [[connection]]_ $\nabla$.  The idea is that the action of the differential operation given by a vector field $v$ on $X$ on a section $\sigma$ of the sheaf (over some patch $U$) is to be thought of as the covariant derivative $\sigma \mapsto \nabla_v \sigma$ with respect to the flat connection $\nabla$. 

In fact when $X$ is a complex analytic manifold, any $D_X$-module which is coherent as $O_X$-module is isomorphic to the sheaf of sections of some holomorphic vector bundle with flat connection. Furthermore, the subcategory of nonsingular $D_X$-modules coherent as $D_X$-modules is equivalent to the category of [[local systems]].

If $X$ is a variety over a field of positive characteristic $p$, the terms "$O_X$-coherent $D_X$-module" and "vector bundle with flat connection" are not interchangeable, since $D_X$  no longer is the enveloping algebra of $O_X$ and $\text{Der}_X(O_X,O_X)$. A theorem by Katz states that for smooth $X$ the category of $O_X$-coherent $D_X$-modules is equivalent to the category with objects sequences $(E_0, E_1,\ldots)$ of locally free $O_X$-modules together with $O_X$-isomorphisms $\sigma_i: E_i\rightarrow F^* E_{i+1}$, where $F$ is the Frobenius endomorphism of $X$.

+-- {: .query}

[[John Baez]]: it would be nice to have a little more explanation about how not every $D$-module that is coherent as an $O$-module is coherent as a $D$-module.  If I understand correctly, this may be the same question as how not every holomorphic vector bundle with flat connection is a local system.  Perhaps the answer can be found under [[local system]]?  Apparently not.  Perhaps the point is that not every flat connection on a holomorphic vector bundle is locally holomorphically trivializable?  If so, this is different than how it works in the $C^\infty$ category, which might explain my puzzlement.

=--

#Related entries#

D-modules are closely related to

* [[local systems]]

#References#

* Bernstein's [notes](http://www.math.uchicago.edu/~arinkin/langlands/Bernstein/Bernstein-dmod.pdf)
* Schneiders' [notes](http://www.analg.ulg.ac.be/jps/rec/idm.pdf)
* Mili&#269;i&#263;'s [notes](http://www.math.utah.edu/~milicic/Eprints/dmodules.pdf)
* Gieseker: Flat Vector Bundles and the Fundamental Group in Non-Zero Characteristics,  Ann. Scuola Norm. Sup. Pisa Cl. Sci. (4)  2  (1975), no. 1, 1--31. 

#Blog discussion#

* Secret Blogging Seminar [Musings on D-modules](http://sbseminar.wordpress.com/2007/07/07/musings-on-d-modules/), [Musings on D-modules, part 2](http://sbseminar.wordpress.com/2007/07/14/musings-on-d-modules-part-2/)

* The Everything Seminar [D-module Basics I](http://cornellmath.wordpress.com/2007/09/06/d-module-basics-i/), [D-Module Basics II](http://cornellmath.wordpress.com/2007/09/09/d-module-basics-ii/).


[[!redirects D-modules]]