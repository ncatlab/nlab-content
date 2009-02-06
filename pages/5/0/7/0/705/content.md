#Idea#

Consider three paths that begin at $x_0$ and end at $x_{2\tau}$ enclosing the spacetime region depicted below

$$\array{
{} & {} & {} & x_{2\tau} & {} & {} & {} \\
{} & {} & {} &  \bullet     & {} & {} & {} \\
{} & {} & {}^{v^-_{\tau}}\nearrow & {} & \nwarrow^{v_{\tau}^+} & {} & {} \\
x^-_{\tau} & \bullet & \stackrel{F^-}{\Uparrow} & \stackrel{v_0}{\uparr} & \stackrel{F^+}{\Uparrow} & \bullet & x^+_{\tau} \\
{} & {} & {}_{v_0^-}\nwarrow & {} & \nearrow_{v_0^+} & {} & {} \\
{} & {} & {} &  \bullet & {} & {} & {} \\
{} & {} & {} &    x_0   & {} & {} & {} 
}$$

Staring at the above picture, we want to understand the analogy:

$$\array{
category & functor & natural transformation \\
fiber & connection & curvature \\
position & velocity & acceleration
}$$

For those who better understand the mathematics of the first line, this analogy is likely to help motivate the physics as we go down the ladder. For those who better understand the physics of the bottom line, it is hoped that this analogy will help to motivate the mathematics as we move up the ladder.

#Formulation#

Denote the spacetime region by $\mathbb{D}^2$ and let $P^2(\mathbb{D}^2)$ denote the strict 2-category with

* Objects $\{x_0,x^+_\tau,x^-_\tau,x_{2\tau}\}$
* Morphisms $\{x_0\stackrel{v_0}{\to}x_{2\tau},x_0\stackrel{v^+_0}{\to}x^+_\tau,x_0\stackrel{v^-_0}{\to}x^-_\tau,x^+_\tau\stackrel{v^+_\tau}{\to}x^+_{2\tau},x^-_\tau\stackrel{v^-_\tau}{\to}x^-_{2\tau}\}$
* 2-Morphisms $\{v^+_0\stackrel{F^+}{\Rightarrow}v^+_\tau,v^-_0\stackrel{F^-}{\Rightarrow}v^-_\tau\}$


#Discussion#

