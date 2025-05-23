
> This entry is supposed to be a survey of and motivation for the role of [[fiber bundles]] in [[physics]].

***

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Physics
+-- {: .hide}
[[!include physicscontents]]
=--
#### Bundles
+-- {: .hide}
[[!include bundles - contents]]
=--
=--
=--



#Fiber Bundles in Physics#
* table of contents
{:toc}

## Idea
 {#Idea}


\begin{imagefromfile}
    "file_name": "WuYang-PhysicsBundlesDictionary.jpg",
    "float": "right",
    "width": 600,
    "unit": "px",
    "margin": {
        "top": -40,
        "bottom": 20,
        "right": 0, 
        "left": 10
    },
    "caption": "(from [Wu and Yang 1975](#WuYang75), cf. [Yang 2009](https://www.youtube.com/watch?v=6d3hZ8jnqXg&t=2337s))"
\end{imagefromfile}


All of [[physics]] has two aspects: a local or even [[infinitesimal object|infinitesimal]] aspect, and a global aspect. Much of traditional lore deals just with the local and infinitesimal aspects -- the _[[perturbative field theory|perturbative]]_ aspects -- and [[fiber bundles]] play little role there. But they are the all-important structure that govern the global -- the _[[non-perturbative field theory|non-perturbative]]_ -- aspects. [[bundles|Bundles]] are the _global_ structure of [[physical fields]] and they are irrelevant only for the crude local and perturbative description of reality.

##  Basic idea of the definition of fiber bundles
 {#BasicIdeaOfDefinition}

One way to think of fiber bundles is that they are the data to _globally twist functions_ (on [[spacetime]], say) where "global twist" is much in the sense of "global [[anomaly]]" and the like, namely an effect visible on topologically nontrivial spaces when moving around non-contractible cycles. The concept of _[[monodromy]]_ -- which may be more familiar to physicists -- is closely related: monodromy is something exhibited by a [[connection on a bundle]] and specifically by a [[flat connection|flat bundle]]. For a [[discrete group|discrete]] structure group ([[gauge group]]) _every_ bundle is flat, and in this case non-trivial bundles and non-trivial [[monodromy]] come down to essentially the same thing (see also at _[[local system]]_).

More explicitly, suppose $X$ denotes [[spacetime]] and $F$ denotes some space that one wants to map into. For instance $F$ might be the [[complex numbers]] and a [[free field|free]] [[scalar field]] would be a [[function]]  $X\to F$. For the following it is useful to talk about functions a bit more indirectly: observe that the [[projection]] $pr_2 \colon F \times X \to X$ from the [[product]] of $F$ with $X$ down to $X$ is such that a [[section]] of this map, namely a $\Phi \colon X \to X\times F$ such that

$$
  pr_2 \circ \Phi = id_X
  \phantom{AAAAA}
  \array{
     && F \times X
     \\
     &
     {}^{\mathllap{\Phi}}\nearrow
     & \downarrow\mathrlap{pr_2}
     \\
     X &=& X
  }
$$

is just the same data as a function $X \to F$. We think of the projection $X \times F \overset{pr_2}{\to} X$ as encoding the fact that there is one copy of $F$ associated with each point of $X$, and think of a function with values in $F$ as something that, of course, takes values in $F$ over each point of $X$. One says that this projection, suggestively shown vertically,

$$
  \array{
    F \times X
    \\
    \downarrow\mathrlap{pr_2}
    \\
    X
  }
$$ 

is the _[[trivial bundle|trivial]]_ $F$-[[fiber bundle]] over $X$. 

If $F$ is equipped with the [[structure]] of a [[vector space]] then one calls this a _[[trivial vector bundle|trivial]] [[vector bundle]]_, etc.

The point being that more generally we may add a global "twist" to the $F$-valued functions by making the space $F$ vary to some degree as we move along $X$. For a [[fiber bundle]] one requires that it doesn't change _much_: in fact the word "fiber" in "[[fiber bundle]]" refers to the fact that _all_ fibers (over all points of $X$) are _[[equivalence|equivalent]]_. But the point is that any $F$ may be equivalent to _itself_ in more than one way (it may have "[[automorphisms]]"), and this allows non-trivial global structure even though all fibers look alike.

In this sense, a general $F$-[[fiber bundle]] on some $X$ is defined to be a [[space]] $P$ equipped with a map 

$$
  \array{
     P
     \\
     \downarrow \mathrlap{fb}
     \\ 
     X
  }
$$ 

to the base space $X$ (e.g. to spacetime), such that _locally_ it looks like the trivial $F$-fiber bundle, up to equivalence. 

To say this more technically: $P \overset{fb}{\to} X$ is called an $F$-[[fiber bundle]] if there exists a [[cover]] ([[open cover]]) of $X$ by patches (e.g. [[coordinate charts]]!) $U_i \to X$ for some index [[set]] $I$, such that for each patch $U_i$ (with $i \in I$) there exists a fiberwise [[equivalence]] between the restriction $P|_{U_i}$ of $P$ to $U_i$, and the trivial $F$-fiber bundle $F\times U_i \to U_i$ over the patch $U_i$.

To say this again in terms of sections: this means that a [[section]] $\Phi$ of $P \overset{fb}{\to} X$ 

$$
  fb \circ \Phi = id_X
  \phantom{AAAAA}
  \array{
     && P
     \\
     &
     {}^{\mathllap{\Phi}}\nearrow
     & \downarrow\mathrlap{fb}
     \\
     X &=& X
  }
$$


is locally on each ([[coordinate chart|coordinate]]) patch $U_i$ simply an $F$-valued function, but when we change patches (change coordinates) then there may be a non-trivial identifications (notably: [[gauge transformations]]) that relates the values of the function on one patch to that on another patch, where they overlap.

Even if this may seem a bit roundabout on first sight, this is actually something at the very heart of modern physics, in that it embodies the two central principles of modern physics, namely

1. the _principle of locality_;

1. the _gauge principle_.

The first roughly says that every global phenomenon in physics must come from local data. In the above discussion this means that any "globally $F$-valued thing on spacetime $X$" must come from just $F$-valued functions on local (coordinate) charts $U_i \hookrightarrow X$ of spacetime. BUT -- and this is key now --, second, the _gauge principle_ says that we may never strictly identify any two phenomena in physics (neither locally nor globally) but we must always ask instead for [[gauge transformations]] connecting two maybe seemingly different phenomena. Hence combining the gauge principle with the locality principle means that if an $F$-valued something on spacetime is locally given by plain $F$-valued functions, then it should be globally given by gluing these $F$-valued functions together not by _identification_ but by [[gauge equivalence]]. The result may be a structure that has global twists, and the nature of these global twists is precisely what an $F$-fiber bundle embodies.





## Examples of fiber bundles in physics

For instance the [[gauge fields]] in [[Yang-Mills theory]], hence in [[electromagnetism]], in [[QED]] and in [[QCD]], hence in the [[standard model of particle physics|standard model of the known universe]], are not really just the local [[differential 1-forms]] "$A_\mu^a$" known from so many textbooks, but are _globally_ really [[connections on principal bundles]] (or their [[associated bundles]]) and this is all-important once one passes to [[non-perturbative field theory|non-perturbative]] [[Yang-Mills theory]], hence to the full story, instead of its infinitesimal or local approximation.

Notably what is called a _[[Yang-Mills instanton]]_ in general and the _[[QCD instanton]]_ in particular is nothing but the underlying nontrivial class of the principal bundle underlying the Yang-Mills [[gauge field]]. Specifically, what physicists call the _[[instanton number]]_ for [[special unitary group|SU(2)]]-[[gauge field theory]] in 4-dimensions is precisely what mathematically is called the [[Chern class|second Chern-class]], a "[[characteristic class]]" of these gauge bundles.

> _YM Instanton = class of principal bundle underlying the non-perturbative gauge field_

To appreciate the utmost relevance of this, observe that the non-perturbative vacuum of the [[experiment|observable world]] is a "sea of instantons" with about one [[Yang-Mills instanton|YM instanton]] per [[femtometer]] to the 4th. See for instance the first sections of ([Schaefer-Shuryak 98](instanton+in+QCD#SchaeferShuryak98))
for a review of this fact. So the very substance of the physical world, the very vacuum that we inhabit, is all controled by non-trivial fiber bundles and is inexplicable without these.

Also [[monopole]] solutions in physics are mathematically nontrivial [[principal bundles]]. For instance the [[Dirac monopole]] (that appears in [[Dirac charge quantization]]) or the [[Yang monopole]].

Similarly [[fiber bundles]] control all other [[topology|topologically]] non-trivial aspects of [[physics]]. For instance most [[quantum anomalies]] are the statement that what looks like an [[action functional|action]] _[[function]]_ to feed into the [[path integral]], is globally really the [[section]] of a non-trivial bundle -- notably a [[Pfaffian line bundle]] resulting from the [[fermionic path integrals]]. Moreover _all_ [[classical anomalies]] are statements of nontrivializability of certain fiber bundles. 

Indeed, as the discussion there shows, [[quantization]] as such, if done [[non-perturbative field theory|non-perturbatively]], is all about lifting [[differential form]] data to [[line bundle]] data, this is called the _[[prequantum line bundle]]_ which exists over any globally quantizable [[phase spaces]] and controls all of its [[quantum theory]]. It reflects itself in many [[central extensions]] that govern [[quantum physics]], such as the [[Heisenberg group]] central extension of the Hamiltonian translation and generally and crucially the [[quantomorphism group]] central extension of the [[Hamiltonian diffeomorphisms]] of [[phase space]]. All these [[central extensions]] are non-trivial fiber bundles, and the "quantum" in "quantization" to a large extent a reference to the discrete (quantized) [[characteristic classes]] of these bundles. One can indeed understand quantization as such as the lift of infinitesimal classical differential form data to global bundle data. This is described in detail at _[quantization -- Motivation from classical mechanics and Lie theory](quantization#MotivationFromClassicalMechanicsAndLieTheory)_.

But actually the role of fiber bundles reaches a good bit deeper still. Quantization is just a certain [[extension]] step in the general story, but already [[classical field theory]] cannot be understood globally without a notion of bundle. Notably the very formalization of what a _[[field (physics)|classical field]]_ really is says: a [[section]] of a _[[field bundle]]_. For instance the global nature of [[spinors]], hence _[[spin structures]]_ and their subtle effect on [[fermion]] physics are all encoded by the corresponding [[spinor bundles]]. 

Two aspects of bundles in physics come together in the theory of [[gauge fields]] and combine to produce [[fiber infinity-bundle|higher fiber bundles]]: namely we saw above that a [[gauge field]] is itself already a bundle (with a [[connection on a bundle|connection]]), and hence the bundle of which a gauge field is a section has to be a "second-order bundle". This is called _[[gerbe]]_ or _[[principal 2-bundle|2-bundle]]_: the only way to realize the [[Yang-Mills field]] both locally and globally accurately is to consider it as a section of a bundle whose typical fiber is $\mathbf{B}G$, the universal [[moduli stack]] of $G$-[[principal bundles]]. For more on this see on the nLab at _[The traditional idea of field bundles and its problems](field%20%28physics%29#IdeaOfFieldBundlesAndItsProblems)_.

All of this becomes even more pronounced as one digs deeper into _[[local quantum field theory]]_, with locality formalized as in the [[cobordism hypothesis|cobordism theorem]] that classifies local [[topological field theories]]. Then already the [[local Lagrangians]] and [[local action functionals]] themselves are [[principal infinity-connection|higher connections]] on higher bundles over the [[moduli infinity-stack|higher moduli stack]] of fields. For instance the fully local formulation of [[Chern-Simons theory]] exhibits the Chern-Simons [[action functional]]  --- with all its global [[gauge invariance]] correctly realized -- as a [[universal Chern-Simons circle 3-bundle]]. This is such that by [[transgression]] to lower [[codimension]] it reproduces all the global gauge structure of this field theory, such as in codimension 2 the _[[WZW gerbe]]_ (itself a fiber 2-bundle: the [[background gauge field|background]] [[B-field]] of the [[WZW model]]!), in codimension 1 the [[prequantum line bundle]] on the [[moduli space of connections]] whose sections in turn yield the [[Hitchin connection|Hitchin bundle]] of [[conformal blocks]] on the [[moduli space of Riemann surfaces]].

And so on and so forth. In short: all global structure in [[field theory]] is controled by [[fiber bundles]], and all the more the more the field theory is [[quantum field theory|quantum]] and [[gauge field theory|gauge]]. The only reason why this can be ignored to some extent is because field theory is a complex subject and maybe the majority of discussions about it concerns really only a small little perturbative local aspect of it. But this is not the reality. The [[QCD]] [[vacuum]] that we inhabit is filled with a sea of non-trivial bundles and the whole quantum structure of the laws of nature are bundle-theoretic at its very heart.
 
## Related concepts

* [[Aharonov-Bohm effect]]

* [[geometry of physics]]

* [[twisted smooth cohomology in string theory]]

* [[motivation for sheaves, cohomology and higher stacks]]

* [[higher category theory and physics]]

* [[string theory FAQ]]

* [[motivation for higher differential geometry]]

* [[applications of (higher) category theory]]

* [[motivation for cohesion]]

* [[Hilbert's sixth problem]]

* [[motives in physics]]

* [[model theory and physics]]

* [[L-infinity algebras in physics]]


## References

> See also the references at _[[Dirac charge quantization]]_ at *[[gauge potential]]*.

The understanding of [[electromagnetic potentials]] as [[connection on a bundle|connections]] on [[fiber bundles]] originates with:

* {#WuYang75} [[Tai Tsun Wu]], [[Chen Ning Yang]], *Concept of nonintegrable phase factors and global formulation of gauge fields*, Phys. Rev. D **12** (1975) 3845 &lbrack;[doi:10.1103/PhysRevD.12.3845](https://doi.org/10.1103/PhysRevD.12.3845)&rbrack;

Further discussion and review:

* {#EguchiGilkeyHanson80} [[Tohru Eguchi]], [[Peter Gilkey]], [[Andrew Hanson]], _Gravitation, gauge theories and differential geometry_, Physics Reports **66** 6 (1980) 213-393 &lbrack;<a href="https://doi.org/10.1016/0370-1573(80)90130-1">doi:10.1016/0370-1573(80)90130-1</a>&rbrack;

* [[Aiyalam P. Balachandran]], [[Giuseppe Marmo]], [[Bo-Sture Skagerstam]], [[Allen B. Stern]]: *Gauge Symmetries and Fibre Bundles -- Applications to Particle Dynamics*, Lect. Notes in Physics **188** Springer (1983) &lbrack;[arXiv:1702.08910](https://arxiv.org/abs/1702.08910), [doi:10.1007/3-540-12724-0](https://doi.org/10.1007/3-540-12724-0)&rbrack;

* [[Aiyalam P. Balachandran]], [[Giuseppe Marmo]], [[Bo-Sture Skagerstam]]: *Classical Topology and Quantum States*, World Scientific (1991) &lbrack;[doi:10.1142/1180](https://doi.org/10.1142/1180)&rbrack;
  > (emphasis on [[solitons]], [[Skyrmions]] etc.)

* [[Chen Ning Yang]]: *Vector Potentials and Connections*, talk at 13th Annual Geometry Festival *Connections in Modern Mathematics and Physics*, Stony Brook University (April 1998) &lbrack;video:[YT](https://youtu.be/uaBVQe7w2Hs)&rbrack;

* L. Mangiarotti, [[Gennadi Sardanashvily]], _Connections in Classical and Quantum Field Theory_, World Scientific (2000) &lbrack;[doi:10.1142/2524](https://doi.org/10.1142/2524)&rbrack;


* Luciano Boi, _Geometrical and topological foundations of theoretical physics: From gauge theories to string program_, 2003 ([pdf](http://www.emis.de/journals/HOA/IJMMS/2004/33-361777.pdf))


* [[Mikio Nakahara]]: *[[Geometry, Topology and Physics]]*, IOP (2003) &lbrack;[doi:10.1201/9781315275826](https://doi.org/10.1201/9781315275826), <a href="http://alpha.sinp.msu.ru/~panov/LibBooks/GRAV/(Graduate_Student_Series_in_Physics)Mikio_Nakahara-Geometry,_Topology_and_Physics,_Second_Edition_(Graduate_Student_Series_in_Physics)-Institute_of_Physics_Publishing(2003).pdf">pdf</a>&rbrack;


* [[Dale Husemoeller]], [[Michael Joachim]], [[Branislav Jurco]], [[Martin Schottenloher]], _[[Basic Bundle Theory and K-Cohomology Invariants]]_,  Lecture Notes in Physics, Springer (2008) &lbrack;[pdf](http://www.mathematik.uni-muenchen.de/~schotten/Texte/978-3-540-74955-4_Book_LNP726corr1.pdf)&rbrack;

* [[Adam Marsh]]: _Gauge Theories and Fiber Bundles: Definitions, Pictures, and Results_ &lbrack;[arXiv:1607.03089](https://arxiv.org/abs/1607.03089)&rbrack;, chapter 10 in: [[Adam Marsh]], _Mathematics for Physics: An Illustrated Handbook_, World Scientific (2018) &lbrack;[doi:10.1142/10816](https://doi.org/10.1142/10816), [book webpage](https://www.mathphysicsbook.com/)&rbrack;

* {#RudolphSchmidt17} [[Gerd Rudolph]], [[Matthias Schmidt]], _Differential Geometry and Mathematical Physics: Part II. Fibre Bundles, Topology and Gauge Fields_, Theoretical and Mathematical Physics Series, Springer (2017) &lbrack;[doi:10.1007/978-94-024-0959-8](https://doi.org/10.1007/978-94-024-0959-8)&rbrack;

* [[Kirill Krasnov]], §1.12 in: *Formulations of General Relativity*, Cambridge Monographs on Mathematical Physics, Cambridge University Press (2020) &lbrack;[doi:10.1017/9781108674652](https://doi.org/10.1017/9781108674652), taster:[pdf](https://www.maths.nottingham.ac.uk/plp/pmzkk/book_taster.pdf)&rbrack;

* [[Roberto Percacci]]: *Non-Perturbative Quantum Field Theory -- An Introduction to Topological and Semiclassical Methods*, SISSA & ICTP (2024) &lbrack;[doi:10.22323/9788898587056](https://doi.org/10.22323/9788898587056), [pdf](https://library.oapen.org/bitstream/handle/20.500.12657/96025/9788898587056.pdf)&rbrack;


Specifically in [[solid state physics]] ([[valence bundles]] and their [[K-theory classification of topological phases of matter]]):

* [[Jérôme Cayssol]], [[Jean-Noël Fuchs]], *Topological and geometrical aspects of band theory*, J. Phys. Mater. **4** (2021) 034007 ([arXiv:2012.11941](https://arxiv.org/abs/2012.11941), [doi:10.1088/2515-7639/abf0b5](https://doi.org/10.1088/2515-7639/abf0b5))


category: motivation


[[!redirects fiber bundles and physics]]

  