#General idea#

A bundle gerbe is a categorification of a transition function of a fiber bundle. For that reason, it is sometimes also addressed as a transition bundle.

Despite its name, a bundle gerbe is not a [[gerbe]]. A gerbe is rather a categorification of the sheaf of sections of a fiber bundle.

A fiber bundle can be characterized (up to isomorphism) 
in several different ways, for instance as

<ul>
 <li>
   a fibration,
 </li>
 <li>
   a sheaf of sections,
 </li>
 <li> 
   a transition function,
 </li>
 <li> 
   an Atiyah groupoid extension.
 </li>
</ul>
If it is a principal $U(1)$-bundle or a complex line bundle, it can also be characterized as
<ul>
 <li>
  an element in second integral cohomology.
 </li>
</ul>

Each of these descriptions has a categorification. They go, respectively, by the name

<ul>
 <li>
   a 2-bundle,
 </li>
 <li>
   a gerbe,
 </li>
 <li> 
   a bundle gerbe,
</li>
 <li> 
   an Atiyah 2-groupoid extension,
 </li>
 <li>
  an element in third integral cohomology.
 </li>
</ul>

The degree to which these have been 
studied and understood differs. In as far as they have been understood, one finds essentially the expected equivalences.

In particular, bundle gerbes are equivalent to a certain sub(-2-)category of gerbes, and are classified by third integral cohomology.

This cohomological classification has, historically, been one of the main motivations for the development of gerbes and bundle gerbes. For that reason, bundle gerbes are sometimes addressed as a "geometric realization of third integral cohomology", in the same sense that complex line bundles are a "geometric realization of second integral cohomology".

Of course this classification by integral cohomology applies only to what should be more precisely called <em>complex line bundle gerbes</em> or $U(1)$-principal bundle gerbes, which were introduced by Murray. Other notions of bundle gerbes can be defined, and in particular nonabelian principal bundle gerbes have been studied by Aschieri-Cantini--Jur&ccaron;o.

It turns out that line bundle gerbes can alternatively be regarded as central extensions of groupoids. This is not to be confused with the (2-)groupoid extension mentioned above.


<br/><strong>Definition.</strong>

A bundle gerbe over a space $X$ is 

<ul>
  <li>
    a regular epimorphism
    $$
      \array{
          Y
          \\
          \pi \downarrow
          \\
          X
      }
    $$
  </li>
  <li>
    a fiber bundle
    $$
        \array{
           B
           \\
           p \downarrow \;\;
           \\
           Y^{[2]}
        }
    $$
     over the fiber product $Y^{[2]}$ of $Y$ with itself, i.e.
    $$
      \array{
          L
          \\
          p \downarrow \;\;
          \\
          Y^{[2]} &\stackrel{\rightarrow}{\rightarrow}& Y
          \\
          && \pi \downarrow \;\;
          \\
          && 
          X
      }
     \,,
    $$
   together with a notion of product $\otimes$ of fibers of $B$;
  </li>   
  <li>
    on $Y^{[3]}$ an isomorphism
   $$
     \mu : \pi_{12}^*B \;\otimes\; \pi_{23}^*B \;\stackrel{\sim}{\to}\; \pi_{13}^* B
     \,,
   $$
    which satisfies an associativity relation on $Y^{[4]}$.
   Here $\pi_{12}, \pi_{23}, \pi_{13}$ are the three obvious maps
    $$
       Y^{[3]} \stackrel{\stackrel{\rightarrow}{\rightarrow}}{\rightarrow}
       Y^{[2]}
       \,.
    $$
  </li>
</ul>

For line bundle gerbes, $X$ is taken to be a smooth space, $\pi : Y \to X$ 
a surjective submersion, $B$ a smooth line bundle and $\mu$ a smooth
isomorphism. This case was introduced by Murray in 
<a href="http://arxiv.org/abs/dg-ga/9407015">dg-ga/9407015</a>.


