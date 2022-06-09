This page is about spectral sequences in [[homotopy type theory]].  For now, it contains mainly a fixed version of two blog posts, one at the [n-category cafe](http://golem.ph.utexas.edu/category/2013/08/what_is_a_spectral_sequence.html) and the other on the [HoTT blog](http://homotopytypetheory.org/2013/08/08/spectral-sequences/).

# Spectral sequences in homotopy type theory
* table of contents
{: toc}

## What is a spectral sequence?

There are many answers to "what is a [[spectral sequence]]?", but the one I'm proposing right now is the following analogy.  (In my experience, category theorists tend to like analogies --- possibly because, as John Baez once said, every sufficiently good analogy is yearning to become a functor.  This one is no exception.)

> Spectral sequences are to long exact sequences as iterated extensions are to extensions.

(Without knowing anything else, the terminology suggests that spectral sequences could also be called "iterated long exact sequences".)

There are four phrases here that I need to explain, and two more concepts that have a ghostly presence (fibration sequences and iterated fibration sequences).  First of all, an *extension* is a sequence of morphisms of abelian groups (for simplicity --- more generally we could be in any abelian category):
$$ A \xrightarrow{f} B \xrightarrow{g} C$$
such that $f$ is the inclusion of the kernel of $g$, and $g$ is the quotient of $B$ by the image of $f$.  Equivalently, $f$ is injective, $g$ is surjective, and the image of $f$ is equal to the kernel of $g$.  The simplest example is
$$ A \xrightarrow{(id,0)} A\oplus C \xrightarrow{proj_2} C.$$
An extension that's isomorphic to one of this form is said to be *split*.  In general, we can regard an extension as exhibiting $B$ as "put together" in some more general way from $A$ and $C$; we say that $B$ is an "extension of $C$ by $A$".  The underlying set of $B$ is always isomorphic to the cartesian product $A\times C$, so we can think of $B$ as a sort of "twisted product" of $A$ and $C$.  (In fact, as usual in this sort of situtaion, the twisting is measured by a cohomology class, living in $Ext^1(C,A)$, but we won't need that today.)

Thinking of $B$ as put together from $A$ and $C$, we can draw certain conclusions about the one from the other, or the other from the one.  The most obvious is that if $A=C=0$, then also $B=0$.  The converse also holds: if $B=0$, then $A=C=0$.  If only $A=0$, then we can conclude $B=C$, and similarly if $C=0$ we have $A=B$.  We can also say fancier things of this sort, e.g. $B$ is finite, or finitely generated, if and only if both $A$ and $C$ are.

Next, a *long exact sequence* (LES) is a longer sequence of morphisms of abelian groups
$$ \cdots \xrightarrow{f_{n+1}} A_{n+1} \xrightarrow{f_n} A_n \xrightarrow{f_{n-1}} \cdots $$
such that for each $n$, the image of $f_n$ is equal to the kernel of $f_{n-1}$ (called "exactness at $A_n$").  The sequence might be infinite or finite in either direction.  How are LES's related to extensions?  Well, one obvious relationship is that an extension can equivalently be described as an exact sequence of the form
$$ 0 \to A \xrightarrow{f} B \xrightarrow{g} C \to 0$$
(a "short exact sequence"), since in such a sequence, exactness at $A$ just means injectivity of $f$, and exactness at $C$ just means surjectivity of $g$.  However, what I want to focus on instead is the basic homotopical origin of LES's, namely fibration sequences.  A *fibration sequence* is a sequence of maps of pointed spaces
$$ X \xrightarrow{f} Y \xrightarrow{g} Z $$
such that $f$ is (up to homotopy) the inclusion of the homotopy fiber of $g$ over the basepoint.  (By "space" I really mean "$\infty$-groupoid", which a classical topologist could read as "topological space up to weak homotopy equivalence" or "simplicial set up to weak homotopy equivalence", and a homotopy type theorist could read as "type".)  The simplest example is
$$ X \to X\times Z \to Z,$$
the "trivial bundle" over $Z$ with fiber $X$.  In general, we can think of $Y$ as being "put together" from $X$ and $Z$ in some more general way, as a "twisted product".  Note that this is very similar to how we think of an extension, except that we've replaced our abelian groups with spaces.

Of course, a space is not exactly an abelian group, but it contains many abelian groups, namely its homotopy groups.  So we might expect that if $Y$ is a twisted product of $X$ and $Z$ as above, that its homotopy groups $\pi_n(Y)$ would be twisted products of $\pi_n(X)$ and $\pi_n(Z)$, i.e. that there would be extensions $\pi_n(X) \to \pi_n(Y) \to \pi_n(Z)$.  This is not true, since the various dimensions $n$ can "interact" in a nontrivial way; but instead we have a *long* exact sequence
$$ \cdots \to \pi_{n+1}(X) \to \pi_{n+1}(Y) \to \pi_{n+1}(Z) \to \pi_n(X) \to \pi_n(Y) \to \pi_n(Z) \to \cdots. $$
This LES can be regarded as expressing a way in which the groups $\pi_n(Y)$, considered as a whole, are "put together" out of the $\pi_n(X)$'s and $\pi_n(Z)$'s.  We get some of the same sorts of results, e.g. if $\pi_n(X)=0$ for all $n$, then $\pi_n(Y) = \pi_n(Z)$ for all $n$, and dually.  But some different things happen, e.g. if $\pi_n(Y)=0$ for all $n$, rather than $\pi_n(X) = 0 = \pi_n(Z)$ we get $\pi_n(X) = \pi_{n+1}(Z)$ for all $n$ (and indeed, if $Y$ is contractible, then $X = \Omega Z$).

Another way to express the LES of a fibration, which looks more like what we'll see for spectral sequences later on, is that there exist maps $\delta_n : \pi_n(Z) \to \pi_{n-1}(X)$ and extensions
$$ im(\delta_{n+1}) \to \pi_n(Y) \to ker(\delta_n). $$
In other words, instead of $\pi_n(Y)$ being put together from $\pi_n(X)$ and $\pi_n(Z)$, it's put together from a *subgroup* of $\pi_n(Z)$ and a *quotient* of $\pi_n(X)$.  This allows us to fulfil the yearnings of the analogy between fibration sequences and extensions: for each $n$ there's a functor from the category of fibration sequences to the category of extensions, sending $X\to Y\to Z$ to the above extension.

Of course, $\pi_n$ is only an abelian group for $n\ge 2$.  Some of what we do with abelian groups can be extended to the case of groups ($n=1$) and pointed sets ($n=0$), but I don't want to get into that.  Feel free to assume all spaces are simply connected.  Another way to avoid nonabelianness is to replace spaces with *spectra*, in which case $\pi_n$ is an abelian group not only for all $n\ge 0$ but for all $n\in \mathbb{Z}$.  In this case, the LES of a fibration sequence extends infinitely in both directions.

