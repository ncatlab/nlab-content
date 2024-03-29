
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Differential geometry
+-- {: .hide}
[[!include synthetic differential geometry - contents]]
=--
#### Mapping space
+-- {: .hide}
[[!include mapping space - contents]]
=--
=--
=--

# Contents
* automatic table of contents
{: toc}

# Loops with Singularities # {: #title}

##### Andrew Stacey ##### {: #author}

+-- {: .num_section #sectiona }
=--
## The Original Question ## {: .num_section}

On [MathOverflow](http://www.mathoverflow.com) there was a question "[I was wondering if the set of singular loops is somewhere a submanifold of loop space?](http://mathoverflow.net/questions/75071/i-was-wondering-if-the-set-of-singular-loops-is-a-somewhere-submanifold-of-loop)". [[Ryan Budney]] and [[Torsten Ekedahl]] gave two answers that showed that the answer was "No". In the chronology, Torsten's answer came first and gave an example to show why the space described in the first version of the question could not work. The question was modified to take account of that, whereupon Ryan stepped in to show why the modified space could not be a smooth manifold. Whilst Ryan and Torsten's answers do give the complete answer, the question intrigued [[Andrew Stacey|me]] since there are spaces related to the one in the question that are smooth manifolds. This page is the result of thinking about that.

At time of writing, the question reads as follows (formatting and links added).

> The set of all smooth maps $S^{1}\to M^{n}$ ($M$ is a smooth manifold) is a generalized manifold (see [[smooth loop space]]).

> I was wondering if the set of singular loops (maps with self-crossings or zeros of derivative) is a ([[Fréchet manifold|Fréchet]], [[Frölicher space|Frölicher]], [[diffeological space|diffeological]]) submanifold of the [[loop space]]?

> **EDIT:** it is clear that answer is no (see [Torstens answer](http://mathoverflow.net/questions/75071/i-was-wondering-if-the-set-of-singular-loops-is-a-somewhere-submanifold-of-loop/75077#75077)). So, I rewrite the question: is it true that set of singular loops is a collection of submanifolds of different codimension (set of loops with one self-intersection has codimension $\dim M-2$, loops with zero of derivative has codimension $\dim M -3$ and so on. Set of loops with infinite number of singularities should have infinite codimension\dots . Let's forget about them.)

> So, the question is about local situation: for example, let's consider a loop with one self-intersection (and without other singlarities). Is it true that set of near loops with one self-intersection is a submanifold in sense of ([[Fréchet manifold|Fréchet]], [[Frölicher space|Frölicher]], [[diffeological space|diffeological]])?

> **EDIT 2.** I reformulate the question. $\map (S^{1} \to \mathbb{R} ^{3})$ is a functional space, so we can apply a technique of singularity theory. Generic map $f$ with one self-intersection has one-parameter versal deformation $V\colon [0,1]\times S^{1}\to \mathbb{R} ^{3}$ -- and any deformations are induced from $V$. Does it imply that $D$ (set of singular loops) near the $f$ is a submanifold of codimension 1 in sense of [[Fréchet manifold|Fréchet]] or [[Frölicher space|Frölicher]]?

I'm going to take a different approach to this question. I'm going to start with a space that I know is a submanifold of $L M$ and modify it little-by-little until I get to what (I think) you describe. As I do so, hopefully it will be clear where we lose the manifold structure (and why).

+-- {: .num_section #sectionb }
=--
## Finding a Manifold ## {: .num_section}

The space that is a submanifold is the space of loops with a particular coincidence. Let us think of the circle as the unit circle in the complex plane (for definiteness). Then of all the smooth maps $S^{1} \to M$ we can consider the subset which are coincident at $1$ and $-1$. Identifying $1$ and $-1$ gives us one form of the figure eight and so we can think of this subspace as $C^{\infty } (8,M)$. Indeed, if we work in one of the categories of [generalised smooth space](http://ncatlab.org/nlab/show/generalised smooth space), then there is a "smooth space" $8$ and the subspace we are interested in truly is $C^{\infty } (8,M)$.

This space is a manifold, in whatever sense you wish. The model space is $C^{\infty } (8,\mathbb{R} ^{n})$; its tangent space at a map $f$ is the space of sections of $f^{*} T M$ which agree at $1$ and $-1$. It is also a submanifold of $L M$, and actually has a tubular neighbourhood. So it's as nice as you can get!

The most obvious difference between this and your space is that we have not just a coincidence, but we have fixed where it must occur. So our first generalisation is to allow that coincidence to move. But we want to proceed cautiously, so we start by considering triples $(f,p,q)$ where $f \colon S^{1} \to M$ is a smooth map and $p,q \in S^{1}$ are two points. This is $L M \times S^{1} \times S^{1}$. Next, we consider the subset of these triples that satisfy $f(p) = f(q)$ and $p \ne q$.

I claim that this is a manifold. Let us start by considering those triples $(f,p,q)$ with $\Re p \gt \frac{1}{2}$ and $\Re q \lt - \frac{1}{2}$ (and $f(p) = f(q)$). Let us label this space as $W$. Let us choose a smooth family of diffeomorphisms of the circle, say $\tau _{a,b}$, parametrised by $a, b \in S^{1}$ with $\Re a \gt \frac{1}{2}$ and $\Re b \lt -\frac{1}{2}$ with the property that $\tau _{a,b}(a) = 1$ and $\tau _{a,b}(b) = -1$. We define a map $W \to C^{\infty } (8,M) \times S^{1} \times S^{1}$ by $(f,p,q) \mapsto (f \circ \tau _{p,q}^{-1}, p, q)$. The claim is that this is a diffeomorphism onto its image which is an open subset of the target. The inverse is given by $(f,p,q) \mapsto (f \circ \tau _{p,q},p,q)$. The target is $\{ (f,p,q) : \Re p \gt \frac{1}{2}, \Re q \lt -\frac{1}{2}\} $.

For a more general point, $(f,p,q)$, we choose a diffeomorphism, say $\sigma $, of the circle which maps $p$ to $1$ and $q$ to $-1$. Then we define a diffeomorphism of $L M \times S^{1} \times S^{1}$ by $(g,r,s) \mapsto (g \circ \sigma ^{-1},\sigma (r),\sigma (s))$. This takes $(f,p,q)$ into $W$ and we can pullback the chart from there.

A very simple thing to do at this point is to forget the order of the pair $(p,q)$. This is a $\mathbb{Z} _{2}$--action and the action has all the required properties for the quotient to still be a manifold. Thus we have a manifold of things of the form $(f,\{ p,q\} )$ where $f \colon S^{1} \to M$ is a smooth map, $\{ p,q\} \subseteq S^{1}$ is a two-element subset, and $f(p) = f(q)$ (or $f \!\!\mid _{\{ p,q\} }$ is constant).

+-- {: .num_section #sectionc }
=--
## Finding a Non-Manifold ## {: .num_section}

The final step is to try to project this down on to the first component. That is, to consider the map from our space to $L M$ given by mapping $(f,\{ p,q\} ) \mapsto f$. What would be nice would be if this were some sort of submersion and we could deduce from it (maybe with a little work) that the image was a manifold.

The first problem that we encounter is that the fibre does not have a constant model. For "most" loops in the image, the preimage consists of a single point. This is because for "most" loops with a coincidence, there is only one such coincidence. But a loop with multiple coincidences has several preimages, one for each coincidence (or, more precisely, one for each two-element subset of each coincidence set).

A loop with multiple coincidences doesn't seem a major problem as we can locally just pick one to label. But that's not actually as simple as it might seem. If we have two coincidences and label one of them, then we can rip apart that coincidence *whilst staying in our space* because the other coincidence keeps us there. But if we destroy the labelled coincidence, what do we do with our label?

This is Torsten's objection, except with multiple double coincidences instead of a single triple one.

To fix this, we try restricting to the subset where there is only one coincidence. This means that our fibres are singletons and we have a smooth bijection from the suitable set of $(f,\{ p,q\} )$ to the set of corresponding loops. Leaving aside the question as to whether or not this is a diffeomorphism, this would seem to give a positive answer to the question.

It doesn't.

The reason is simple, but perhaps a little surprising. That is that the subset of those $(f,\{ p,q\} )$ where $\{ p,q\} $ is the *only* coincidence of $f$ is *not* an open subset of our manifold. Why this might be surprising is because if we go one level down then the corresponding family is open. That is, if we take the subset of those loops with *no* coincidences then this is an open subset of all loops (whence a submanifold).

We can show that this subset is not open by taking a sequence of loops with a double coincidence (one of which is labelled) which converges to a loop with a single coincidence. If it were open, at some point in the sequence all terms would have to have a single coincidence.

This is Ryan's objection.

We cannot fix this. The reason being that this subset *contains* an open subset of our manifold (again, by Ryan's answer) so the only way it could be a submanifold would be if it were open.

So the space in question is most emphatically not a submanifold. But there is a nearby manifold, which is the space of loops with a marked coincidence (and possibly other coincidences). For most loops, these two spaces are the same nearby, but for loops such as those that Torsten and Ryan consider, they aren't.


[[!redirects manifold structure of singular loops]]
[[!redirects manifold structures of singular loops]]
[[!redirects the manifold structure of singular loops]]
[[!redirects on the manifold structure of singular loops]]
[[!redirects manifold structure on the space of singular loops]]
[[!redirects manifold structures on the space of singular loops]]
[[!redirects manifold structures on spaces of singular loops]]
[[!redirects singular loop space]]
[[!redirects singular loop spaces]]