For (nonabelian) $G$-principal bundle gerbes, one chooses $B$ to be a 
$G$-principal bibundle, which is a bundle that is $G$-principal both
for a left and a right $G$ action, which mutually commute. In other words,
the fibers of $B$ are $G$-bitorsors. This allows to define the product as
$$
  p_{12}^* B \;\otimes\; p_{23}^* B \;:=\; p_{12}^* B \;\times_G\; p_{23}^* B
  \,.
$$
This case was introduced by Aschieri, Cantini &amp; Jur&ccaron;o in
<a href="http://arxiv.org/abs/hep-th/0312154">hep-th/0312154</a>.

For complex line bundle gerbes
the above definition can be understood as obtained from the definition of a transition
function of a line bundle by replacing the monoid of complex numbers 
by the monoidal category of 1-dimensional complex vector spaces;
and by replacing equations between numbers by coherent (here: associative)
isomorphisms of vector spaces. 

Such a replacement is known as categorification.

Analogously, for principal bundle gerbes 
the above definition can be understood as obtained from the definition of a transition
function of a principal $G$-bundle by replacing the group $G$
by the 2-group 
$$
  G\mathrm{BiTor}
$$
of $G$-bitorsors,
and by replacing equations between group elements by coherent (here: associative)
isomorphisms of bitorsors. 


<br/><em>Interpretation in terms of categorified transition functions.</em>

In order to see this more explicitly, consider the special case where $Y = \mathbf{U}$
is a good covering of $X$ by open contractible sets $\{U_i\}$
$$
  Y := \sqcup_i U_i
  \,,
$$ 
with
$$
\array{
  Y 
  \\
  \downarrow
  \\
  X
}
$$
being the obvious map which embeds a point in $U_i \subset X$ into $X$. Then
$Y^{[2]}$ is the disjoint union of double intersections of these open sets
$$
  Y^{[2]} = \sqcup_{i,j} U_i \cap U_j
  \,.
$$

The transition function of a local trivialization with respect to $Y$ of a complex 
line bundle on $X$ is nothing but a complex function 
$$
  g : Y^{[2]} \to \mathbb{C}
  \,.
$$
satisfying
$$
  g_{ij} g_{jk} = g_{ik}
$$
on each triple intersection $U_i \cap U_j \cap U_k$,
where $g_{ij}$ denotes the restriction of $g$ to to $U_i \cap U_j \subset Y^{[2]}$.

This is equivalent to saying that
$$
  p_{12}^* g \, p_{23}^* g = p_{13}^* g
  \,.
$$
Replacing this equation of (functions with values in) complex numbers by a coherent isomorphism of complex 1-dimensional vector spaces leads to the definition of a line bundle gerbe.

<br/><em>Interpretation in terms of groupoid extensions.</em>

To any morphism
$$
  Y \to X
$$
in a category with pullbacks, we may associate the groupoid
$$
  Y^\bullet := Y^{[2]} \stackrel{\to}{\to} Y
$$
whose object of objects is $Y$, whose object of morphisms is $Y^{[2]}$ and whose
composition law is given by the unique vertical morphsim in
$$
\array{
   &     &      & Y^{[3]}
  \\
  &  & \swarrow &&\searrow
  \\
  & Y^{[2]} & &&&  Y^{[2]}
  \\
  &\swarrow&  &&& \searrow
  \\
  Y &&& \downarrow &&& Y
  \\
  & \nwarrow &&&& \nearrow
  \\
  &&& Y^{[2]}
}
 \,.
$$

For instance, for $\pi : Y \to X$ a surjective submersion, the objects of $Y^\bullet$ are the points
of $Y$, and there is a unique morphism $y_1 \to y_2$ whenever $\pi(y_1) = \pi(y_2)$.

The above definition of a bundle gerbe can be understood as an <em>enrichment</em>
of this groupoid in the sense of enriched categories. For line bundle gerbes the enrichment
is over $1D\mathrm{Vect}$, for principal bundle gerbes the enrichment is over 
$G\mathrm{BiTor}$.

