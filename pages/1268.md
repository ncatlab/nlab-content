#Definition#

A _D-module_ is a [[abelian sheaf|sheaf]] of [[module]]s over the [[sheaf]] $D_X$ of [[regular differential operator]]s on a 'variety" $X$ (the latter notion depends on whether we work over a scheme, manifold, analytic complex manifold etc.). As $O_X$ is a subsheaf of $D_X$ consisting of the constant differential operators (multiplications by the sections of structure sheaf), every $D_X$-module is an $O_X$-module, and (quasi)coherence of $D_X$-modules implies the (quasi)coherence od a $D_X$-module just as $O_X$-module (but not viceversa). 

#Meaning and usage#

D-modules are useful as a means of applying the methods of [[homological algebra]] and [[Categories and Sheaves|sheaf theory]] to the study of analytic systems of partial differential equations.

In as far as an $O$-modules on a [[ringed site]] $(X, O)$ can be interpreted as a generalization of the [[sheaf]] of sections of a vector bundle on $X$, a D-module can be interpreted as a generalization of the [[sheaf]] of sections of a vector bundle on $X$ _with flat [[connection]]_ $\nabla$: 

the action of the differential operation given by a vector field $v$ on $X$ on a section $\sigma$ of the sheaf (over some patch $U$) is to be thought of as the covariant derivative $\sigma \mapsto \nabla_v \sigma$ with respect to the flat connection $\nabla$. 

In fact when $X$ is a complex analytic manifold, any $D_X$-module which is coherent as $O_X$-module is isomorphic to the sheaves of sections of a holomorphic vector bundle with flat connection. Furthermore, the subcategory of nonsingular $D_X$-modules coherent as $D_X$-modules is equivalent to the category of [[local system]]s.

#Related entries#

D-modules are closely related to

* [[local system]]s

#References#

* Bernstein's [notes](http://www.math.uchicago.edu/~arinkin/langlands/Bernstein/Bernstein-dmod.pdf)
* Schneiders' [notes](http://www.analg.ulg.ac.be/jps/rec/idm.pdf)
* Mili&#269;i&#263;'s [notes](http://www.math.utah.edu/~milicic/dmodules.pdf)

#Blog discussion#

* Secret Blogging Seminar [Musings on D-modules](http://sbseminar.wordpress.com/2007/07/07/musings-on-d-modules/), [Musings on D-modules, part 2](http://sbseminar.wordpress.com/2007/07/14/musings-on-d-modules-part-2/)

* The Everything Seminar [D-module Basics I](http://cornellmath.wordpress.com/2007/09/06/d-module-basics-i/), [D-Module Basics II](http://cornellmath.wordpress.com/2007/09/09/d-module-basics-ii/).

