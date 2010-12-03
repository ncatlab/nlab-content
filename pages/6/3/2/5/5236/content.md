## Progress graphs

# Contents
* automatic table of contents goes here
{:toc}
## Idea. 
**Progress graphs** are a simple model for a certain aspect of concurrency theory in Computer Science. The basic idea is to give a description of what can happen when several processes are modifying shared resources.  Given a shared resource, $a$, we consider it as a semaphore which controls its behaviour with respect to processes. (This is a bit like the counter or token used in some old single track railway systems to prevent two trains being on the same stretch of line at the same time.) We are not worried exactly how the resource is used merely the 'locking' and 'unlocking' of the access to that resource.  For instance, $a$ may be a shared variable, so a semaphore is used to ensure that only one process can write on it at a time. (Editing pages in the n-Lab is another example!)

Our system will have $n$ deterministic sequential processes $Q_1, \ldots, Q_n$ Each will be abstracted as a sequence of 'locks' (denoted $P$) or 'unlocks' (denoted $V$) applied to shared resources (denoted $a$ with suffices and superfixes to distinguish them), so $Q_i = R^1a^1_i.R^2a^2_i\ldots R^{n_i}a^{n_i}_i$, as so one. Here each $R$ is an occurrence of a $P$ or a $V$.

There is a natural way to understand the possible behaviours of the concurrent execution of these processes. We associate to each process a different coordinate  direction in the topological space, $\mathbb{R}^n$. The state of the system corresponds to a point in $\mathbb{R}^n$ whose $i^{th}$ coordinate describes the state or  'local time' of the  $i^{th}$ process.

We assume that each process starts at (local time) 0 and finishes at (local time) 1; the $P$ and $V$ actions correspond to sequences of real numbers between 0 and 1, which reflect the order of the $P$s and $V$s.  The initial state is $(0,\ldots,0)$ and the final state $(1,\ldots, 1)$.

To look at a particular example more closely, we suppose $n = 2$ and the two processes look like $T_1= P a.P b.V b.V a$ and $T_2 = P b.P a.V a.V b$.  This gives rise to the two dimensional progress graph below:



<svg
   xmlns:dc="http://purl.org/dc/elements/1.1/"
   xmlns:cc="http://creativecommons.org/ns#"
   xmlns:rdf="http://www.w3.org/1999/02/22-rdf-syntax-ns#"
   xmlns:svg="http://www.w3.org/2000/svg"
   xmlns="http://www.w3.org/2000/svg"
   xmlns:sodipodi="http://sodipodi.sourceforge.net/DTD/sodipodi-0.dtd"
   xmlns:inkscape="http://www.inkscape.org/namespaces/inkscape"
   width="401.625"
   height="401.625"
   id="svg2"
   sodipodi:version="0.32"
   inkscape:version="0.46"
   sodipodi:docname="swiss-flag.svg"
   inkscape:output_extension="org.inkscape.output.svg.inkscape"
   version="1.0">
  <defs
     id="defs4">
    <inkscape:perspective
       sodipodi:type="inkscape:persp3d"
       inkscape:vp_x="0 : 526.18109 : 1"
       inkscape:vp_y="0 : 1000 : 0"
       inkscape:vp_z="744.09448 : 526.18109 : 1"
       inkscape:persp3d-origin="372.04724 : 350.78739 : 1"
       id="perspective10" />
  </defs>
  <sodipodi:namedview
     id="base"
     pagecolor="#ffffff"
     bordercolor="#666666"
     borderopacity="1.0"
     gridtolerance="10000"
     guidetolerance="10"
     objecttolerance="10"
     inkscape:pageopacity="0.0"
     inkscape:pageshadow="2"
     inkscape:zoom="0.35355339"
     inkscape:cx="246.70904"
     inkscape:cy="508.22482"
     inkscape:document-units="px"
     inkscape:current-layer="layer1"
     showgrid="true"
     inkscape:window-width="663"
     inkscape:window-height="701"
     inkscape:window-x="0"
     inkscape:window-y="22">
    <inkscape:grid
       type="xygrid"
       id="grid2383"
       visible="true"
       enabled="true" />
  </sodipodi:namedview>
  <metadata
     id="metadata7">
    <rdf:RDF>
      <cc:Work
         rdf:about="">
        <dc:format>image/svg+xml</dc:format>
        <dc:type
           rdf:resource="http://purl.org/dc/dcmitype/StillImage" />
      </cc:Work>
    </rdf:RDF>
  </metadata>
  <g
     inkscape:label="Layer 1"
     inkscape:groupmode="layer"
     id="layer1"
     transform="translate(-79.25,-91.612183)">
    <rect
       style="fill:none;stroke:#050803;stroke-width:1.5;stroke-miterlimit:4;stroke-dasharray:none;stroke-dashoffset:0;stroke-opacity:1"
       id="rect2385"
       width="400"
       height="400"
       x="80.125"
       y="92.487183" />
    <path
       style="fill:none;stroke:#050803;stroke-width:1;stroke-miterlimit:4;stroke-dasharray:none;stroke-dashoffset:0;stroke-opacity:1"
       d="M 240,172.36218 L 320,172.36218 L 320,252.36218 L 400,252.36218 L 400,332.36218 L 320,332.36218 L 320,412.36218 L 240,412.36218 L 240,332.36218 L 160,332.36218 L 160,252.36218 L 240,252.36218 L 240,172.36218 z"
       id="path2381" />
    <path
       style="fill:#000000;fill-opacity:0.52999998;stroke:#050803;stroke-width:2.82842708;stroke-miterlimit:4;stroke-dasharray:none;stroke-dashoffset:0;stroke-opacity:1"
       d="M 241.61787,371.37325 L 241.61787,331.77527 L 202.01989,331.77527 L 162.42191,331.77527 L 162.42191,293.5915 L 162.42191,255.40773 L 202.01989,255.40773 L 241.61787,255.40773 L 241.61787,214.39554 L 241.61787,173.38335 L 279.80164,173.38335 L 317.9854,173.38335 L 317.9854,214.39554 L 317.9854,255.40773 L 357.58338,255.40773 L 397.18136,255.40773 L 397.18136,293.5915 L 397.18136,331.77527 L 357.58338,331.77527 L 317.9854,331.77527 L 317.9854,371.37325 L 317.9854,410.97123 L 279.80164,410.97123 L 241.61787,410.97123 L 241.61787,371.37325 z"
       id="path2383" />
    <path
       style="fill:none;fill-opacity:0.52999998;stroke:#050803;stroke-width:1.5;stroke-miterlimit:4;stroke-dasharray:none;stroke-dashoffset:0;stroke-opacity:1"
       d="M 80,492.36218 L 160,172.36218 L 480,92.362183 L 478.00418,102.01067 L 400,412.36218 L 80,492.36218 z"
       id="path3155" />
  </g>
