#The Path Integral#

**Under Construction**

##Background/Motivation##

[[target|Target]] space is a finite [[path category]] $P_1(X)$ generated from a [[directed graph]].

We fix a finite [[gauge group]] $G$ and some [[representation]] 

$$\rho: \mathbf{B}G \to Set$$

(where $\mathbf{B}G$ is the one-object [[groupoid]] version of $G$). Let's write $V//G$ for the corresponding [[action groupoid]].

The [[background field]] is a [[functor]]

$$\nabla: P_1(X) \to \mathbf{B}G.$$

A [[state]] is a [[section]] of this restricted to points, namely a [[lift]] of $\left.\nabla \right|_0: P_0(X)\to \mathbf{B}G$ through

$$V\to V//G\to \mathbf{B}G.$$

So that's just a choice of element in $V$ over each point.

A bit more interesting, if we [[transgression|transgress]] to [[path space]] by homming the [[interval category]] $(a\to b)$ into everything to get

$$tg\nabla:hom((a\to b),P_1(X))\to hom(a\to b,\mathbf{B}G).$$

Then restricting that functor to objects and taking sections in terms of lifts through

$$hom(a\to b,V)\to hom(a\to b,V//G)\to hom(a\to b,\mathbf{B}G)$$

over objects yields: over each path a choice of element in $V$ over the endpoints, such that they are related by the parallel transport of $\nabla$ along that path.

Everybody still following? But to some extent that is just motivation for the following simple situation that I want to look at:

##A span of groupoids##

Let's build a [[span]] of finite [[groupoid|groupoids]] this way:

Let

$$\Gamma_X:=\bigcup_{x\in P_0(X)} V//G$$

be something like the groupoid of the graph of sections over points. Big words &#8211; I just mean the disjoint union of one copy of the [[action groupoid]] of our rep over each point of target space. To be thought of as a groupoid of sections over target space.

Similarly, let

$$\Gamma_{PX}:=\bigcup_{\gamma\in hom(a\to b,P_1(x))} \Gamma(tg_\gamma\nabla)$$

be the disjoint union over all morphisms in $P_1(X)$ of all sections of $\nabla$ over that path: for each $\gamma$ this groupoid is isomorphic to $V//G$ again, but we think of an object now as a flat section over the path

$$(x,v_1)\stackrel{(\gamma,g=\nabla(\gamma))}{\longrightarrow} (y,v_2=v_1\cdot g).$$

Now we build a span from these of the form

$$
\array{
{} & {} & \Gamma_{PX} & {} & {}  \\
{} & {}^{in}\swarrow & {} & \searrow^{out} & {} \\
\Gamma_X & {} & {} & {} & \Gamma_X
}
$$

Here the functor $in:\Gamma_{PX}\to\Gamma_X$ simply projects out the left end of a path, and the functor $out:\Gamma_{PX}\to\Gamma_X$ the right end. So

$$in:((x,v_1)\stackrel{(\gamma,g=\nabla(\gamma))}{\longrightarrow} (y,v_2))\mapsto (x,v_1)$$

and

$$out:((x,v_1)\stackrel{(\gamma,g=\nabla(\gamma))}{\longrightarrow} (y,v_2))\mapsto (y,v_2).$$

Okay, now lets do groupoidily linear algebra and see how bundles of sets over $\Gamma_X$ pull-push through this span.

Let me pick one single point $x$ in target space and one section over it, $v\in V$.
Define 

**Under Construction**

{&#8226;}  &#8600;   &#915; X


to be the functor of groupoids which sends the single object of the terminal groupoid to that object  (x,v) in &#915; X.


The pull-push


     in *{&#8226;}      &#8595; {&#8226;}     &#915; PX     &#8747;in *{&#8226;}  &#8600;   in&#8601;   &#8600; out  &#8601;   &#915; X     &#915; X


produces first in *{&#8226;}&#8594;&#915; P X: that has precisely one point sitting over each labeled path which starts at x and is labeled there by v.


Then it produces &#8747;in *{&#8226;}&#8594;&#915; X: this has over the point y with label v&#8242; one point per path x&#8594;y which is labeled by v over x and by v&#8242; over y.


To see what this means, fix one point y in X. Then we get one point over each label v&#8242; for each path from x to y labeled by v on the left and by v&#8242; on the right.


But since the labels of the paths are sections of the transgressed transport functor over these paths, which just means that these are flat sections of the original transport over these paths, it means that the v&#8242; appearing here are of the form &#8711;(g)v for g the parallel transport over the given path.


So the "total" space of &#8747;in *{&#8226;} over y&#8712;X is the V-colored set
&#8746; &#947;:x&#8594;y{&#8226; &#8711;(&#947;)v},


where I write &#8226; v for an element colored by v. 


If V has an additive structure, for instance if it is a vector space, we have the cardinality operation on V-colored sets
&#8739;&#8901;&#8739;:Set V&#8594;V
and get that the cardinality of the above is


&#8721; &#947;:x&#8594;y&#8711;(&#947;)v,


But that's the right path integral kernel for propagation from x to y acting on the state v over x.



So what?


About all ingredients of the above we have talked before, in one way or another. Lots of ingredients from John's discussion of groupoidification and John an Jeffrey's "categorified" quantum mechanics appear. But somehow I feel that I have not before put things together in the picture as above. To me, I had the feeling this clarified some things that had been a bit mysterious to me before:


a) the fact that the path integral should be "taking sections at codimension 0";


b) the natural connection of a) to groupoidification;


c) the natural and automatic appearance of V-colored sets.



But I have to stop here. If Konrad or Hisham read this, or some of the other people waiting for me getting back to them with tasks finished, they'll be unhappy to see me instead talk about foundational abstract nonsense here. But I needed to relax a bit. :-)

##References##

+-- {.query}
This is material that Urs originally posted at the [n-Cafe](http://golem.ph.utexas.edu/category/2008/06/an_exercise_in_groupoidificati.html), but I think deserves to be cleaned up and made into a nice introductory example.
=--

* [[Exploding a Category]]
