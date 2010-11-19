## Progress graphs

# Contents
* automatic table of contents goes here
{:toc}
## Idea. 
**Progress graphs** are a simple model for a certain aspect of concurrency theory in Computer Science. The basic idea is to give a description of what can happen when several processes are modifying shared resources.  Given a shared resource, $a$, we consider it as a semaphore which controls its behaviour with respect to processes. (This is a bit like the counter or token used in some old single track railway systems to prevent two trains being on the same stretch of line at the same time.) We are not worried exactly how the resource is used merely the 'locking' and 'unlocking' of the access to that resource.  For instance, $a$ may be a shared variable, so a semaphore is used to ensure that only one process can write on it at a time. (Editing pages in the n-Lab is another example!)

Our system will have $n$ deterministic sequential processes $Q_1, \ldots, Q_n$ Each will be abstracted as a sequence of 'locks' (denoted $P$) or 'unlocks' (denoted $V$) applied to shared resources (denoted $a$ with suffices and superfixes to distinguish them), so $Q_i = R^1a^1_i.R^2a^2_i\ldots R^{n_i}a^{n_i}_i$, as so one. Here each $R$ is an occurrence of a $P$ or a $V$.

There is a natural way to understand the possible behaviours of the concurrent execution of these processes. We associate to each process a different coordinate  direction in the topological space, $\mathbb{R}^n$. The state of the system correponds to a point in $\mathbb{R}^n$ whose $i^{th}$ coordinate describes the state or  'local time' of the  $i^{th}$ process.

(To be continued... with a PICTURE! Here is the picture.)

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


##References##

(This entry is adapted from the treatment of the idea in the following paper:)

 *  [[Eric Goubault]], [[Some geometric perspectives in concurrency theory]], 