For line bundle gerbes this is often expressed as saying that a line bundle gerbe is
a $U(1)$-central extension of $Y^\bullet$.

##Connection on a bundle gerbe##

Like bundle gerbes are a categorification of transitions in fiber bundles,
bundle gerbes with connection are a categorification of transitions in
fiber bundles with connection.

Like a connection on a locally trivialized bundle is encoded in a 
Lie algebra-valued connection 1-form on $Y$, the connection on a bundle gerbe 
gives rise to a Lie-algebra valued 2-form on $Y$ (this shift in degree
is directly related to the step from second to third integral cohomology). This 2-form
is sometimes addressed as the <em>curving</em> 2-form of a bundle gerbe.

But there is more data necessary to describe a connection on a bundle gerbe.
The details of the definition - which is evident for line bundle gerbes but more
involved for principal bundle gerbes - can be naturally derived from a functorial
concept of parallel surface transport, just like connection 1-forms on bundles
can be derived from parallel line transport.

<br/><strong>Connection on a bundle gerbe - Definition.</strong>

<em>Line bundle gerbes.</em>

A connection (also known as "connection and curving") on a line bundle
gerbe
$$
  B \stackrel{p}{\to} Y^{[2]} \stackrel{\to}{\to} Y \stackrel{\pi}{\to} X
$$ 
is

<ul>
  <li>
    a 2-form on $Y$
    $$
      B \in \Omega^2(Y)
    $$
  </li>
  <li>
    a connection $\nabla$ on the line bundle $B \to Y^{[2]}$
  </li>
  <li>
   such that
   $$
      \pi_1^*B \; -\;  p_2^*B \;=\; F_\nabla
   $$
  </li>
  <li>
    together with an extension of the bundle gerbe product $\mu$ to an isomorphism
    $$
        \mu_\nabla \;:\; p_{12}^* (B,\nabla) \;\; \otimes p_{23}^* (B,\nabla) \;\to\; p_{13}^* (B,\nabla)
    $$
    of line bundles with connection.
  </li>
</ul>



Notice that this condition ensures that $d B$ is a 3-form on $Y$ which agrees on
double intersections
$$
  p_1^* d B \;\; = \;\; p_2^* d B
  \,.
$$
This means that $d B$ actually descends to a 3-form on $X$.

The <strong>curvature</strong> associated with the connection on a line bundle gerbe 
is the unique 3-form on $X$
$$
  H \in \Omega^3(X)
$$
such that
$$
  \pi^* H = d B
  \,.
$$

The deRham class $[H]$ of this 3-form is the image in real cohomology of the class in integral coholomology classifying the bundle gerbe.

<br/><em>Principal bundle gerbes.</em>

A connection on a $G$-principal bundle gerbe is

<ul>
  <li>
    a $\mathrm{Lie}(G)$-valued 2-form on $Y$
    $$
       B \in \Omega^2(Y,\mathrm{Lie}(G))
    $$
  </li>
  <li>
    together with a $\mathrm{Lie}(\mathrm{Aut}(G))$-valued 1-form on $Y$
    $$
       A \in \Omega^1(Y,\mathrm{Lie}(\mathrm{Aut}(G)))
    $$
  </li>
  <li>
    and a certain twisted notion of connection on the $G$-bundle $B$
  </li>
  <li>
    satisfying a couple of conditions that reduce to those described above in the case
    $G = U(1)$.
  </li>
</ul>

For the case that $F_{A} + \mathrm{ad} B = 0$, these conditions are nothing but
a tetrahedron law on a 2-functor from 2-paths in $Y$ to the category 
$\Sigma(G\mathrm{BiTor})$. This is discussed in
<a href="http://arxiv.org/abs/math.DG/0511710">math.DG/0511710</a>.

