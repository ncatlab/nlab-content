{:myproof: .proof style="margin-left:2em;"}
{:mynumdef: .num_defn style="border:solid #cccccc;border-width:2px 1px;padding:0 1em;margin:0 1em;"}
{:goal: .un_remark style="border:solid #0000cc;background: #add8e6;border-width:2px 1px;padding:0 1em;margin:0 1em;"}


#Examples of [[Frölicher Spaces]]#
* automatic toc
{:toc}

## Manifolds as Fr&#246;licher Spaces ##

Any [[smooth manifold]] defines a Fr&#246;licher space with curves $C^\infty(\mathbb{R}, M)$ and functions $C^\infty(M, \mathbb{R})$.

## The Pinched Plane ##

Taking quotients in the category of Fr&#246;licher spaces is straightforward: the smooth functions are those that pull-back to smooth functions on the original space.

   As an example, consider the plane $\mathbb{R}^2$ quotiented out by the $x$-axis.

   +-- {: #quotientx style="text-align:center"}
   <svg width="188" height="197" xmlns="http://www.w3.org/2000/svg" se:nonce="83381" xmlns:se="http://svg-edit.googlecode.com" xmlns:xlink="http://www.w3.org/1999/xlink">
   <!-- Created with SVG-edit - http://svg-edit.googlecode.com/ -->
   <g>
   <title>Layer 1</title>
   <line fill="none" stroke-width="2" stroke="#000000" id="svg_83381_1" y2="1" x2="183" y1="1" x1="1"/>
   <line id="svg_83381_2" fill="none" stroke-width="2" stroke="#000000" y2="195" x2="187" y1="195" x1="5"/>
    <path id="svg_83381_3" d="m2,2c2,157 181,35 185,193" stroke-width="2" stroke="#000000" fill="none"/>
    <path id="svg_83381_4" d="m182,2c5,173 -179,18 -177,194" stroke-width="2" stroke="#000000" fill="none"/>
    <path id="svg_83381_5" d="m39,2c3,167 107,25 109,192" stroke-width="2" stroke="#9b9b9b" fill="none"/>
    <path id="svg_83381_6" d="m136,2c5,175 -86,17 -85,193" stroke-width="2" stroke="#9b9b9b" fill="none"/>
    <line fill="none" stroke-width="2" stroke="#9b9b9b" id="svg_83381_7" y2="193.99999" x2="96" y1="2" x1="94"/>
   </g>
   </svg>
   =--

   Let us write this as $X$.
This example is closely related to taking cones and suspensions in algebraic topology.
The smooth functions on $X$ are simple to describe: the set is equivalent to those smooth functions $\mathbb{R}^2 \to \mathbb{R}$ which are constant on the $x$-axis.

   Now let us consider the smooth curves.
Let $\alpha : \mathbb{R} \to X$ be a smooth curve.
We can partition $\mathbb{R}$ into two pieces: those points that are mapped to the squashed point in $X$ and those points that aren't.
Let us write $A$ for the set of points that are __not__ mapped to the squashed point.
Using bump functions it is easy to show that $A$ is open in $\mathbb{R}$.
As the quotient map $\mathbb{R}^2 \to X$ is bijective off the $x$-axis, the restriction of $\alpha$ to $A$ has a unique lift to $\mathbb{R}^2$.
Let us write $\alpha_x$ and $\alpha_y$ for the coordinate functions of this lift.
Again using bump functions, it is easy to show that $\alpha_x$ and $\alpha_y$ are smooth on $A$.
Furthermore, as the projection $(x,y) \mapsto y$ descends to a smooth function on $X$, $\alpha_y$ is actually the restriction to $A$ of a smooth function $\mathbb{R} \to \mathbb{R}$ which we shall also denote by $\alpha_y$.
Note that $A = \alpha_y^{-1}(0)$.

   The interesting part comes when looking at what happens to $\alpha_x$ at the boundary of $A$.
As $A$ is open, it is a disjoint union of open intervals.
The boundaries of each of these intervals forms part of the boundary of $A$ and it is simplest to start with these points.
For further simplicity, let us assume that $(0,1)$ is one of the components of $A$ and we are considering the boundary point $0$.
Thus we wish to consider $\lim_{t \to 0^+} \alpha_x(t)$.

   The general rule is simple to state: $\alpha_y$ must go to zero faster than $\alpha_x$ (and any of its derivatives) can go to infinity.

## Coequaliser Example ##

Let us give an example that shows that the category of Fr&ouml;licher spaces is not [[locally cartesian closed category|locally cartesian closed]].
Consider a [[coequaliser]] diagram $\mathbb{R} \setminus \{0\} \to \mathbb{R} \amalg \mathbb{R}$ where the two maps are the inclusions into the two cofactors.

   <svg width="507" height="252" xmlns="http://www.w3.org/2000/svg" se:nonce="83382" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:se="http://svg-edit.googlecode.com">
   <!-- Created with SVG-edit - http://svg-edit.googlecode.com/ -->
   <defs>
   <marker viewBox="0 0 10 10" id="se_arrow_83382_fw1" refY="5" markerUnits="strokeWidth" markerWidth="5" markerHeight="5" orient="auto" refX="8">
   <path d="m0,0l10,5l-10,5l5,-5l-5,-5z" fill="#930000"/>
   </marker>
   <marker viewBox="0 0 10 10" id="se_arrow_83382_fw2" refY="5" markerUnits="strokeWidth" markerWidth="5" markerHeight="5" orient="auto" refX="8">
   <path d="m0,0l10,5l-10,5l5,-5l-5,-5z" fill="#000093"/>
   </marker>
   </defs>
   <g>
   <title>Layer 1</title>
   <line x1="155.5" y1="98.5" x2="306.5" y2="30.5" stroke="#000000" stroke-width="5" fill="none" id="svg_83382_3"/>
   <line x1="147.5" y1="249.5" x2="298.5" y2="181.5" stroke="#000000" stroke-width="5" fill="none" id="svg_83382_5"/>
   <line x1="2.5" y1="68.5" x2="71.5" y2="37.5" id="svg_83382_7" stroke="#000000" stroke-width="5" fill="none"/>
   <line x1="82.5" y1="33.5" x2="151.5" y2="2.5" stroke="#000000" stroke-width="5" fill="none" id="svg_83382_8"/>
   <path fill="none" stroke="#930000" stroke-width="2" d="m89.5,38.5c41,-19 88,-14 113,-6" id="svg_83382_9" marker-end="url(#se_arrow_83382_fw1)"/>
   <path fill="none" stroke="#930000" stroke-width="2" d="m86.5,42.5c24,24 46,33 95,34" id="svg_83382_10" marker-end="url(#se_arrow_83382_fw1)"/>
   <line x1="152.5" y1="75.5" x2="303.5" y2="7.5" id="svg_83382_1" stroke="#000000" stroke-width="5" fill="none"/>
    <line x1="240.64777" y1="78.3657" x2="414.16693" y2="31.72597" stroke="#930000" stroke-width="2" fill="none" marker-end="url(#se_arrow_83382_fw1)" id="svg_83382_11" transform="rotate(14.9951, 327.408, 55.0469)"/>
    <line x1="78.5" y1="46.5" x2="201.5" y2="209.5" id="svg_83382_12" stroke="#000093" stroke-width="2" fill="none" marker-end="url(#se_arrow_83382_fw2)"/>
   <line x1="236.5" y1="75.5" x2="208.5" y2="205.5" id="svg_83382_13" stroke="#000093" stroke-width="2" fill="none" marker-end="url(#se_arrow_83382_fw2)"/>
   <line x1="421.5" y1="74.5" x2="218.5" y2="205.5" id="svg_83382_14" stroke="#000093" stroke-width="2" fill="none" marker-end="url(#se_arrow_83382_fw2)"/>
   <ellipse cx="429.5" cy="53.5" id="svg_83382_15" fill="#000000" stroke="#000000" stroke-width="2" rx="3" ry="4"/>
   <line x1="355.5" y1="93.5" x2="424.5" y2="62.5" stroke="#000000" stroke-width="5" fill="none" id="svg_83382_17"/>
   <line x1="435.5" y1="58.5" x2="504.5" y2="27.5" stroke="#000000" stroke-width="5" fill="none" id="svg_83382_18"/>
   <ellipse cx="431.5" cy="67.5" fill="#000000" stroke="#000000" stroke-width="2" rx="3" ry="4" id="svg_83382_19"/>
   </g>
   </svg>
   
   The coequaliser of this diagram is $\mathbb{R} \cup \{*\}$ where the $*$ is a doubled-point at $0$.  (So this is the well-known example of a non-Hausdorff [[manifold]].)
Thus any smooth function $\psi : \mathbb{R} \cup \{*\} \to \mathbb{R}$ has to satisfy $\psi(0) = \psi(*)$, which means that any smooth curve $\alpha : \mathbb{R} \to \mathbb{R} \cup \{*\}$ can choose whether to pass through $0$ or $*$ completely arbitrarily.

   We consider this as a coequaliser of spaces over $\mathbb{R}$ by taking the obvious map to $\mathbb{R}$ in each case.
The colimit is the same whether we work in the full category of Fr&ouml;licher spaces or just those over $\mathbb{R}$.

   Now let $Y$ be any Fr&ouml;licher space and consider it as a space over $\mathbb{R}$ via the [[constant function|constant]] zero map, $\omicron : Y \to \mathbb{R}$.
We take the [[fibred product]] over $\mathbb{R}$ of the coequaliser diagram.
Since $\mathbb{R} \setminus \{0\}$ has no points mapping to $0$, $(\mathbb{R} \setminus \{0\}) \times_{\mathbb{R}} Y = \emptyset$.
For the third space, we see that $(\mathbb{R} \amalg \mathbb{R}) \times_{\mathbb{R}} Y = Y \amalg Y$.
Thus the coequaliser diagram is now $\emptyset \to Y \amalg Y$.
The coequaliser is thus $Y \amalg Y$.
Note that smooth curves into $Y \amalg Y$ are of the form $(i, \beta)$ where $i$ is a constant in $\{0,*\}$ that distinguishes the cofactors and $\beta : \mathbb{R} \to Y$ is a smooth curve in $Y$.

   Let us consider the product over $\mathbb{R}$ of $\mathbb{R} \cup \{*\}$ with $Y$.
As a set, this is just $Y \amalg Y$ again.
However, as a Fr&ouml;licher space it has different functions to those on $Y \amalg Y$.
The product over $\mathbb{R}$ is a subspace of $(\mathbb{R} \cup \{*\}) \times Y$ and thus a curve into it is smooth if and only if it is smooth into $(\mathbb{R} \cup \{*\}) \times Y$, whence it is smooth if and only if the projections to $\mathbb{R} \cup \{*\}$ and to $Y$ are smooth.
As we are considering curves in $(\mathbb{R} \cup \{*\}) \times_\mathbb{R} Y$, the projection to $\mathbb{R} \cup \{*\}$ must have image in $\{0,*\}$.
Thus _any_ curve is allowed by this and so the smooth curves into $(\mathbb{R} \cup \{*\}) \times_\mathbb{R} Y$ are of the form $(\alpha, \beta)$ where $\alpha$ is *any* function from $\mathbb{R}$ into $\{0,*\}$ and $\beta : \mathbb{R} \to Y$ is a smooth curve in $Y$.

   +-- {: .query}
   I notice that in some classically false versions of [[constructive mathematics]], the only functions from $\mathbb{R}$ to $\{0,*\}$ are the constant ones.  It would be nice if there were a nonclassical [[dream mathematics|dream universe]] in which the category of Fr&#246;licher spaces were locally cartesian closed!  Unfortunately, the counterexample can be saved by using a continuously parametrised coproduct $\coprod_{\mathbb{R}} \mathbb{R}$ instead of $\coprod_{\{0,*\}} \mathbb{R} = \mathbb{R} \amalg \mathbb{R}$.  ---Toby

   [[Andrew Stacey]] I think I'd be disappointed if locally cartesian became a property of what set theory was being used!  I suspect that the real reason this example works is the fact that $Y \to \mathbb{R}$ has such bad path-lifting properties and the coequaliser diagram that I chose is just a simple one that demonstrates it.

   I've been pondering how one might fix this.  I ought to write up Kriegl and Michor's extension of a manifold as, although they haven't done much with it, it contains some ideas that may be of interest.  What makes me think of it here is that that definition of a manifold (which isn't, by the way, the one in their weighty tome) has two parts: a space and its tangent space, and relationships between them.  This suggests that a smooth space, of whatever variety, should be more than just one space but some sort of diagram of spaces.

   This is also suggested by trying to generalise the Frolicher "idea" to non-set-based theories.  It's not immediately obvious how to make the saturation condition work, but the basic idea is to have objects as $(C,F,c)$ with $c : C \times F \to Hom$ and morphisms as $f : C_X \times F_Y \to Hom$.  The saturation condition, whatever it is, is what is needed to make this into a category.  So here it's obvious that objects are just special morphisms.  Feeding this back into the definition you get a glimmer of an idea that maybe a morphism (let me go back to genuine Frolicher spaces here for clarity) $f : X \to Y$ needs some sort of saturation condition as well as a compatibility condition.
   =--

   This is not the same as $Y \coprod Y$ and thus the functor $- \times_{\mathbb{R}} Y$ does not preserve colimits.