Now let's move on to the other side of the analogy, starting with iterated extensions.  By an *iterated extension* I mean a sequence of extensions of the following form:
$$\array{
  \vdots \\
  A_{s+1} \to B_{s+1} \to B_s\\
  A_s \to B_{s} \to B_{s-1} \\
  A_{s-1} \to B_{s-1} \to B_{s-2}\\
  \vdots
}$$
The intent here is to regard $B :\equiv \lim (\cdots \to B_{s+1} \to B_s \to \cdots)$ as "put together" from the $A_s$'s and from $C :\equiv \colim (\cdots \to B_{s+1} \to B_s \to \cdots)$.  In many cases, the sequence of $A_s$'s will be eventually zero in one direction or the other, so that the sequence of $B_s$'s will similarly be eventually constant.  Eventual constancy as $s\to\infty$ implies that $B$ is the eventual value, while eventual constancy as $s\to-\infty$ implies that $C$ is that eventual value.  In the latter case it simplifies things with no essential loss of generality to end with
$$\array{
  \vdots \\
  A_{1} \to B_{1} \to B_0\\
  B_0 \to B_{0} \to 0 \\
  0 \to 0 \to 0 \\
  \vdots
}$$
so that $C=0$ and the $A_s$'s are the only "ingredients" of $B$ (with $A_0 = B_0$).  I'm going to focus mostly on the case where this holds and the sequence is also eventually constant in the other direction, so we have only finitely many extensions.  In this case it's easy to draw some of the same sorts of conclusions as in a single extension, e.g. $B=0$ if and only if all $A_s=0$, and so on; the general case is sometimes trickier but often works out, although "$\lim^1$" terms start to pop up.

It's more common to describe iterated extensions in terms of *filtrations*.  From any iterated extension as above, we have a sequence of subgroups
$$ \cdots \subseteq F_s B \subseteq F_{s-1} B \subseteq \cdots \subseteq B $$  
where $F_s B$ is the kernel of the projection $B \to B_s$.  Since this projection is surjective, we have $B_s = B/F_s B$, and hence $A_s = F_{s-1} B/F_s B$.  Thus, the whole iterated extension can be recovered from the filtration:
$$\array{
  \vdots\\
  F_s B / F_{s+1} B \to B / F_{s+1}B \to B/F_s B\\
  F_{s-1} B / F_{s} B \to B / F_{s}B \to B/F_{s-1} B\\
  \vdots
}$$
One problem with this point of view is that just having a filtration doesn't ensure that $B$ is the limit $\lim_s B/ F_s B$.  When this is the case, one says that the filtration is *complete and Hausdorff*.  (As you might guess, these words refer to a [uniformity](http://ncatlab.org/nlab/show/uniform+space) induced on $B$ by the filtration.)  The other condition we might want is that $C = B / \bigcup_s F_s B$ is zero, i.e. that $\bigcup_s F_s B = B$; a filtration with this property is called *exhaustive*.  For *finite* iterated extensions, however, these conditions are all automatic.

A more serious problem with the filtration point of view is that it relies on the fact that the quotient of the kernel of a surjection is that same surjection --- otherwise we couldn't recover $B_s$ from $F_s B$.  This is no longer true when we replace abelian groups by pointed spaces and extensions by fibration sequences.  Thus, in that case we *have* to consider instead an *iterated fibration sequence*, consisting of a sequence of fibration sequences:
$$\array{
  \vdots \\
  X_{s+1} \to Y_{s+1} \to Y_s\\
  X_s \to Y_s \to Y_{s-1}\\
  X_{s-1} \to Y_{s-1} \to Y_{s-2}\\
  \vdots
}$$
As before, we view this as expressing the limit $Y :\equiv \lim_s (\cdots \to Y_{s+1}\to Y_s \to \cdots)$ as put together out of the $X_s$'s.  It's more common to describe this as a *tower of fibrations*
$$ \cdots \to Y_{s+1}\to Y_s \to Y_{s-1} \to \cdots $$
since $X_s$ is determined as the (homotopy) fiber of the map $Y_s \to Y_{s-1}$.  But by talking about iterated extensions instead of filtrations, and iterated fibration sequences instead of towers of fibrations, we can see the analogy much more easily.

(If we were working with spectra instead of spaces, then from an iterated fibration sequence we could define a "filtration" of the limit $Y$, where $F_s Y$ is the fiber of the map $Y\to Y_s$.  Then $Y_s$ *would* be the cofiber of $F_s Y \to Y$.  However, $F_s Y \to Y$ would not necessarily be "injective" in any sense.)

The goal now is to extract some algebraic relationship among the groups $\pi_n(X_s)$ and $\pi_n(Y)$ in an iterated fibration sequence, which relate to iterated extensions just as LES's relate to extensions.  Of course, the first thing we get is a sequence of LES's:
$$\array{
  \vdots\\
  \cdots \to \pi_n(X_{s+1}) \to \pi_n(Y_{s+1}) \to \pi_n(Y_s) \to \pi_{n-1}(X_{s+1}) \to \cdots \\
  \cdots \to \pi_n(X_{s}) \to \pi_n(Y_{s}) \to \pi_n(Y_{s-1}) \to \pi_{n-1}(X_{s}) \to \cdots \\
  \vdots
}$$
These sequences are related in that each group $\pi_n(Y_s)$ appears in *two* of them.  This enables us to construct the following composite "connecting maps"
$$ \pi_n(X_s) \to \pi_n(Y_s) \to \pi_{n-1}(X_{s+1}). $$
relating the homotopy groups of the fibers $X_s$.  For reasons that will become clear later, we'll call these maps $d^2$ (note that this does *not* mean the square of a map $d$; the superscript $2$ is just an index).  The first interesting thing we notice about them is that they satisfy $d^2 \circ d^2 = 0$, since in the composite
$$ \pi_n(X_s) \to \pi_n(Y_s) \to \pi_{n-1}(X_{s+1}) \to \pi_{n-1}(Y_{s+1}) \to \pi_{n-2}(X_{s+2}) $$
the middle two maps are adjacent in a LES, hence compose to $0$.  Thus, for every value of $n+s$, we have a *chain complex*
$$ \cdots \xrightarrow{d^2} \pi_n(X_s) \xrightarrow{d^2} \pi_{n-1}(X_{s+1}) \xrightarrow{d^2} \pi_{n-2}(X_{s+2}) \xrightarrow{d^2} \cdots. $$
Of course, if we're experienced homological-algebraists, the first thing that we want to do with a chain complex is take its homology, but let's step back a second to make sure that that's a sensible thing to do.

