A _quiver_ is a free category on a [[directed graph]]. Given a directed graph $G$ with collection of vertices $G_0$ and collection of edges $G_1$, there is the free category $F(G)$ on the graph whose collection of objects coincides with the collection of vertices, and whose collection of morphisms consists of finite sequences of edges in $G$ that fit together head-to-tail. The composition operation in this free category is the concatenation of sequences of edges.

Here we taking advantage of the [[adjunction]] between [[Cat]] (the category of small categories) and [[DiGraph]] (the category of directed graphs).  Namely, any category has an underlying directed graph:

$$U : Cat \to DiGraph $$

and the left adjoint of this functor gives the free category on a directed graph:

$$F : DiGraph \to Cat $$

A [[representation]] of a quiver $Q = F(G)$ is a functor

$$R : Q \to Vect $$

Concretely, such a thing assigns a vector space to each vertex of the graph $G$, and a linear operator to each edge.  Representations of quivers are fascinating things, with connections to ADE theory, quantum groups, string theory, and more.

#Literature#

* Harm Derksen and Jerzy Weyman, [Quiver representations](http://www.ams.org/notices/200502/fea-weyman.pdf) _AMS Notices_, 2005.

* William Crawley-Boevy, [Lectures on quiver representations](http://www.amsta.leeds.ac.uk/~pmtwc/quivlecs.pdf).
 
* Alistair Savage, [Finite-dimensional algebras and quivers](http://www.arxiv.org/pdf/math/0505082), _Encyclopedia of Mathematical Physics_, eds. J.-P. Fran&#231;oise, G.L. Naber and Tsou S.T., Oxford, Elsevier, 2006, volume 2, pp. 313-320.

These references need to be cleaned up. There are also many more to be added.