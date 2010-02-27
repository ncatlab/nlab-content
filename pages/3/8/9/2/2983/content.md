A **building** (also **Tits building**, **Bruhat--Tits building**) is a combinatorial and geometric structure which simultaneously generalizes certain aspects of [[flag manifold]]s, finite [[projective plane]]s, and [[Riemannian manifold|Riemannian]] [[symmetric space]]s.

Initially introduced by [[Jacques Tits]] as a means to understand the structure of [[exceptional Lie group]]s, the theory has also been used to study the geometry and topology of [[homogeneous space]]s of p-adic Lie groups and their discrete subgroups of symmetries, in the same way that [[tree]]s have been used to study [[free group]]s.


> (for the moment the above text is simply a copy of the intro of the [wikipedia entry](http://en.wikipedia.org/wiki/Building_%28mathematics%29))

See also

* [[toddtrimble:Buildings for category theorists]] 


[[!redirects Tits building]]
[[!redirects Bruhat-Tits building]]
[[!redirects Bruhat–Tits building]]
[[!redirects Bruhat--Tits building]]

####Introductory references#### 

For a short, gentle and geometrical introduction, see:

* [[John Baez: This Week's Finds in Mathematical Physics, [week 263] (http://math.ucr.edu/home/baez/week263.html) second half.]] 

An introductory textbook that starts with explaining Coxeter groups is this:

* [[Abramenko, Peter; Brown, Kenneth S.: Buildings. Theory and applications. (Springer 2008, [ZMATH entry] (http://www.zentralblatt-math.org/zmath/en/advanced/?q=an:pre05288866&format=complete) )]]

####Introduction####
This page is intended to be a supplementary exposition of the page [[toddtrimble:Buildings for category theorists]], at least for now. So we will try to explain the aspects of buildings that the kind reader would like to now in order to understand the category theoretic construction over there.
The notion of a building relies heavily on that of a Coxeter group, which we will not explain here, see for example

* [[Wikipedia: [Coxeter groups] (http://en.wikipedia.org/wiki/Coxeter_group) ]]

and especially, for an elementary and readable introduction,

* [[Humphreys, James E.: Reflection groups and Coxeter groups.(Cambridge Studies in Advanced Mathematics 29, 1990, [ZMATH entry] (http://www.zentralblatt-math.org/zmath/en/advanced/?q=an:0725.20028&format=complete
) )]]

Taking the notion of Coxeter groups for granted, there are currently three different viewpoints of thinking about a building. 
From now on, let W be a Coxeter group and S the set of generators, which may be finite or infinite: In case we need S to be finite we will mention it explicitly.

####Buildings from three Viewpoints####
The three viewpoints are distinguished by how one thinks about chambers.

#####Simplicial Complexes#####
In Tits original approach, a building is a simplicial complex satisfying additional axioms. Chambers are maximal simplices.

#####Combinatorial Approach#####
This more modern approach originated with

* [Jaques Tits: A local approach to buildings, The geometric vein (C. Davis, B.Gr&#252;nbaum, and F. A. Sherk, eds.), Springer-Verlag, New York, 1981, pp. 519&#8211;547.]

Buildings are viewed as sets of chambers with a Coxeter-group-valued distance function satisfying certain axioms. Chambers are elements of an abstract set - more is not needed in the definition. As an alternative, chambers can be viewed as vertices of a graph. This is the point of view we will expand in future versions of this page.

#####Buildings as Metric Spaces#####
The following paper

* [M. W. Davis, Buildings are CAT(0), Geometry and cohomology in group theory
(P. H. Kropholler, G. A. Niblo, and R. St&#168;ohr, eds.), London Mathematical
Society Lecture Note Series, vol. 252, Cambridge University Press, Cambridge,
1998, pp. 108&#8211;123.]

explains that every building has a geometric realization that admits a CAT(0) metric, which means that it has metric properties analogous to those of complete simply connected Riemannian manifolds of nonpositive curvature.

* [Wikipedia: [CAT(k) spaces] (http://en.wikipedia.org/wiki/CAT%28k%29_space)]

From this viewpoint chambers a metric spaces.