A *cycle* in this chain complex is an element $x\in \pi_n(X_s)$ that becomes zero in $\pi_{n-1}(X_{s+1})$.  This means that when we map $x$ into $\pi_n(Y_s)$, it lands in the kernel of $\pi_n(Y_s) \to \pi_{n-1}(X_{s+1})$.  But since the sequence 
$$ \cdots \to \pi_n(X_{s+1}) \to \pi_n(Y_{s+1}) \to \pi_n(Y_s) \to \pi_{n-1}(X_{s+1}) \to \cdots $$
is exact, that means exactly that the image of $x$ in $\pi_n(Y_s)$ lies in the image of $\pi_n(Y_{s+1})$.  In other words, an element $x\in \pi_n(X_s)$ automatically gives us an element of $\pi_n(Y_s)$, while $d^2(x)$ is precisely the "obstruction" to lifting that to an element of $\pi_n(Y_{s+1})$.  This naturally seems like the "first step" towards lifting it to an element of $\pi_n(Y)$, which is what we're really interested in.

Similarly, a *boundary* in this chain complex is an element of $\pi_n(X_s)$ that's in the image of $\pi_{n+1}(X_{s-1})$, and hence in particular in the image of $\pi_{n+1}(Y_{s-1})$.  But since the sequence
$$  \cdots \to \pi_{n+1}(Y_{s-1}) \to \pi_n(X_{s}) \to \pi_n(Y_{s}) \to \pi_n(Y_{s-1}) \to \cdots $$
is exact, any such element must map to zero in $\pi_n(Y_{s})$, and hence also lift to zero in $\pi_n(Y_{s+1})$.  So the homology at $\pi_n(X_s)$ (the group of cycles modulo the group of boundaries) is indeed a reasonable "second approximation" to "what we can learn about $\pi_n(Y)$ from $\pi_n(X_s)$".

For a "third approximation", we can more or less repeat the process.  Given something in this homology "$H_{n,s}(\pi_\ast(X_\ast))$", we can lift it to $\pi_n(Y_{s+1})$, then map it into $\pi_{n-1}(X_{s+2})$.  The result is not well-defined because the lift is not well-defined, but its indeterminacy is precisely that of the lift, which by exactness is just an element of $\pi_n(X_{s+1})$.  Thus, we do have a well-defined element of the quotient of $\pi_{n-1}(X_{s+2})$ by the image of $d^2$, which happens to also lie in the kernel of $d^2$, and hence a map $d^3 : H_{n,s}(\pi_\ast(X_\ast)) \to H_{n-1,s+2}(\pi_\ast(X_\ast))$.  I'll leave it to you to check that these maps make $H_{n,s}(\pi_\ast(X_\ast))$ into another chain complex, and that elements of its homology can be lifted to $\pi_n(Y_{s+2})$.

In order to describe these higher approximations uniformly, let's introduce a bit more terminology.  Recall that if $G$ is an abelian group, then a *$G$-graded abelian group* is just a family $(A_g)_{g\in G}$ of abelian groups indexed by the underlying set of $G$.  If $A$ and $B$ are $G$-graded abelian groups and $h\in G$, then a *degree-$h$ map* $f:A\to B$ consists of maps $f_g : A_g \to B_{g+h}$ for all $g$.  The composite of a degree-$h_1$ map with a degree-$h_2$ map is a degree-$(h_1+h_2)$ map.  For example, an unbounded chain complex may be defined as a $\mathbb{Z}$-graded abelian group equipped with a degree-1 (or degree-$(-1)$) endomap $d$ such that $d \circ d = 0$ (an equality of maps of degree 2 or $(-2)$).

Now, the groups $\pi_n(X_s)$ and $\pi_n(Y_s)$ can be assembled into a pair of $(\mathbb{Z}\times \mathbb{Z})$-graded abelian groups $D$ and $E$, and three maps between them $i$, $j$, and $k$.  The obvious grading is by $n$ and $s$, but for historical reasons, I'm going to choose a different basis of $\mathbb{Z}\times \mathbb{Z}$, and write $(p,q)$ for the indexing elements.
$$ E_{p,q} :\equiv \pi_{p+q}(X_q) $$
$$ D_{p,q} :\equiv \pi_{p+q}(Y_q) $$
If $p+q\lt 0$, then by convention we set $\pi_{p+q}=0$ (unless we are working with spectra, in which case no special convention is needed).  Now each long exact sequence
$$ \cdots \to \pi_n(X_{s}) \to \pi_n(Y_{s}) \to \pi_n(Y_{s-1}) \to \pi_{n-1}(X_{s}) \to \cdots $$
can be rewritten as
$$ \cdots \to E_{n-s,s} \xrightarrow{k_{n-s,s}} D_{n-s,s} \xrightarrow{i_{n-s,s}} D_{n-s+1,s-1} \xrightarrow{j_{n-s+1,s-1}} E_{n-s-1,s} \to \cdots $$
Together, the maps in these LES's assemble into three graded maps
$$\array{
  D & & \xrightarrow{i} & & D\\
  & _{k}\nwarrow & & \swarrow_j\\
  && E
}$$
where $i$, $j$, and $k$ have degrees $(1,-1)$, $(-2,1)$, and $0$ respectively.  Moreover, the exactness of the LES's implies that this triangle is exact at each vertex.  This structure (two graded groups $D$ and $E$ and maps $i:D\to D$, $j:D\to E$, and $k:E\to D$ of some degrees such that the above triangle is exact at each vertex) is called an *exact couple*.

Now we can formalize the above process of successive approximation through passage to homology as follows.  Given any exact couple $(D,E,i,j,k)$, we construct a new *derived* exact couple as follows.

