#Contents#
* tic
{:toc}

+--{: .query}
This entry is about ( a fragment of) a paper by [[Anders Kock]]
=--

##Pregroupoids derived from a groupoid##
Let $G:=\{G_0\to G_1\}$ a groupoid, $A,B\subset G_0$ subsets.

Then the object $G(A,B)$ defined to be the set of arrows in $G_1$ whose source is in $A$ and whose target is in $B$ equipped with the two evident structure maps
$$s:G(A,B)\to A$$
$$t:G(A,B)\to B$$
is a [[heap|pregroupoid]]. If $A=B$ this is a full subgroupoid of $G$.

##Pregroupoid associated to a principal bundle##
Let $p:P\to A$ be a principal right $G$-bundle for a group $G$. Then the span $A\xleftarrow{p}P\xrightarrow{!} * $ is a pregroupoid.

##The category of pregroupoids##
There is a category $\mathbf{PGrpd}$ with pregroupoids as objects and triples $(c_0,c,c_1)$ of morphisms making
$$\array{A&\xleftarrow{a}&^X&\xrightarrow{b}&B\\ {}_{c_0}\downarrow&&{}_c\downarrow&&{}_{c_1}\downarrow\\A^\prime&\xleftarrow{a^\prime}&X^\prime&\xrightarrow{b^\prime}&B^\prime}$$
commute.

There is a forgetful functor
$$V:\begin{cases}Grpd\to PGrpd\\G\to G(G_0,G_0)\end{cases}$$

##Groupoids associated to a pregroupoid
There are three candidates of a groupoid associated to a pregroupoid: $PP^{-1}$, $P^{-1}P$ and $E(P)$. $PP^{-1}$ and $P^{-1}P$ are called edges of the pregroupoid $P$, since they appear as edges of some bisimplicial set. $E(P)$ is called enveloping groupoid for the pregroupoid $P$. $E(P)$ contains the edges of $P$ as subgroupoids.

###The Ehresmann groupoid $PP^{-1}$
For a pregroupoid $A\xleftarrow{\alpha} P\xrightarrow{\beta} B$ the **Ehresmann groupoid** $PP^{-1}$ is defined by $PP^{-1}_0:=A$ and 
$$PP^{-1}(a,a^\prime):=xy^{-1}:=\{(x,y)|\alpha(x)=a,\,\alpha(y)=a^\prime\}/\sim$$
where $(x,y)\sim(u,z)$ iff $u=xy^{-1}z$

###The ''inverse Ehresmann'' groupoid $PP^{-1}$
For a pregroupoid $A\xleftarrow{\alpha} P\xrightarrow{\beta} B$ the **''inverse Ehresmann'' groupoid** $P^{-1}P$ is defined by $P^{-1}P_0:=B$ and 
$$P^{-1}P(b,b^\prime):=y^{-1}z:=\{(y,z)|\beta(y)=b,\,\alpha(z)=b^\prime\}/\sim$$
where $(y,z)\sim(x,u)$ iff $u=xy^{-1}z$

If $P$ is a principal $G$-bundle, the groupoid $P^{-1}P$ is canonically isomorphic to the one object groupoid $G$ by
$$\begin{cases}P^{-1}P\to G\\(y^{-1}z:y\to z)\to g,&yg=z\end{cases}$$

##The enveloping groupoid $E(P)$

Let $A\xleftarrow{\alpha} P\xrightarrow{\beta} B$ be a pregroupoid.

The **enveloping groupoid $E(P)$ for $P$** is defined by $E(P)_0:=A\coprod B$ and $E(P)_1:=PP^{-1}\coprod P^{-1}P\coprod P\coprod P^{-1}$, where $P^{-1}$ denotes the pregroupoid $P$ with $\alpha$ and $\beta$ interchanged. And calculations (see [arxiv](http://home.imf.au.dk/kock/pbgc4.pdf) p.9) show that this is a groupoid.

##Properties

* The edges of $P$ act on $P$ principally on the left and the right, respectively and the actions commute with each other.

* Let $p:P\to A$ be a principal $G$ bundle. Then there is a groupoid $E$ with $E_0=A\coprod *$ and $E_1=P$. In this cases $G=E(*,*)$

* The functor $E(-):PGrdp\to Grpd$ is a faithful left adjoint to the forgetful functor $V$, the unit for the adjunction is injective.

##References
Anders Kock: 

* Principal bundles, groupoids and connections ([arxiv](http://home.imf.au.dk/kock/pbgc4.pdf)),