_John said (from [n-Cafe](http://golem.ph.utexas.edu/category/2009/01/the_third_time_is_the_charm.html#c021749)):_

Todd wrote:


<blockquote>

Position, velocity, acceleration; Newton?

</blockquote>

YES!!!

Each one is clearly obtained from the previous one in a systematic way, and Newton invented this way &#8212; differentiation!  

But, he needed differentiation not for first derivatives, but for second derivatives.  His grand discovery was this: the laws of motion become clear not when we try to explain an object's position, nor when we try to explain its velocity, but only when we try to explain its acceleration!

So, just as Eilenberg and Mac Lane needed categories to define functors, and needed functors to define natural transformations, so they could make precise sense of cohomology theories being 'naturally isomorphic' ...

... Newton needed position to define velocity, and velocity to define acceleration, so he could make precise sense of 

$$F=ma.$$

There's even a nice analogy between these two trios.  An category is a place for an object to sit.  A functor is a way of changing an object.  A natural transformation changes a way of changing an object.  

I haven't quite figured out how to exploit this analogy.  It's interesting to note that an n-category internal to Vect is automatically a chain complex and is thus related to second derivatives by the formula 

$$d^2=0.$$

But somehow I should get natural transformations (chain homotopies) into the game.

Anyway, it might be a sign of genius for somebody to study a trio of concepts, each systematically derived from the previous one, where the third one is the charm.

***

_Urs said (from [n-Cafe](http://golem.ph.utexas.edu/category/2009/01/the_third_time_is_the_charm.html#c021768)):_

Let $G$ be a Lie group &#8211; and let's concentrate here on $G=\mathbb{R}$ to get closest to the Newtonian example regarded as a 1-object groupoid $\mathbf{B}\mathbb{R}$.

Functors from $\mathbf{B}\mathbb{R}$ to itself and natural transformations between these arrange themselves into the smooth 2-groupoid $\mathbf{BE}(\mathbb{R})$.

To find the infinitesimal version of this triple gadget (object = position, morphism = functor, 2-morphism = natural transformation) we proceed the way one differentiates any Lie group: we map smooth 1- and 2-parameter paths into this:

So let $P^2(\mathbb{R}^2)$ be the strict 2-groupoid of smooth paths in the plane and consider smooth 2-functors

$$F:P^2(\mathbb{R}^2)\to\mathbf{BE}(\mathbb{R}).$$

These 2-functors are in bijection with 1-forms $A$ on $\mathbb{R}^2$.

The way the equivalence works is precisely the Newtonian example:

Regarding the value of the functor $F$ on a path $\gamma$ in $\mathbb{R}^2$ as a trajectory in $\mathbb{R}$, $A$ gives the velocity of this trajectory with respect to "parameter time". For instance if you think of the standard speed parameterized path $\gamma:t\mapsto (t,0)$ in $\mathbb{R}^2$ and write $A=A_t dt$, then $A_t=v$ is precisely the velocity of the trajectory.

And the value of the 2-functor $F$ on 2-morphisms then, i.e. its value in natural transformations of functors on $\mathbf{B}\mathbb{R}$, is indeed given by the ("exterior") acceleration $dA$.

This example, incidentally, when we pass from $\mathbb{R}$ to more general groups and include linear representations, then also subsumes the first Trimblean triple as a "special case" of "category-functor-natural transformation".

***

_Urs then said (from [n-Cafe](http://golem.ph.utexas.edu/category/2009/01/the_third_time_is_the_charm.html#c021795)):_

Okay, let me try to find a setup in which this becomes very obvious.

First of all, the more obvious part of the analogy is

$$\array{
category & functor  & natural transformation \\
fiber & connection & curvature
}$$

so let me start with that. 

Here a simple situation is that where 

* each fiber looks like a group $G$, regarded as a one-object groupoid (hence a category), which I write as $\mathbf{B}G$;
* all functors go from $\mathbf{B}G$ to itself;
* and the natural transformations in question are the natural transformations between these functors.

And we want to assume that $G$ is a Lie group, so that we can proceed with the analogy which clearly presupposes a smooth setup.

In this case, the main subtlety in making sense of the above analogy comes from the existence of outer automorphisms on $G$. So, in the spirit of making everything as clear as possible, let me assume a situation where these vanish. For instance assume $G=E_8$ (i.e. the compact real form of $E_8$).

Then (I am saying this to be self contained for the record and for other readers) the relation between the two lines in the above analogy is established by the notioin of smooth 2-functors

$$tra:P^2(X)\to Cat$$

from the 2-groupoid $P^2(X)$ whose

* objects are points in a manifold $X$;
* morphisms are classes of smooth paths in $X$;
* 2-morphisms are classes of smooth surfaces in $X$.

Assume this 2-functor $tra$ assigns

1. to each point the fiber of a $G$-principal bundle $P$ over $X$, which we can locally identify with $G$ and hence with the category $\mathbf{B}G$
$$\array{
BG \\
category \\
fiber \\
P x
}$$
1. to each path $\gamma:x\to y$ a functor from the fiber over $x$ to the fiber over $y$. 
+-- {: .un_theorem #Connection}
###### Theorem
Such smooth assignments of functors to paths are in bijection with connections $\nabla$ on the $G$-principal bundle: upon identifying the fibers with $\mathbf{B}G$ the functor is given by an automorphism of $G$ hence, by assumption, by an element of $G$, and this element is the parallel transport $P\exp(\int_\gamma \nabla)$.
=--
$$\array{
\mathbf{B}G & BG\stackrel{tra(\gamma)}{\to} \mathbf{B}G \\
category & functor \\
fiber & connection \\
P_x & \nabla
}$$
1. to each surface $\Sigma:\gamma\to\gamma':x\to y$ a _natural transformation_ of functors $tra(\gamma)\to tra(\gamma')$. Since $\mathbf{B}G$ has a single object, such natural transformations are given by elements of $G$ once we identify the fibers with $\mathbf{B}G$.
+-- {: .un_theorem #Curvature}
###### Theorem
This element of $G$ is the group element
$P_\nabla\exp(\int_\Sigma F_\nabla)$
where $F_\nabla$ is the curvature 2-form of $\nabla$ and $P_\nabla\exp(\int \cdots)$ denotes the surface ordered exponential integral of a 2-form with respect to $\nabla$ (as appearing in the non-abelian Stokes theorem).
=--

$$\array{
\mathbf{B}G & \mathbf{B}G\stackrel{tra(\gamma)}{\to}\mathbf{B}G & tra(\gamma)\stackrel{\exists !}{\Rightarrow}tra(\gamma') \\
category & functor & natural transformation \\
fiber & connection & curvature \\
P_x & \nabla & F_\nabla
}$$

So that's how this works. Before going into the further analogy

$$\array{
category & functor & natural transformation \\
fiber & connection & curvature \\
position & velocity & acceleration
}$$

let's massage the above kind of observation into a form that we are all happy with.

***

_Urs then said (from [n-Cafe](http://golem.ph.utexas.edu/category/2009/01/the_third_time_is_the_charm.html#c021833)):_

Hi John,

<blockquote>

So maybe we can focus on the next stage [&#8230;]

</blockquote>

Okay. In my comment which started this discussion I essentially pointed out that:

the bijection/equivalence

(smooth 1-functors from paths in $X\to$ endomorphisms of $G$) $\simeq$ (1-forms)

is &#8211; manifestly the way one proves it &#8211; controlled by the concept of velocity:

if you think of $X$ as 1-dimensional, then the 1-form on $X$ with values in $Lie(G)$ is nothing but the gadget which reads in a bit of "coordinate time" for a trajectory on $G$ and spits out the velocity tangent vector of that trajectory with respect that coordinate time.

This is really what "parallel transport" of 1-forms means: find the trajectory such that its velocity is at every point prescribed by the given 1-form.

Think in the case $X=\mathbb{R}$ of the functor as describing a particle which propagates on a group manifold. The fact that the functor is smooth says that we have a smooth trajectory. The fact that it is functorial means that this trajectory is obtained by integrating a velocity 1-form.

Now, in my comment which started this discussion I next said that on 2-cells our parallel transport computes the "exterior acceleration": given a 1-parameter family of trajectories, the 2-form that controls the value of a smooth 2-functor on it is the exterior differential of the "velocity 1-form". 

At first it is admittedly a bit of a stretch as far as the Newtonmian concept of acceleration goes to call this curvature 2-form the "acceleration" here, though it does consist of second derivatives of the original trajectories.

But then notice the Newton-force law for charged relativitic particles: the Lorentz-force law. it says that the acceleration bivector  $\dot{v} v$ of the relativistic particle equals the (electric component of) the curvature 2-form. So we have

$$\array{
fiber & inner degrees of freedom at given position \\ connection & action functional in terms of velocity \\ curvature & force law in terms of acceleration.
}$$

There must be better ways to say this. But maybe this helps to indicate what I am thinking of.

#References#

* [Orbifold String Topology: Paths in Smooth Categories](http://golem.ph.utexas.edu/string/archives/000735.html)
* [A connection whose curvature is the Lie bracket](http://arxiv.org/abs/0803.3321)
* [Spacetime Calculus](http://modelingnts.la.asu.edu/html/STC.html)

category: drafts