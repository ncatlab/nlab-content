[[!redirects ?ech method]]
[[!redirects Čech method]]
[[!redirects Cech method]]
[[!redirects ?ech methods]]
[[!redirects Čech methods]]
[[!redirects Cech methods]]

#&#268;ech methods#
* automatic table of contents goes here
{:toc}

## Idea ##

The construction of &#268;ech homology used coverings of the space by families of open sets. The way the open sets overlap gives 'combinatorial' information on the space. 

This has been abstracted and extended to [[homotopy]] and also in the direction of algebraic geometry. This article aims to introduce some of the main ways this idea has interacted with some of the many themes in the nLab.

 
##History (&#268;ech 1930s)##



The term '[[Čech nerve|nerve of a covering]]' has been used from the  late 
1920s for a  construction that starts with a space and an open cover of it and builds a [[simplicial complex]]. 
Historically these data were organizes as a  [[simplicial complex]], rather than a [[simplicial set]]. The idea had been parallely worked out by [[Eduard Cech|Čech]] and P.S. Aleksandrov
so one often talks about Aleksandrov--&#268;ech (co)homology. There was an alternative approach described by Vietoris (1927), which led to what is known as [[Vietoris homology]]  There are separate entries in nlab for [[Cech homology|Čech homology]]
and [[Čech cohomology]]. The first is not exact, and so is  not really
a homology theory in the sense of Steenrod--Eilenberg axioms. It is also not the (Alexander--Spanier) dual of &#268;ech cohomology.  The two problems  can be avoided at the same time using coherent homotopy theory. The resulting homology is one which is exact.  It also is one that satisfies the wedge axiom, and then it is the unique such theory, nowadays sometimes called [[strong homology]] and in special cases it reduces to what was called [[Steenrod-Sitnikov homology]] (but which was originally constructed in a different way).



##Definitions##

Given a (compact) space $X$ and a finite open cover, $\alpha$, of $X$, we can
form a [[simplicial set]], $C(X,\alpha)$, called the *nerve of the cover* whose $n$-[[simplex|simplices]] are $(n + 1)$-strings
of open sets  from $\alpha$, i.e. $\langle U_0, \ldots, U_n\rangle$, each $U_i \in \alpha$,
satisfying $\cap U_i \neq \emptyset$.

If $\beta$ is another cover such that for each $V\in \beta$, there is a $U\in
\alpha$ with $V\subseteq U$, then the assignment $V\to U$ in this case defines 
a map 

$$C(X,\alpha)\to C(X,\beta)$$

dependent on the choice of $U$ for each
$V$, but independent 'up to homotopy'.  

Applying one's favourite homotopy
functor, $F : \mathbf{S}\to \mathbf{A}$, to each $C(X,\alpha)$ and to these homotopy
classes of induced transition maps, yields an inverse  system of objects in
$\mathbf{A}$, i.e.,  a
[[pro-object]]  in $\mathbf{A}$, but the $C(X,\alpha)$ by themselves do _not_ define a pro-object in the category of simplicial sets. They do form a pro-object in $Ho(sSets)$, or alternative, a 'coherent pro-object'in $sSets$, (see [[Čech homotopy]] for more discussion on this point.)


### &#268;ech homology and cohomology ###

Aleksandrov and &#268;ech in the 1930s, applied 
homology and cohomology in this situation to extend simplicially-based
homology to a much wider class of spaces.  Lefshetz, without the language of
category theory, studied, again in the 1930s, the formal properties of inverse 
systems of polyhedra and maps between them and his student Christie looked at the homotopy groups in this setting.  

* see [[Čech cohomology]] and [[Čech homotopy]] for more on this.

### Shape theory as a &#268;ech homotopy theory ###

Borsuk (1968) developed [[shape theory]], which although initially very geometric in flavour turned out also to be described in terms of Christie's
theory of the "&#268;ech extensions" of homotopy theory, (see [[shape theory]] and [[Čech homotopy]] for references and more on this area).


### &#268;ech-like methods in algebraic geometry ###

The use of modified &#268;ech methods in algebraic geometry was well
established when Grothendieck and his collaborators in Paris started adapting
it to work with a [[Grothendieck topology]].  Verdier in SGA4,
introduced hypercoverings and in Artin and Mazur (SLN 100), you can find their use
in homotopy theory.  (The work of Lubkin (1967) should also be
mentioned here as it contains much that is parallel to the development by
Verdier, Artin and Mazur and is sometimes much easier to decipher for the
non-specialist algebraic geometer.)