* The composite $d :\equiv j k : E \to E$ satisfies $d d = j k j k = 0$, so we can define $E' :\equiv ker(d)/im(d)$ to be its homology.
* Let $D' = im(i) \subseteq D$.  (Of course, both of these should be interpreted "degreewise", remembering that $i$ and $d$ may have nonzero degrees.)
* Let $i':D'\to D'$ be the restriction of $i$ to $D'$ (which obviously lands inside $D'$).
* Define $j':D'\to E'$ as follows.  Given $x\in D'$, we have $x = i(y)$ for some $y\in D$; let $j'(x)$ be the homology class determined by $j(y)$ (which is a cycle since $k j = 0$).  This is well-defined since if $x = i(y')$ as well, then $i(y-y') = 0$, hence $y-y' = k(z)$ for some $z\in E$, and thus $j(y) - j(y') = d(z)$ is a boundary.
* Define $k':E'\to D'$ by restricting $k$ to $ker(d)$ (which lands inside $D'$ since if $d(x) = j(k(x)) = 0$, then $k(x)$ lies in the image of $i$ by exactness) and then passing to the quotient (which is well-defined since $k j = 0$).
* I'll leave it as an exercise to check the exactness of $i'$, $j'$, and $k'$.  Note that $deg(i') = deg(i)$ and $deg(k')=deg(k)$, but $deg(j')=deg(j) - deg(i)$.

We can thus iterate this process.  We write $(D^r,E^r,i^r,j^r,k^r)$ for the exact couple obtained by $r-2$ iterations.  In particular, we have graded abelian groups $E^r$, each of which is equipped with a differential $d^r : E^r \to E^r$ of degree $deg(j) + deg(k) - (r-2)\cdot deg(i)$ satisfying $d\circ d = 0$, and such that $E^{r+1}$ is the homology of $(E^r,d)$.  This structure is called a *spectral sequence*.

Note that I've chosen the indexing so that $E^2$ is the graded group $E$ we started with.  Like the change from $(n,s)$ to $(p,q)$, this is to match the convention used in the literature.  (And that, in turn, is because some other ways of constructing spectral sequences begin with an $E^1$ whose homology is $E^2$.  And that, I guess, is because someone a long time ago thought that the natural numbers started with $1$, since I've never heard of an "$E^0$".  Although no doubt someone in the comments will point out a spectral sequence that starts with $E^0$.)

When the groups in a spectral sequence are $(\mathbb{Z}\times\mathbb{Z})$-graded, as in our example and in most cases, it is usual to draw them in a lattice on the plane, with $p$ the horizontal coordinate and $q$ the vertical one.  For instance, $E^2$ can be drawn like this:
$$\array{
  & \vdots & \vdots & \vdots & \vdots & \\
  \cdots & E_{-1,2}^2 & E_{0,2}^2 & E_{1,2}^2 & E_{2,2}^2 & \cdots\\
  \cdots & E_{-1,1}^2 & E_{0,1}^2 & E_{1,1}^2 & E_{2,1}^2 & \cdots\\
  \cdots & E_{-1,0}^2 & E_{0,0}^2 & E_{1,0}^2 & E_{2,0}^2 & \cdots\\
  \cdots & E_{-1,-1}^2 & E_{0,-1}^2 & E_{1,-1}^2 & E_{2,-1}^2 & \cdots\\
  & \vdots & \vdots & \vdots & \vdots &
}$$
We call this the $E^2$ *page* of the spectral sequence.  When the degrees of the differentials are as they are in our example (which is, again, the most common situation), we can draw the differential $d^2$ on this lattice as moving two steps left and one step up.  The best picture I've been able to find of this online is [here](http://mathworld.wolfram.com/SpectralSequence.html), although it's of the dual "cohomologically indexed" case where the arrows go down and right instead of up and left.

Just to keep ourselves a bit more grounded, here's what the $E^2$ page looks like in the case of an iterated fibration sequence of spaces:
$$\array{
  & \vdots & \vdots & \vdots & \vdots & \\
  \cdots & \pi_1(X_2) & \pi_2(X_2) & \pi_3(X_2) & \pi_4(X_2) & \cdots\\
  \cdots & \pi_0(X_1) & \pi_1(X_1) & \pi_2(X_1) & \pi_3(X_1) & \cdots\\
  \cdots & 0 & \pi_0(X_0) & \pi_1(X_0) & \pi_2(X_0) & \cdots\\
  \cdots & 0 & 0 & 0 & 0 & \cdots\\
  & \vdots & \vdots & \vdots & \vdots &
}$$
With spectra, the zero groups above would be replaced by negative homotopy groups such as $\pi_{-1}(X_0)$, etc.

We then obtain the $E^3$ page by replacing each entry $E^2_{p q}$ of the $E^2$ page by the homology of $d^2$ at that spot, i.e. the kernel of the outgoing differential modulo the image of the incoming one.  The $E^3$ page then has its own differential $d^3$ which goes *three* steps left and *two* steps up, and we repeat.  We then "take the limit" of $E^r$ as $r\to\infty$, and hope that the resulting "$E^\infty$" terms are useful --- in our example, we hope they tell us something about the groups $\pi_n(Y)$.

First of all, we have to address the question of what it means to "take the limit", since in general $E^{r+1}$ is neither a subobject nor a quotient object of $E^r$, but a *subquotient* (a quotient of a subobject, or equivalently a subobject of a quotient).  One can make sense of this in general, but in many (perhaps most) applications of spectral sequences, there's a much simpler answer.  Namely, it often happens that for each grading $(p,q)$, the groups $E^r_{p q}$ eventually stabilize as $r\to\infty$, so that we can define $E^\infty_{p q}$ to be their eventual value.  (The $r$ at which this happens generally depends on $(p,q)$, so that interesting things are still happening *somewhere* in $E^r$ for arbitrarily large values of $r$.)

Of course, having $E^{r+1}_{p q} = E^r_{p q}$ means that the differentials coming into and out of $E^r_{p q}$ are zero, and a good reason for this is if their domain and codomain are respectively the zero group.  Note that when the differentials have the usual degrees, they always move from one diagonal $p+q=n$ to the next lower one $p+q=n-1$.  Thus, if each diagonal in the $E^2$ page (hence also in every other page) contains only finitely many nonzero groups, then the groups $E^r_{p q}$ will eventually stabilize for each $(p,q)$.

In particular, this is the case in the example arising from a *finite* iterated fibration sequence, where the nonzero part of the spectral sequence lives entirely in a finite strip $0\le q\le Q$.  It's also the case for a bounded *above* fibration sequence (which stabilizes above some point $s=T$ but extends infinitely downwards) as long as for every $n$, there is a point below which $\pi_n(X_s) = \pi_n(Y_s)=0$, such as if the truncatedness of $Y_s$ decreases, or their connectedness increases, as $s\to-\infty$.  In this case, we have the following.

**Convergence Theorem:** Suppose given a bounded-above iterated fibration sequence
$$\array{
  X_{T} \to Y_{T} \to Y_{T-1}\\
  \vdots \\
  X_s \to Y_s \to Y_{s-1}\\
  X_{s-1} \to Y_{s-1} \to Y_{s-2}\\
  \vdots
}$$
such that for every $n$, there is an $R$ such that $\pi_n(X_s) =\pi_n(Y_s)=0$ for $s\le R$, and let $Y = \lim_s Y_s = Y_T$.  Then for every $n$, there is a finite iterated extension:
$$\array{
  E^\infty_{n-T,T} \to B_{n,T} \to B_{n,T-1}\\
  \vdots \\
  E^\infty_{n-s,s} \to B_{n,s} \to B_{n,s-1}\\
  E^\infty_{n-s+1,s-1} \to B_{n,s-1} \to B_{n,s-2}\\
  \vdots\\
  E^\infty_{n-R,R} \to B_{n,R} \to 0
}
$$
such that $B_n = \lim_s B_{n,s}= B_{n,T}$ is equal to $\pi_n(Y)$.

This theorem makes our second analogy also into a functor between suitable categories of iterated fibration sequences and iterated extensions.

Note that the $E^\infty$ groups appearing in the iterated extension for $\pi_n(Y)$ are those on the diagonal $p+q=n$.  Thus, the theorem says that when $Y$ is put together out of the $X_s$'s, then $\pi_n(Y)$ is put together out of the groups on this diagonal, which are computed from the homotopy groups of the $X_s$'s in some way (encoded by the spectral sequence).  It's traditional to write this sort of "convergence" as
$$ E^2_{p,q} = \pi_{p+q}(X_q) \;\Rightarrow\; \pi_{p+q}(Y) $$
to indicate which $E^\infty$ groups are the "ingredients" of which group in the target.

At this point I should remind you that we're either assuming all spaces are simply connected, or working with spectra instead of spaces.  The notion of "convergence" is a lot trickier when you have to deal with nonabelianness of $\pi_1$ and nongroupness of $\pi_0$.  There are also fancier convergence theorems that allow more infinite behavior, such as when $E^r_{p q}$ doesn't stabilize but still has a "limit".  Finally, with an unbounded-above iterated fibration sequence we would also have to deal with the fact that $\pi_n(\lim_s Y_s)$ may not equal $\lim_s \pi_n(Y_s)$.

**Proof of convergence theorem:** For any $(p,q)$, let $r \ge max(T-q+3,q-R+1)$.  Then $E^r_{p q}$ has stabilized, so that $E^\infty_{p q} = E^r_{p q}$.  For such an $r$, $D^r_{p q}$ is the $(r-2)$-fold image of $i:D^2\to D^2$, i.e. those elements in $D^2$ of the form $i(i(\cdots i(x)\cdots ))$ with $(r-2)$ copies of $i$.  Since $i$ consists of the maps $\pi_n(Y_s) \to \pi_n(Y_{s-1})$, and $\pi_n(Y_s) = \pi_n(Y)$ for $s\ge T$, this means $D^r_{p q}$ is the image of $\pi_{p+q}(Y)$ in $\pi_{p+q}(Y_q)$ (and in particular is independent of $r$ sufficiently large).  Let $B_{n,s}= D^r_{n-s,s}$ for any such $r$, i.e. the image of $\pi_n(Y)$ in $\pi_n(Y_s)$.

It remains to construct the extensions $E^\infty_{n-s,s} \to B_{n,s} \to B_{n,s-1}$ displayed above.  However, just as we put together the exact couple $(D^2,E^2,i^2,j^2,k^2)$ from long exact sequences, from the exact couple $(D^{r},E^{r},i^{r},j^{r},k^{r})$ we can extract some other long exact sequences.  Note that by iterating the above formulas for degrees in a derived exact couple, we have $deg(i^{r}) = (1,-1)$ and $deg(k^{r}) = 0$, but $deg(j^{r}) = (-r,r-1)$.  Thus, we have LES's
$$ \cdots \to D^{r}_{p+r,q-r+1} \xrightarrow{j} E^{r}_{p,q} \xrightarrow{k} D^{r}_{p,q} \xrightarrow{i} D^{r}_{p+1,q-1} \xrightarrow{j} E^{r}_{p-r+1,q+r-2} \to\cdots $$
If we choose $r \ge max(T-s+4,s-R+1)$, then all three terms in the middle have stabilized, while the two on the ends are zero.  Thus, inside this LES we have a short exact sequence
$$0 \to E^\infty_{n-s,s} \to B_{n,s} \to B_{n,s-1} \to 0 $$
which is the extension that we wanted.  $\Box$


This is all very abstract, so let's look at a couple of degenerate cases.  First, in the case of a finite iterated fibration sequence with $T=1$, we have
$$\array{
  X_1 \to Y \to X_0\\
  X_0 \to X_0 \to \ast
}$$
hence essentially just a single fibration sequence.  The spectral sequence is confined to the strip $q\in \{0,1\}$, with $E^2$ page looking like:
$$\array{
\cdots & \pi_0(X_1) & \pi_1(X_1) & \pi_2(X_1) & \pi_3(X_1) & \cdots \\
\cdots & 0 & \pi_0(X_0) & \pi_1(X_0) & \pi_2(X_0) & \cdots
}$$
The differentials on this page go, as always, left two and up one, hence from $\pi_n(X_0) \to \pi_{n-1}(X_1)$; these are exactly the "connecting maps" $\delta_n$ in the ordinary LES of the fibration.  Since the differentials entering $\pi_n(X_0)$ come from zero, and those leaving $\pi_n(X_1)$ go to zero, on passage to homology we get the $E^3$ page
$$\array{
  \cdots & im(\delta_1) & im(\delta_2) & im(\delta_3) & im(\delta_4) & \cdots \\
  \cdots & 0 & ker(\delta_0) & ker(\delta_1) & ker(\delta_2) & \cdots
}$$
We have $E^3 = E^\infty$ since all the remaining differentials hit zero on one side or the other, so that $E^\infty_{p,0} = ker(\delta_p)$ and $E^\infty_{p,1} = im(\delta_{p+2})$.  The theorem then gives an iterated extension
$$ \array{
  im(\delta_{n+1}) \to \pi_n(Y) \to ker(\delta_n)\\
  ker(\delta_n) \to ker(\delta_n) \to 0
  }$$
which is just the ordinary extension we observed above as coming from an LES.

Another degenerate case is when the iterated fibration sequence is the *Postnikov tower* of a space (or spectrum) $Y$.  Suppose $Y$ is an $m$-type, i.e. $\pi_n(Y)=0$ for $n\gt m$.  Then for any $n\le m$ we have an $n$-type ${\Vert Y\Vert}_n$, with fibration sequences
$$ X_n \to {\Vert Y\Vert}_n \to {\Vert Y\Vert}_{n-1} $$
where $X_n = K(\pi_n(Y),n)$ is an Eilenberg-Mac Lane space, with $\pi_n(X_n) = \pi_n(Y)$ and $\pi_i(X_n) = 0$ for $i\neq n$.  Together these form an iterated fibration sequence with limit $Y$.  When $Y$ is an $m$-type space, it is a finite sequence; when $Y$ is an $m$-type spectrum it is bounded above and satisfies the condition on downward homotopy groups; thus the convergence theorem applies.  Since each fiber $X_n$ is an Eilenberg-Mac Lane space of dimension $n$, the $E^2$ page of the spectral sequence is concentrated on the line $p=0$, looking like this:
$$\array{
  \vdots \\
  \pi_2(Y)\\
  \pi_1(Y) \\
  \pi_0(Y)\\
  \vdots
}$$
There is no room for any nontrivial differentials, $E^2=E^\infty$, and for each $n$ we obtain the trivial iterated extension
$$\array{
  0 \to \pi_n(Y) \to \pi_n(Y) \\
  \vdots\\
  0 \to \pi_n(Y) \to \pi_n(Y) \\
  \pi_n(Y) \to \pi_n(Y) \to 0 \\
  0 \to 0 \to 0 \\
  \vdots\\
  0 \to 0 \to 0.
}$$

Of course, the *interesting* applications of spectral sequences are less trivial, but this post is already quite long enough.  In the companion post on the HoTT blog, I'll talk about how to use this spectral sequence (with spectra) to extract versions of the Atiyah-Hirzebruch and Serre spectral sequences, and see what they can do for us.

One final teaser: note that while the groups in the $E^{r+1}$ page of a spectral sequence are determined by the groups and the differentials in the $E^r$ page, the differential in the $E^{r+1}$ page is not so determined.  To figure out what it is, we need to know about the rest of the $r^{\mathrm{th}}$ exact couple, which can be tedious to work out.  In many applications it suffices to know that such a differential *exists*, without knowing anything about it; but sometimes the values of the differential do matter.  However, if we had a fully *constructive* definition of the whole exact couple and spectral sequence, as we would obtain by implementing the definition in a hypothetical fully constructive version of homotopy type theory, then the definition would be a program, and we could simply ask the computer to evaluate it on any input we cared about.  This suggests to me a vague possibility of a way that homotopy type theory might conceivably one day be useful even to the "working algebraic topologist".

## Spectral Sequences in HoTT

Now we want to construct the cohomological Serre spectral sequence of a fibration (i.e. a type family).  First recall that a **spectrum** is a family of pointed types $ Y : \mathbb{N} \to \mathsf{Type}_\ast$ such that $ Y_n = \Omega Y_{n+1}$ for all $n$.  Last time I defined the **cohomology** of a type $X$ with coefficients in a spectrum $Y$ to be 

$$ H^n(X;Y) :\equiv \Vert X \to \Omega^{k-n} Y_k \Vert_0$$

for $k$ sufficiently large that $ k-n \ge 0$.  An equivalent way to define this is as

$$ H^n(X;Y) :\equiv \pi_{-n} (\mathsf{SpMap}(X,Y))$$

where $ \mathsf{SpMap}(X,Y)$ is the *mapping spectrum* defined by $ \mathsf{SpMap}(X,Y)_n :\equiv (X\to Y_n)$, and the homotopy groups of a spectrum $Z$ are defined by

$$ \pi_n (Z) :\equiv \pi_{k+n}( Z_k)$$

for any $ n \in \mathbb{Z}$ and any $k$ sufficiently large that $ n+k\ge 0$.  Again, the definition of a spectrum makes this independent of $k$.  In general, we can "do homotopy theory" with spectra just as we can with types.  A map of spectra is, of course, a fiberwise pointed map $ f : \prod_{(n:\mathbb{N})} Y_n \to Z_n$ such that the evident squares commute relating it to the equivalences $ Y_n = \Omega Y_{n+1}$ and $ Z_n = \Omega Z_{n+1}$.  Similarly, the *fiber* of such a map is defined levelwise, with $ \mathsf{fib}(f)_n :\equiv \mathsf{fib}(f_n)$.  It's easy to see that this inherits a spectrum structure.  Moreover, the long exact sequences of homotopy groups for the fiber sequences $ \mathsf{fib}(f_n) \to Y_n \to Z_n$ splice together into a long exact sequence

$$ \cdots \to \pi_n(\mathsf{fib}(f)) \to \pi_n(Y) \to \pi_n(Z) \to \cdots $$

which is infinite in *both* directions, with all entries being abelian groups.

Now in part one above, I explained how from an iterated fibration sequence

$$ \array{\vdots \\
     X_{s+1} \to Y_{s+1} \to Y_s\\
     X_s \to Y_s \to Y_{s-1}\\
     X_{s-1} \to Y_{s-1} \to Y_{s-2}\\
     \vdots}
$$

we obtain a spectral sequence with $ E^2_{p q} = \pi_{p+q}(X_q)$.  Moreover, if the iterated fibration sequence stabilizes as $ s\to \infty$ (i.e. for $ s\gt T$ it becomes $ \mathbf{1} \to Y \to Y$) and eventually becomes zero at each homotopy group separately as $ s \to -\infty$, then this spectral sequence "converges" to the homotopy groups of $Y$, in the sense that for each $n$ we have a finite iterated extension

$$\array{
  E^\infty_{n-T,T} \to \pi_n(Y) \to B_{n,T-1}\\
  \vdots\\
  E^\infty_{n-s,s} \to B_{n,s} \to B_{n,s-1}\\
  E^\infty_{n-s+1,s-1} \to B_{n,s-1} \to B_{n,s-2} \\
  \vdots\\
  E^\infty_{n-R,R} \to E^\infty_{n-R,R} \to 0
}
$$

in which the $ E^\infty$ terms occurring are precisely the nonzero ones on the diagonal $ p+q=n$ of the $ E^\infty$ page.  (There are fancier sorts of convergence that apply to more general situations, but I don't want to get into that right now.)  One writes this as

$$ E^2_{p,q} = \pi_{p+q}(X_q) \Rightarrow \pi_{p+q}(Y) $$

The only homotopical input required was the long exact sequences of homotopy groups associated to the iterated fibration sequence, which as we've seen applies just as well to spectra as to types.  After that, it was only homological algebra of abelian groups, which was fully constructive, and hence formalizable using sets in homotopy type theory, with higher inductive types for quotients and images.

Part one was kind of light on examples, though.  I mentioned the obvious example of an iterated fibration sequence, namely the Postnikov tower of $Y$:

$$\array{
  K(\pi_s(Y),s) \to {\Vert Y\Vert}_s \to {\Vert Y\Vert}_{s-1}\\
  K(\pi_{s-1}(Y),s-1) \to {\Vert Y\Vert}_{s-1} \to {\Vert Y\Vert}_{s-2}\\
  \vdots
}
$$

If $Y$ is an $m$-type for some $ m\lt \infty$, then this satisfies our simple hypotheses for convergence.  A spectrum also has a Postnikov tower, with $ (\Vert Y \Vert_s)_n$ defined to be $ \Vert Y_n\Vert_{n+s}$.  This makes sense for any $ s \in \mathbb{Z}$, as long as we make the convention that $ \Vert X\Vert_{m} = \mathbf{1}$ if $ m \lt  -1$.  If we define an **$m$-type spectrum** to be one for which $ Y_n$ is an ordinary $ (n+m)$-type for all $ n \ge -m-2$, then the Postnikov tower of such a $Y$ also satisfies our simple hypotheses for convergence despite potentially being infinite downwards (an $m$-type spectrum can have nontrivial $ \pi_n$ for all $ -\infty \lt  n \le m$).

The Postnikov tower of a space or spectrum doesn't give rise to an interesting or useful spectral sequence.  However, mapping out of a type preserves fibration sequences, so for any type $X$ and spectrum $Y$ we have an induced iterated fibration sequence

$$\array{
\mathsf{SpMap}(X,K(\pi_s(Y),s)) \to \mathsf{SpMap}(X,{\Vert Y\Vert}_s) \to \mathsf{SpMap}(X,{\Vert Y\Vert}_{s-1}) \\
\mathsf{SpMap}(X,K(\pi_{s-1}(Y),s-1)) \to \mathsf{SpMap}(X,{\Vert Y\Vert}_{s-1}) \to \mathsf{SpMap}(X,{\Vert Y\Vert}_{s-2}) \\
\vdots
}
$$

where $ K(A,s)$ denotes the spectrum whose $ n^{\mathrm{th}}$ space is the usual Eilenberg-Mac Lane space $ K(A,s+n)$ if $ s+n\ge 0$, and contractible otherwise.  Note that the spectrum $ K(A,0)$ is the Eilenberg-Mac Lane spectrum that we denoted $ H A$ last time.

Hence, we have a spectral sequence with

$$\begin{aligned}
    E^2_{p q} &= \pi_{p+q}(\mathsf{SpMap}(X,K(\pi_q(Y),q)))\\
             &= \pi_p(\mathsf{SpMap}(X,H(\pi_q(y)))\\
             &= H^{-p}(X;\pi_q(Y))
  \end{aligned}$$

the "ordinary" $ (-p)^{\mathrm{th}}$ cohomology of $X$ with coefficients in the abelian group $ \pi_q(Y)$.  If $Y$ is an $m$-type spectrum for some $m$, then this spectral sequence converges in the above sense to the homotopy groups $ \pi_n( \mathsf{SpMap}(X,Y))$, which as remarked above are the cohomology $ H^{-n}(X;Y)$.

This is called the *Atiyah-Hirzebruch spectral sequence*.  It says that for any (sufficiently nice) spectrum $Y$, the cohomology of any type $X$ with coefficients in $Y$ (what algebraic topologists call "generalized cohomology") can be put together out of the "ordinary" cohomology of $X$ with coefficients in the homotopy groups of $Y$.  One usually flips the sign of $p$ and $q$ in "cohomological" spectral sequences of this sort, simultaneously switching the subscripts and superscripts; thus we write instead

$$ E_2^{p q} = H^p(X;\pi_{-q}(Y)) \Rightarrow H^{p+q}(X;Y)$$

Graphically, this corresponds to rotating all the "pages" of the spectral sequence by 180 degrees about the origin.  This causes the differentials to go down and right rather than left and up.  (Note also that $ \pi_{-q}(Y) = H^q(\mathbf{1};Y)$ is also the $ q^{\mathrm{th}}$ cohomology of a point with coefficients in $Y$.)

Of course, this may not seem very interesting unless you have some spectra up your sleeve other than $ H A$ whose cohomology you care about.  However, we can also use it to construct the Serre spectral sequence, which is interesting even as a statement only about ordinary cohomology.

First we have to generalize our notion of cohomology a bit.  In the language of classical algebraic topology, we're going to define *parametrized* cohomology theories, including as a special case *cohomology with local coefficients*.  However, in type-theoretic language, what's going on is extremely simple and natural: replacing function types with *dependent* function types.

Thus, suppose $X$ is a type and $ Y : X \to \mathsf{Spectrum}$ is an $X$-indexed family of spectra.  We define the cohomology of $X$ with coefficients in $Y$ to be

$$ H^n(X;Y) :\equiv \pi_{-n} (\mathsf{SpSect}(X,Y))$$

where $ \mathsf{SpSect}(X,Y)$ is the "spectrum of sections of $Y$" defined by $ \mathsf{SpSect}(X,Y)_n :\equiv \prod_{(x:X)} Y(x)_n)$.  As usual with dependent function types, when $Y$ is a constant family this reduces to the previously defined notion of cohomology.

Where do families of spectra come from?  One place they come from is families of abelian groups.  If $ A : X \to \mathsf{AbGp}$ is such, then composing it with the "Eilenberg-Mac Lane spectrum" function $ H : \mathsf{ApGp}\to \mathsf{Spectrum}$ we obtain an $X$-indexed family of spectra, $ H A$.  Note that since abelian groups are sets, $ \mathsf{AbGp}$ is a 1-type, and hence any such $A$ factors through $ \Vert X \Vert_1$, the "fundamental groupoid" of $X$.  This is the homotopy-type-theory version of what classical algebraic topologists would call a *local system* on $X$.  If $X$ is pointed and connected, then $ \Vert X \Vert_1 = K(\pi_1(X),1)$, and so (using the univalence axiom) we can further reduce a local system to a single abelian group with an action by $ \pi_1(X)$, the most classical notion.  The cohomology of $X$ with coefficients in $ H A$ is called *cohomology with local coefficients*.

Where do local systems come from?  One place they come from is homotopy groups of families of types (or spectra).  We can compose $ \pi_n : \mathsf{Type}_\ast \to \mathsf{AbGp}$ or $ \pi_n : \mathsf{Spectrum} \to \mathsf{AbGp}$ with any family $ Y : X \to \mathsf{Type}_\ast$ of pointed types or $ Y : X \to \mathsf{Spectrum}$ of spectra to obtain a local system.  I think the ease with which we can pass back and forth between local systems and families of spectra is a good example of the value of the type-theoretic framework.

In the same way, we can construct the "fiberwise" Postnikov tower of a family of spectra $ Y : X \to \mathsf{Spectrum}$, obtaining an $X$-indexed family of iterated fibration sequences.  The fibers of these fibration sequences are loopings or deloopings of "parametrized Eilenberg-Mac Lane spectra" associated to the local systems $ \pi_q(Y) : X \to \mathsf{AbGp}$.  Sinc $ \mathsf{SpSect}$, like $ \mathsf{SpMap}$, preserves fibration sequences, we get a more general Atiyah-Hirzebruch spectral sequence with $ E^{p q}_2 = H^{p}(X;\pi_{-q}(Y))$ (meaning the cohomology with local coefficients in the local system $ \pi_{-q}(Y)$), which converges to $ H^{p+q}(X;Y)$ if $Y$ is a family of $m$-type spectra.

Now we're ready to deduce the Serre spectral sequence.  Let $Y$ be an ordinary spectrum, such as $H A$, and let $ F : X \to \mathsf{Type}$ be a type family.  Then $ x\mapsto \mathsf{SpMap}(F_x,Y)$ is an $X$-indexed family of spectra, which are $m$-type spectra if $Y$ is.  Thus, we have the above "parametrized" Atiyah-Hirzebruch spectral sequence:

$$ H^p(X;\lambda x.\pi_{-q}(\mathsf{SpMap}(F_x,Y))) \Rightarrow H^{p+q}(X;\lambda x.\mathsf{SpMap}(F_x,Y)).$$

On the left, we have $ \pi_{-q}(\mathsf{SpMap}(F_x,Y)) = H^q(F_x;Y)$ by definition.  And as for the right side, we have

$$
\begin{aligned}
  H^n(X;\lambda x.\mathsf{SpMap}(F_x,Y)) &= \pi_{-n}(\mathsf{SpSect}(X,\lambda x.\mathsf{SpMap}(F_x,Y)))\\
  &= \pi_{-n}(\mathsf{SpMap}(\sum_{(x:X)} F_x, Y))\\
  &= H^n(\sum_{(x:X)}F_x;F)
\end{aligned}
$$

the cohomology of the total space of the fibration *F* with coefficients in $Y$.  (The second step is a spectral version of the ordinary universal mapping property of $ \Sigma$-types, $ ((\sum_{(x;X)} F_x) \to Z) = \prod_{(x:X)} (F_x \to Z)$.)  Thus, our spectral sequence becomes

$$ H^p(X;\lambda x. H^q(F_x;Y)) \Rightarrow H^{p+q}(\sum_{(x:X)} F_x;Y)$$

which is the usual cohomological Serre spectral sequence, relating the cohomology of the base, with local coefficients in the cohomology of the fiber, to the cohomology of the total space.  Note that if $X$ is pointed and simply connected, so that $ \Vert X \Vert_1 = \mathbf{1}$, then any local system on $X$ is constant, and so the cohomology with local coefficients in the domain reduces simply to the ordinary cohomology of $X$ with coefficients in the cohomology of the fiber over the basepoint.

After all of this theory, I ought to give you at least one application to justify it all.  Here's a fairly easy one.  Suppose we have a fibration of spheres, i.e. a fiber sequence $ S^a \to S^b \to S^c$ in which all three types are spheres of some dimension, and suppose that $ c\gt1$ so that $ S^c$ is simply connected and that $ a\gt0$ and $ b\gt0$ for nontriviality.  Then we have a Serre spectral sequence

$$ H^p(S^c; H^q(S^a;\mathbb{Z})) \Rightarrow H^{p+q}(S^b;\mathbb{Z}).$$

The Eilenberg-Steenrod axioms for ordinary cohomology (i.e. with coefficients in $ H \mathbb{Z}$) easily imply that $ H^n(S^m;\mathbb{Z})$ is $ \mathbb{Z}$ when $ n=0$ and $ n=m$, and zero otherwise.  Thus, the $ E_2$ page of this spectral sequence is $ \mathbb{Z}$ at $ (0,0), (c,0), (0,a), (c,a)$, and zero everywhere else.  The only possible nontrivial differential would be a map from $ E^r_{0,a}$ to $ E^r_{c,0}$, and this is only possible if $ c = a+1$.  If there is *no* such differential, then $ E_\infty = E_2$, and so the target $ H^n(S^b;\mathbb{Z})$ will be built out of nontrivial groups for $ n = 0,a,c,a+c$.  However, we know that $ H^n(S^b;\mathbb{Z})$ is zero unless $ n = 0,b$, so this is impossible.  Therefore, $ c = a+1$, the differential $ E^r_{0,a} \to E^r_{c,0}$ is an isomorphism and "kills" both of these groups, and $ b = a+c = 2a+1$.  (This argument by contradiction is valid constructively, since natural numbers have decidable equality.)

In conclusion, *the only possible fibrations of spheres are of the form* $ S^a \to S^{2a+1}\to S^{a+1}$.  When $ a=1$ we do have such a fibration, namely the Hopf fibration.  (Classically, there are also such fibrations for $ a=3,7$ and no other positive values of $a$ --- the latter is a famous theorem called the "Hopf invariant one problem".)

There are lots of other applications of spectral sequences; it'll be fun to see how many of them we can reproduce.  Many of them require homology in addition to cohomology, though, which would be a whole other post.

One last comment deserves to be made.  I claimed that this "is" the Serre spectral sequence, but actually I haven't proven that.  It has the same groups in its $ E_2$ page, and converges to the same thing, but that doesn't imply that the whole spectral sequence is the same (although it strongly suggests it).  And I haven't seen this construction of the Serre SS anywhere in the classical algebraic topology literature (although I'd be surprised if it were new) --- most constructions use instead a CW decomposition of $X$, which is unavailable to us.  So does this "Serre spectral sequence" agree with the classical one when interpreted in the simplicial model?  I'm not sure how to go about trying to prove that.  *(Edit: See [below](#Maunder)!)*

## On indexing choices

The "natural" indexing of the spectral sequence $\pi_n(X_s)$ constructed above is by $n$ and $s$, and in this indexing the initial differential has degree $(-1,1)$.  We chose to reindex it by writing $n = p+q$ and $s=q$, in which case the initial differential has $(p,q)$ degree $(-2,1)$, thereby matching the indexing and degrees for the $E_2$ page of some known spectral sequences (such as the Serre and Atiyah-Hirzebruch SS).

However, there are other ways to do the reindexing.  For instance, if we instead set $n = t-s$, then the initial differential will have $(s,t)$ degree $(1,0)$, which looks more like the $E_1$ page of a spectral sequence.  For instance, the Adams spectral sequence can be obtained in this way from a suitably chosen tower of fibrations (although usually in that case one talk about cofibers rather than fibers, which in the world of spectra are the same up to a furtherh degree shift).  Thanks to [[nlab:Urs Schreiber]] for pointing this out.

## Notes

Some notes not in the original blog posts:

* In the section on Spectral Sequences on HoTT it is ambiguous whether $\mathsf{SpMap}(X,Y)$ and $\mathsf{SpSect}(X,Y)$ consists of pointed or unpointed maps. Most steps taken are true both when they are interpreted as pointed or as unpointed maps. If $\mathsf{SpMap}(X,Y)$ is unpointed then $X$ is unpointed and $\pi_{-n} (\mathsf{SpMap}(X,Y))$ is the unreduced cohomology of $X$ (with coefficients in $Y$). If $\mathsf{SpMap}(X,Y)$ is pointed then $X$ is interpreted as a pointed type and $\pi_{-n} (\mathsf{SpMap}(X,Y))$ is the reduced cohomology. Everything in the proof of the Atiyah-Hirzebruch spectral sequence holds for both cases, so the Atiyah-Hirzebruch spectral sequence exists for both reduced and unreduced cohomology. However, the Serre Spectral sequence is only valid for unreduced cohomology, since the equivalence
$$\mathsf{SpSect}(X,\lambda x.\mathsf{SpMap}(F_x,Y)) = \mathsf{SpMap}(\sum_{(x:X)} F_x, Y)$$
used in the proof is only true for unpointed maps.

* Urs Schreiber has [pointed out](https://homotopytypetheory.org/2013/08/08/spectral-sequences/#comment-100544) that this construction of the AHSS appears in a [1963 paper](http://journals.cambridge.org/abstract_S0305004100037245) by C. R. F. Maunder, who also shows that it agrees with the standard construction by constructing an isomorphism of exact couples.  It seems likely that a similar method would work for the Serre SS.
 {#Maunder}

* This construction has been formalized [here](https://github.com/cmu-phil/Spectral) in Lean, and will appear in the PhD thesis of Floris van Doorn.

category: homotopy theory