For the more general case a choice for these conditions that harmonizes with the
conditions found for (proper) gerbes with connection by Breen &amp; Messing in
<a href="http://arxiv.org/abs/math.AG/0106083">math.AG/0106083</a> has
been given by Aschieri, Cantini &amp; Jur&ccaron;o in  
<a href="http://arxiv.org/abs/hep-th/0312154">hep-th/0312154</a>.

<br/>
<strong>Surface transport.</strong>

From a line bundle gerbe with connection one obtains a notion of parallel transport along surfaces in a way that generalizes the procedure for locally trivialized fiber bundles with connection.

Recall that in the case of fiber bundles, the holonomy associated to a based loop $\gamma$ is obtained by

<ul>
  <li>
     choosing a triangulation of the loop (i.e., a decomposition into intervals) such that each vertex sits in a double intersection $U_{ij}$ and such that each edge sits in a patch $U_i$ 
  </li>
  <li>
    choosing for each edge a lift into $Y = \sqcup_i U_i$
  </li>
  <li>
    choosing for each vertex a lift into $Y^{[2]} = \sqcup_{ij} U_i\cap U_j$
  </li>
  <li>
    assigning to each edge lifted to $U_i$ the transport computed from the connection 
    1-form $a_i$
  </li>
  <li>
    assigning to each vertex  lifted to $U_i \cap U_j$ the value of the transition function
    $g_{ij}$ at that point
  </li>
  <li>
    multiplying these data in the order given by $\gamma$ .
  </li>
</ul>

For bundle gerbes this generalizes to a procedure that assigns a triangulation to a closed surface, that lifts faces, edges, and vertices to single, double and triple intersections,
respectively, and which assigns the exponentiated integrals of the 2-form over faces, of the connection 1-form over edges, and assigns the isomorphism $\mu_{ijk}$ to vertices.

For the abelian case (line bundle gerbes) this procedure has been first described in

K. Gawedzki &amp; N. Reis
<br/><em>WZW branes and Gerbes</em>
<br/><a href="http://arxiv.org/abs/hep-th/0205233">hep-th/0205233</a>

based on

O. Alvarez
<br/><em>Topological quantization and cohomology.</em>
<br/> Commun. Math. Phys. 100 (1985), 279-309.

Further discussion can be found in 

A. Carey, S. Johnson &amp; M. Murray
<br/><em>Holonomy on D-branes</em>
<br/><a href="http://arxiv.org/abs/hep-th/0204199">hep-th/0204199</a>.

Gawedzki and Reis showed this way that the Wess-Zumino term in the WZW-model is nothing but the surface holonomy of a (line bundle) gerbe.

In terms of string physics this means that the string (the 2-particle) couples to the Kalb-Ramond field  - which hence has to be interpreted as the connection ("and curving") of a gerbe - in a way that categorifies the coupling of the electromagnetically charged (1-)particle to a line bundle.

The necessity to interpret the Kalb-Ramond field as a connection on a gerbe was originally discussed in

D. Freed and E. Witten
<br/><em>Anomalies in string theory with D-branes</em>
<br/> Asian J. Math. 3 (1999), 819-851.
<br/><a href="http://arxiv.org/abs/hep-th/9907189">hep-th/9907189</a>.

Underlying the Gawedzki-Reis formula is a general mechanism of transition of transport 2-functors. This applies to more general situations than ordinary line bundle gerbes with connection.

The generalization to unoriented surfaces (hence to type I strings) was given in

K. Waldorf, C. Schweigert &amp; U. S.
<br/><a href="http://golem.ph.utexas.edu/string/archives/000708.html">Unoriented WZW Models and Holonomy of Bundle Gerbes</a>
<br/><a href="http://arxiv.org/abs/hep-th/0512283">hep-th/0512283</a>.

##References##

Taken from two blog posts:

Urs Schreiber, [Bundle Gerbes: General Idea and Definition](http://golem.ph.utexas.edu/category/2006/10/bundle_gerbes.html)

Urs Schreiber, [Bundle Gerbes: Connections and Surface Transport](http://golem.ph.utexas.edu/category/2006/10/bundle_gerbes_connections_and.html)