Given that a [[Grothendieck topology]] is essentially about abstracting a notion
of '[[cover|covering]]', it is not surprising that 
modified &#268;ech methods can be applied. Artin and Mazur 
used Verdier's idea of a [[hypercover|hypercovering]] to get, for each Grothendieck topos,
$\mathbb{E}$, a pro-object in $Ho(\mathbf{S})$ (i.e. an inverse system of
simplicial sets), which they call the &#233;tale [[homotopy type]] of the topos
$\mathbb{E}$ (which for them is 'sheaves for the &#233;tale topology on a
variety').  

Applying homotopy group functors gives pro-groups $\pi_i(\mathbb{E})$ 
such that $\pi_1(\mathbb{E})$ is essentially the same as Grothendieck's [[algebraic fundamental group]],
$\pi_1(\mathbb{E})$.  (Here you need to know that the category of [[profinite
group]]s in the topological sense, is equivalent to the category of [[pro-object]]s in the category of
finite groups (as explained in [[profinite group]]).  (If you remove
'finite' the result does not hold, but you can recover it in part by
working with "pro-discrete [[localic groups]]" instead of topological groups,
i.e. take limits of finite groups within the category of '[[locale|localic]]' rather than 
'[[topological group|topological]]' groups, remembering that 'locales' are almost 'spaces without
points'.

Grothendieck's nice $\pi_1$ has thus an interpretation as a formal limit of a &#268;ech
type, or shape theoretic, system of $\pi_1$s of 'hypercoverings'.  

Can [[shape
theory]] (or its more powerfully structured 'strong' or 'homotopy coherent' version,
cf. Lisica and Marde&#353;i&#263;, Edwards and Hastings, Porter
(papers 1976--78) be useful for studying &#233;tale homotopy
type?  Not without extra work, since the Artin--Mazur--Verdier approach leads  
one  to look at inverse systems in $proHo(\mathbf{S})$, i.e. inverse systems
(diagrams) in a homotopy category not a homotopy category of inverse systems
as in [[strong shape theory]].  Attempts to 'rigidify' the hypercovering approach,
so as to get into $Hopro(\mathbf{S})$ have been made (e.g. by Lubkin, (1967)
or using simplicial schemes in Friedlander, (1982),
but it is not completely clear if one of them is 
the definitive method.
+-- {: .query}
What is the consensus on this here?  I have sometimes seen talks which claim to have THE method but none has been clearly THE ONE. Perhaps I did not go to the right conferences! (Some is needed here, e.g. for more ways of getting around the difficulty.)
=--

One of the difficulties with this hypercovering approach is that 
'hypercovering' is a difficult concept and to the 'non-expert' seem
non-geometric and lacking in intuition.  Thankfully for us, there is an
alternative approach put forward by Ken Brown (1973), (see [[BrownAHT]]).

As the Grothendieck topos $\mathbb{E}$ 'pretends to be' the category of
$Sets$, but with a strange logic, we can 'do' simplicial set theory in
$Simp(\mathbb{E})$ as long as we take care of the arguments we use.  To see a
bit of this in action we can note that the object $[0]$ in $Simp(\mathbb{E})$
will be the constant simplicial sheaf with value the ordinary $[0]$,
"constant" here taking on two meanings at the same time, 

(a) constant sheaf, i.e. not varying 'over $X$' if $\mathbb{E}$ is thought of as $Sh(X)$, and 

(b)
constant simplicial object, i.e. each $K_n$ is the same and all face and
degeneracy maps are identities.  Thus $[0]$ interpreted as an &#233;tale space
is the identity map $X\to X$ as a space over $X$.  Of course not all
simplicial objects are constant and so $Simp(\mathbb{E})$ can store a lot of
information about the space (or site) $X$. 

One can look at the homotopy
structure of $Simp(\mathbb{E})$.  Ken Brown in [[BrownAHT]] showed it had a
fibration category structure and if we look at
those fibrant objects $K$ in which the natural map 

$$p : K \to [0]$$

 is a weak 
equivalence, we find that these $K$ are _exactly_ the [[hypercover|hypercoverings]].  Global
sections of $p$ give a simplicial set, $\Gamma(K)$ and varying $K$ amongst the 
hypercoverings gives a pro-simplicial set (still in $proHo(\mathbf{S})$ not in
$Hopro(\mathbf{S})$ unfortunately) which determines the Artin--Mazur
pro-homotopy type of $\mathbb{E}$


###Links with derived category theory###

This makes it clear there is a link between &#268;ech methods and [[derived category]]
theory.  In the first, the 'space' is resolved using '[[cover]]ings'
and these, in a [[sheaf]] theoretic setting, lead to [[simplicial object]]s in $Sh(X)$
that are weakly equivalent to $[0]$; in the second, to evaluate the 
[[derived functor]] of some functor $F : \mathbf{C} \to \mathbf{A}$, say, on an object $C$,
one takes the 'average' of the values of $F$ on objects weakly equivalent to
$G$, i.e. one works with the functor 

$$F' : \mathbf{W}(C) \to \mathbf{A}$$

(where $ \mathbf{W}(C)$ has objects, $\alpha : C \to C'$, $\alpha$ a
weak equivalence, and maps, the commuting 'triangles', and this has a 'domain' 
functor $\delta :\mathbf{W}(C) \to \mathbf{C}$, $\delta(\alpha) = C'$
and $F'$ is the composite $F\delta$). 

This is in many cases a pro-object 
in $\mathbf{A}$ -- unfortunately standard derived functor theory interprets
'commuting triangles' in too weak a sense and thus corresponds to shape rather 
than strong shape theory -- one thus, in some sense, arrives in $pro
Ho(\mathbf{A})$ instead of in $Ho(pro \mathbf{A})$.  This problem has been in part resolved with Grothendieck's theory of _Derivateurs_ (see the volume by Maltsiniotis.)

* see also [[abelian sheaf cohomology]]