</svg>

The shaded area in the picture represents those states that correspond to 'mutual exclusion'. Suppose we look at a state $(x,y)$ with $Pb\lt x\lt Vb$, but $Pb\lt y\lt Vb$.  In such a state, both $T_1$ and $T_2$ have acquired $b$ and not yet relinquished it, which is impossible since $b$ can only be viewed by at most on process at any time.  Such states are in the **forbidden region**.

##Formalising $PV$-programs##
The PV language was introduced in 1968 by [[E. W. Dijkstra]] as an example 
of a toy language allowing concurrent execution of sequential processes . 
The PV language offers only two instructions called ${P}$ and ${V}$ as abbreviations for the Dutch terms _Prolaag_, short for _probeer te verlagen_, literally "try to reduce,"  and _Verhogen_ ("increase"). 

Let $S$ be a set whose elements 
are called the _semaphores_. Each semaphore _s_ is associated with an _arity_ that 
is an integer $\alpha_s\geq 2$. We suppose that for each integer $\alpha  \geq 2$, there exist 
infinitely many semaphores whose arity is $\alpha$. The only instructions are ${P}(s)$ 
and ${V}(s)$, where $s$ is some semaphore. The terms, $\mathbb{P}$, of the language, called _processes_, are the 
finite sequences of instructions. When $\mathbb{P}$ is a process and $j$, an integer less or 
equal to the length of $\mathbb{P}$, we denote by $\mathbb{P}(j )$ the $j^{th}$ instruction of the process, 
in particular $\mathbb{P}(1)$ is the first instruction. 

We will separate the instructions of a process by a dot, mostly in order to make 
them easier to read. For example we have the processes 

$${P}(a).{V}(a)$$ 

$$P(a).P(b).V(a).V(b)$$
 as we discussed more informally earlier. 



##Formalising $PV$-programs and their semantics##

+--{: .un_defn}
######Definition######
A **PV program** is a finite sequence of processes separated by the operator 
$\mid$, which should be read _run concurrently with_.
=--


For instance,  ${P}(a).{V}(a) | {P}(a).{V}(a) $
is an example of a PV program made of two copies of a process, whilst 
$${P}(a).{P}(b).{V}(a).{V}(b) | {P}(b).{P}(a).{V}(b).{V}(a)$$ 
is an example made of two distinct processes. 

(To be continued.)

##References##

This entry is partially adapted from the treatment of the idea in the following paper:)

 *  [[Eric Goubault]], [[Some geometric perspectives in concurrency theory]], 


and from 


* [[Emmanuel Haucourt]], [Concurrency and Directed Algebraic Topology](http://www.lix.polytechnique.fr/Labo/Emmanuel.Haucourt/uploads/lectures-cdat.pdf), Notes &#201;cole Polytechique, Jan.  2010.