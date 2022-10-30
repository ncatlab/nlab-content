
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
=--
=--

# Contents
* automatic table of contents goes here
{:toc}

[[!redirects etendue]]
[[!redirects etendu]]

##Idea##

An **&#233;tendue** (also 'etendue', or 'etendu'; from French '&#233;tendue' (fem.) - _extent_) is a [[topos]] $\mathcal{Y}$ that locally looks like the category of sheaves on a space:
>Briefly, the slogan is that $\mathcal{Y}$ is locally a topological space. (Lawvere 1976, p.129)

##History##

Originally defined by [[A. Grothendieck]] in ([[SGA4]], p.482) as a topos $\mathcal{Y}$ that has a well-supported object $X$ such that the slice $\mathcal{Y}/X$ is equivalent to a sheaf topos on a topological space, the definition was generalized by [[Lawvere]] (1975a,1976) by dropping the spatiality of the slice and require only that $\mathcal{Y}/X$ is a [[localic topos]].

Several site characterizations of &#233;tendues are known which come in two flavors, the first being the cancellation property of having an 'all monic' site betraying the origin of the concept as a mild generalization of the concept of space, the second is tied to the 'groupoidalness' of the site. Both ideas were already present in SGA4.

&#201;tendues play an important role in Lawvere's approach to [[cohesion]] and the petit/[[gros topos]] distinction, where they provide one of the classes of [[petit toposes]] (generalized spaces). In this context, Lawvere (1989,1991) interprets the cancellative property of the site as enabling an interpretation of &#233;tendues as _categories of processes_. 

##Definition##

A topos $\mathcal{E}$ is called an _&#233;tendue_ if there is an object $X\in|\mathcal{E}|$ such that the (unique) $X\rightarrow 1$ is epic and the [[slice topos]] $\mathcal{E}/X$  is a [[localic topos]].[^fine]

[^fine]:  An epic $k:X\rightarrow Y$ induces a [[geometric morphism]] $k_\ast:\mathcal{E}/X\rightarrow \mathcal{E}/Y$ whose inverse image part, the change of base functor, $k^\ast:\mathcal {E}/Y\rightarrow\mathcal{E}/X$ is faithful, which means by definition that $k_\ast$ is a surjection, and if $Y=1$ one says that $\mathcal{E}/X$ _covers_ $\mathcal{E}$.

##Examples##

> The first example of an &#233;tendue seems to have been the [[space of moduli]] of algebraic curves, which is prevented from being globally a space due to the action of the [[Galois groups]] within each point. Yes, something vaguely reminiscent of particle spin is going on in such spaces, and the most naked form is that for any group G, the category $\mathcal{S}^G$ is an &#233;tendue with only one point! This is easily seen from the observations that $\mathcal{S}^G/G\cong\mathcal{S}^G$ and that $G\twoheadrightarrow 1$ where the last two $G$'s denote the regular representation.      (Lawvere 1976, pp.129-130)

##Properties##

* **Proposition**. A Grothendieck topos $\mathcal{Y}$ is an &#233;tendue iff there exists a [[site]] $(\mathcal{C}, J)$ for $\mathcal{Y}$ such that every morphism of $\mathcal{C}$ is monic.

* A Grothendieck topos is a Boolean &#233;tendue precisely if it satisfies the _internal [[axiom of choice]]_ (i.e. $(\quad)^X$ preserves epics for all objects $X$ ). An example of such a Boolean &#233;tendue would be $\mathcal{S}^G$ for $G$ a group.

##Related Concepts##
* [[localic topos]]
* [[petit topos]]
* [[gros topos]]


##References

* [[M. Artin]], [[A. Grothendieck]], [[J. L. Verdier]], _Th&#233;orie des Topos et Cohomologie Etale des Sch&#233;mas (SGA 4)_, Springer LNM vol.269 (1972).

* [[Peter Johnstone]], _Sketches of an [[Elephant]] II_, Oxford UP 2002, pp.769-775.

* [[F. William Lawvere]], _Qualitative Distinctions between some Toposes of Generalized Graphs_ , Cont. Math. **92** (1989) pp.261-299.

* [[F. William Lawvere]], _[[Some Thoughts on the Future of Category Theory]]_ , pp.1-13 in Springer LNM vol. 1488 (1991).

* [[F. William Lawvere]], _Variable sets etendu and variable structure in topoi_ , Lecture notes University of Chicago 1975.

* [[F. William Lawvere]], _Variable quantities and variable structures in topoi_ , pp.101-131 in Heller, Tierney (eds.), Algebra, Topology and Category Theory, Academic Press New York 1976. 

* [[F. William Lawvere]], _Axiomatic Cohesion_ , TAC **19** no. 3 (2007) pp.41-49. ([pdf](http://www.tac.mta.ca/tac/volumes/19/3/19-03.pdf))

* [[F. William Lawvere]], _[[Como lectures]]_, Ms. 2008. ([pdf](http://comocategoryarchive.com/Archive/temporary_new_material/FWLawvere-Cohesive-Toposes-Como-January-2008.pdf))