It cannot, therefore, be a left adjoint and so the category of Fr&ouml;licher spaces is not locally cartesian closed.

   This example works because of the structure of $\mathbb{R} \cup \{*\}$.
If one were to work in an "input only" category, then the structure on $\mathbb{R} \cup \{*\}$ would be determined by those curves which lift to $\mathbb{R} \coprod \mathbb{R}$.
Such maps could not arbitrarily swap between $0$ and $*$ because up in $\mathbb{R} \coprod \mathbb{R}$ these two points are far apart.
Thus the subspace structure on $\{0,*\}$ in an "input only" category is _discrete_.
However, in the category of Fr&ouml;licher spaces the outputs control the behaviour of quotients.
Functions out of $\mathbb{R} \cup \{*\}$ cannot detect the difference between $0$ and $*$.
Thus curves into $\mathbb{R} \cup \{*\}$ are allowed to swap between them with aplomb.
The subspace structure on $\{0,*\}$ is thus the _indiscrete_ structure.

   Working in the category of _Hausdorff_ Fr&ouml;licher spaces (see [below](#hausdorff)) does not improve matters.
Then we need to replace each coequaliser but its Hausdorffification.
Now the distinction is clear since taking the product and then the coequaliser yields $Y \coprod Y$ as before but taking the coequaliser and then the product yields just $Y$.

   It is also worth pointing out that with the modification of the previous paragraph, this example only involves manifolds (assuming that $Y$ is chosen to be a manifold).  It therefore shows that a category extending that of smooth manifolds can __either__ be locally cartesian closed __or__ preserve limits and colimits from manifolds _but not both_.
