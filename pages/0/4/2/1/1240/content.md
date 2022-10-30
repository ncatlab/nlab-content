#Idea#


Given a [[group]] $G$ with subgroup $H \hookrightarrow G$ and a [[representation]] of $H$, there is canonically induced a representation of $G$: the _induced representation_.


#Explanation#


We start with a Lie group $G$ acting smoothly and transitively on a smooth manifold $M$.  The stabilizer of your favorite point $x \in M$ will be a Lie subgroup $H \subseteq G$, and we have

$$ M \cong G/H $$

Starting from this, there's a process that takes any representation $s$ of $H$ on a vector space $V$ and turns it into a vector bundle $E$ over $M$ --- the so-called 'induced bundle'.  Even better, the group $G$ acts on this bundle, and the projection 

$$ \pi : E \to M $$

gets along with the action of $G$:

$$ \pi(g e) = g \pi(e) .$$

So, we say that $E$ is a **$G$-equivariant** vector bundle over $M$.

The 'process' described is actually a [[functor]].  

There's a category 

$$Rep(H)$$

of linear representations of $H$, and a category 

$$Vect(M,G)$$

of $G$-equivariant vector bundles over $M$.  The induced bundle construction gives a functor

$$L: Rep(H) \to Vect(M,G) $$

But, if you think about it, you'll notice there's also a functor going back the other way:

$$R: Vect(M,G) \to Rep(H) $$

If you give me a $G$-equivariant vector bundle $E$ over $M$, I can take its fiber over your favorite point $x$, and I get a vector space --- and this becomes a representation of the stabilizer group $H$, thanks to how $G$ acts on $E$.

This functor is <i>simpler</i> than the induced bundle construction!

Whenever we have functors going both ways between two categories, we should suspect that they're [[adjoint functor|adjoints]].   The simpler functor often amounts to 'forgetting' something.  This forgetful functor is usually the <i>right</i> adjoint.  It's partner going the other way, the <i>left</i> adjoint, usually involves 'constructing' something instead of 'forgetting' something.   

And indeed, that's what's happening here!
Technically, this is to say that

$$hom(L V, F) \cong hom(V, R F)$$

Here $V$ is a representation of $H$ --- note abuse of notation in calling it $V$, which is the name for the vector space on which $G$ acts, instead of the more pedantic full name for a representation, which is something like $s: G \to GL(V)$.   

Similarly, $F$ is a $G$-equivariant vector bundle over $M$ --- and this should be something like $\pi : F \to M$, or something even more long-winded that gives a name to how $G$ acts on $F$ and $M$.

$L V$ is the induced bundle corresponding to $V$.

$R F$ is the fiber of $F$ over your favorite point $x$, which becomes a representation of $G$.

And this: 

$$hom(L V, F) \cong hom(V, R F)$$

says that $G$-equivariant vector bundle maps from $L V$ to $F$ are in natural 1-1 correspondence with intertwining operators from $V$ to $R F$.  

Now, whenever you see any sort of 'forgetful' process, you should wonder if it has a left adjoint, a construction which in some loose sense is the 'reverse' of forgetting.  Why?  Because these left adjoints tend to be important.  

Endowed with this heuristic, as soon as you see there's a rather obvious 'forgetful' process that takes a $G$-equivariant vector bundle over $M$ and gives a representation of $H$ on the fiber over $x \in M$, you will seek the 'reverse' process --- and then you'll rediscover the induced bundle construction!

And why is this so great?  Well, there's also a process that takes any representation of $G$ and restricts it to a representation of $H$:

$$R': Rep(G) \to Rep(H) $$

And this too, has a left adjoint:

$$L' : Rep(H) \to Rep(G) $$

which is called the <b>induced representation</b> trick.



#Detailed description#


Given a [[group]] $G$ with a subgroup $H$, and a [[representation]] $s$ of $H$ on a vector space $V$, we define a left [[action]] of $H$ on the [[product]] $G\times V$ by $h\cdot (g, v) = (g h^{-1}, s(h)v)$.  We write $[(g,v)]$ for the orbit, or equivalence class, that contains $(g,v)$.

We then define $E = (G\times V)/H$ as the set of orbits of that [[action]] of $H$, $M = G/H$ as the set of left cosets of $H$, and the projection $\pi: E\to M$ by $\pi ([(g,v)]) = g H$, where of course it makes no difference if we re-describe the orbit $[(g,v)]$ as $[(g h^{-1}, s(h)v]$ for any $h\in H$ because $(g h^{-1}) H = g H$.

For each $x\in M$, choose $g$ to be any element of $G$ such that $x = g H$.  Define $E_x = \pi^{-1}(x)$, and $\phi_g:V\to E_x$, $\phi_g(v) = [(g,v)]$.

The map $\phi_g$ is onto:  for any $[(k,w)]\in E_{(g H)} = \pi^{-1}(g H)$, we have $k=g h_1^{-1}$ for some $h_1\in H$, so $k^{-1} g\in H$, $(k^{-1} g)\cdot (g, s(g^{-1} k)w) = (k,w)$, so $\phi_g(s(g^{-1} k)w) = [(g, s(g^{-1} k)w)] = [(k,w)]$.

The map $\phi_g$ is one-to-one:  if $\phi_g(v) = \phi_g(w)$, then $[(g,v)]=[(g,w)]$, so for some $h_1\in H$, we have $h_1\cdot (g,v) = (g,w)$, or $(g h_1^{-1}, s(h_1)v) = (g,w)$; equating the first coordinates requires $h_1=e$, and $s$ is a representation so $s(e)=1_V$, and $v=w$.

Since $\phi_g$ is a bijection between $E_x$ and the vector space $V$, we can make $E_x$ into a vector space by defining $\alpha p + \beta q \equiv \phi_g(\alpha \phi_g^{-1}(p) + \beta \phi_g^{-1}(q))$, for all $\alpha, \beta \in \mathbb{R}, p, q \in E_x$.  But is this independent of our choice of $g$?  If we chose $g h$ instead of $g$, we'd have $\phi_{g h}(v) = [(g h,v)] = [(g, s(h)v)] = \phi_g(s(h)v)$, so $\phi_{g h}=\phi_g\circ s(h)$, and $\phi_{g h}^{-1}=s(h^{-1})\circ \phi_g^{-1}$.  Then:

$\phi_{g h}(\alpha \phi_{g h}^{-1}(p) + \beta \phi_{g h}^{-1}(q)) =
(\phi_g\circ s(h))(\alpha (s(h^{-1})\circ \phi_g^{-1})(p) + \beta (s(h^{-1})\circ \phi_g^{-1})(q)) = \phi_g(\alpha \phi_g^{-1}(p) + \beta \phi_g^{-1}(q))$


in agreement with our original definition.

We define the action of $G$ on $E$ by $g_1\cdot [(g,v)] = [(g_1 g,v)]$, or in other words $g_1\cdot \phi_g(v) = \phi_{g_1 g}(v)$.
We then have:

$\pi(g_1\cdot [(g,v)]) = \pi[(g_1 g,v)] = (g_1 g) H = g_1\cdot (g H) = g_1\cdot \pi([(g,v)])$

That is, $\pi$ is a $G$-morphism.  This also means that the action maps fibers to fibers, $g_1:E_{(g H)}\to E_{g_1\cdot (g H)}$.  What's more, the action of $g_1$ restricted to the fiber $E_{(g H)}$ is $\phi_{g_1 g}\circ \phi_g^{-1}$, passing from $E_{(g H)}\to V \to E_{g_1\cdot (g H)}$, and this
is linear simply by virtue of the way we've defined the vector space operations on the $E_x$.

We get a representation $r$ of $G$ on the vector space $\Gamma(E)$ of sections of the bundle $E$ by:

$(r(g_1)f)(x) = g_1\cdot f(g_1^{-1}\cdot x)$

#Adjoint of induced bundle construction#


The induced bundle construction described above is a functor that takes representations of the stabilizer subgroup $H$ to $G$-equivariant vector bundles over $M$:

$$L: Rep(H) \to Vect(M,G) $$

There is a related functor going the other way:

$$R: Vect(M,G) \to Rep(H) $$

which restricts the action of $G$ on the whole bundle to the action of the stabilizer subgroup $H$ on the fiber over the chosen point $x$.  We now wish to show that $L$ and $R$ are adjoint functors.

<svg version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink' width='600' height='700'>
<g transform='translate(-66.000000, -5.000000)'>
<polyline fill='none' stroke-opacity='1' stroke-width='2px' stroke='rgb(0%,0%,0%)' points='113.369,252.501 257.731,252.501 ' />
<g transform='translate(92.368778, 244.501131)'>
<text x='0' y='12' font-size='12px'><tspan font-style='italic'>M</tspan></text>
</g>
<g transform='translate(127.414027, 260.501131)'>
<text x='0' y='12' font-size='12px' font-style='italic'>x</text>
</g>
<g transform='translate(100, 30)'>
<text x='39' y='16' font-size='12px'><tspan font-style='italic'>G</tspan>-equivariant</text>
<text x='0' y='32' font-size='12px'>vector bundle <tspan font-style='italic'>F</tspan>, &#x03c0;<tspan dy='5px' font-size='10px'>1</tspan><tspan dy='-5px'>: </tspan><tspan font-style='italic'>F</tspan> &#8594; <tspan font-style='italic'>M</tspan></text>
</g>
<g transform='translate(464, 30)'>
<text x='10' y='16' font-size='12px'>Representation <tspan font-style='italic'>R</tspan>(<tspan font-style='italic'>F</tspan>) of <tspan font-style='italic'>H</tspan></text>
<text x='60' y='32' font-size='12px'>on &#x03c0;<tspan dy='5px' font-size='10px'>1</tspan><tspan dy='-10px' font-size='10px'>&#8211;1</tspan><tspan dy='5px'>(</tspan><tspan font-style='italic'>x</tspan>)</text>
</g>
<polygon stroke='none' opacity='1' fill-rule='evenodd' fill='rgb(100%,100%,100%)' points='149.459,180.32 185.55,108.139 113.369,72.0486 77.2783,144.23 ' />
<polygon fill='none' stroke-opacity='1' stroke-width='2px' stroke='rgb(0%,0%,0%)' points='149.459,180.32 185.55,108.139 113.369,72.0486 77.2783,144.23 ' />
<path stroke='rgb(0%,0%,0%)' stroke-width='0.5px' opacity='1' fill='none' d='M150.488,131.222 A20.1752,20.1752 0 1 0 111.512,131.222' />
<g transform='translate(127.414027, 90.009188)'>
<text x='0' y='12' font-size='12px' font-style='italic'>h</text>
</g>
<ellipse fill='rgb(0%,0%,0%)' opacity='1' stroke='none' cx='146' cy='140' rx='3.5' ry='3.5' />
<ellipse fill='rgb(0%,0%,0%)' opacity='1' stroke='none' cx='117' cy='140' rx='3.5' ry='3.5' />
<polyline fill='none' stroke-opacity='1' stroke-width='0.5px' stroke='rgb(0%,0%,0%)' points='111.926,120.963 111.926,125.052 ' />
<polygon stroke='none' opacity='1' fill-rule='evenodd' fill='rgb(0%,0%,0%)' points='113.768,124.406 113.559,124.509 113.056,124.733 112.754,124.853 112.449,124.956 112.165,125.028 111.926,125.052 111.71,125.028 111.43,124.956 111.115,124.853 110.793,124.733 110.244,124.509 110.011,124.406 111.926,131.406 113.768,124.406 ' />
<polyline fill='none' stroke-opacity='1' stroke-width='1px' stroke='rgb(0%,0%,0%)' points='131.414,189.343 131.414,232.586 ' />
<polygon stroke='none' opacity='1' fill-rule='evenodd' fill='rgb(0%,0%,0%)' points='134.572,231.479 134.213,231.654 133.351,232.039 132.833,232.244 132.31,232.421 131.824,232.544 131.414,232.586 131.043,232.544 130.563,232.421 130.023,232.244 129.472,232.039 128.53,231.654 128.13,231.479 131.414,243.479 134.572,231.479 ' />
<g transform='translate(146.414027, 208.410633)'>
<text x='0' y='12' font-size='12px'>&#x03c0;<tspan dy='5px' font-size='10px'>1</tspan></text>
</g>
<ellipse fill='rgb(0%,0%,0%)' opacity='1' stroke='none' cx='131' cy='253' rx='3.5' ry='3.5' />
<polygon stroke='none' opacity='1' fill-rule='evenodd' fill='rgb(100%,100%,100%)' points='203.595,180.32 239.686,108.139 167.505,72.0486 131.414,144.23 ' />
<polygon fill='none' stroke-opacity='1' stroke-width='2px' stroke='rgb(0%,0%,0%)' points='203.595,180.32 239.686,108.139 167.505,72.0486 131.414,144.23 ' />
<path stroke='rgb(0%,0%,0%)' stroke-width='0.5px' opacity='1' fill='none' d='M205.488,131.222 A20.1752,20.1752 0 1 0 166.512,131.222' />
<g transform='translate(181.549774, 90.009188)'>
<text x='0' y='12' font-size='12px' font-style='italic'>h</text>
</g>
<ellipse fill='rgb(0%,0%,0%)' opacity='1' stroke='none' cx='200' cy='140' rx='3.5' ry='3.5' />
<ellipse fill='rgb(0%,0%,0%)' opacity='1' stroke='none' cx='171' cy='140' rx='3.5' ry='3.5' />
<polyline fill='none' stroke-opacity='1' stroke-width='0.5px' stroke='rgb(0%,0%,0%)' points='166.062,120.963 166.062,125.052 ' />
<polygon stroke='none' opacity='1' fill-rule='evenodd' fill='rgb(0%,0%,0%)' points='167.904,124.406 167.695,124.509 167.192,124.733 166.89,124.853 166.585,124.956 166.301,125.028 166.062,125.052 165.846,125.028 165.566,124.956 165.251,124.853 164.929,124.733 164.38,124.509 164.146,124.406 166.062,131.406 167.904,124.406 ' />
<polyline fill='none' stroke-opacity='1' stroke-width='1px' stroke='rgb(0%,0%,0%)' points='185.55,189.343 185.55,232.586 ' />
<polygon stroke='none' opacity='1' fill-rule='evenodd' fill='rgb(0%,0%,0%)' points='188.708,231.479 188.349,231.654 187.487,232.039 186.969,232.244 186.446,232.421 185.96,232.544 185.55,232.586 185.179,232.544 184.699,232.421 184.159,232.244 183.607,232.039 182.666,231.654 182.266,231.479 185.55,243.479 188.708,231.479 ' />
<g transform='translate(200.549774, 208.410633)'>
<text x='0' y='12' font-size='12px'>&#x03c0;<tspan dy='5px' font-size='10px'>1</tspan></text>
</g>
<ellipse fill='rgb(0%,0%,0%)' opacity='1' stroke='none' cx='186' cy='253' rx='3.5' ry='3.5' />
<polygon stroke='none' opacity='1' fill-rule='evenodd' fill='rgb(100%,100%,100%)' points='257.731,180.32 293.821,108.139 221.64,72.0486 185.55,144.23 ' />
<polygon fill='none' stroke-opacity='1' stroke-width='2px' stroke='rgb(0%,0%,0%)' points='257.731,180.32 293.821,108.139 221.64,72.0486 185.55,144.23 ' />
<path stroke='rgb(0%,0%,0%)' stroke-width='0.5px' opacity='1' fill='none' d='M259.488,131.222 A20.1752,20.1752 0 1 0 220.512,131.222' />
<g transform='translate(235.685520, 90.009188)'>
<text x='0' y='12' font-size='12px' font-style='italic'>h</text>
</g>
<ellipse fill='rgb(0%,0%,0%)' opacity='1' stroke='none' cx='254' cy='140' rx='3.5' ry='3.5' />
<ellipse fill='rgb(0%,0%,0%)' opacity='1' stroke='none' cx='225' cy='140' rx='3.5' ry='3.5' />
<polyline fill='none' stroke-opacity='1' stroke-width='0.5px' stroke='rgb(0%,0%,0%)' points='220.198,120.963 220.198,125.052 ' />
<polygon stroke='none' opacity='1' fill-rule='evenodd' fill='rgb(0%,0%,0%)' points='222.04,124.406 221.83,124.509 221.328,124.733 221.025,124.853 220.721,124.956 220.437,125.028 220.198,125.052 219.981,125.028 219.701,124.956 219.386,124.853 219.065,124.733 218.516,124.509 218.282,124.406 220.198,131.406 222.04,124.406 ' />
<polyline fill='none' stroke-opacity='1' stroke-width='1px' stroke='rgb(0%,0%,0%)' points='239.686,189.343 239.686,232.586 ' />
<polygon stroke='none' opacity='1' fill-rule='evenodd' fill='rgb(0%,0%,0%)' points='242.843,231.479 242.484,231.654 241.623,232.039 241.104,232.244 240.582,232.421 240.095,232.544 239.686,232.586 239.315,232.544 238.835,232.421 238.294,232.244 237.743,232.039 236.802,231.654 236.401,231.479 239.686,243.479 242.843,231.479 ' />
<g transform='translate(254.685520, 208.410633)'>
<text x='0' y='12' font-size='12px'>&#x03c0;<tspan dy='5px' font-size='10px'>1</tspan></text>
</g>
<ellipse fill='rgb(0%,0%,0%)' opacity='1' stroke='none' cx='240' cy='253' rx='3.5' ry='3.5' />
<polygon stroke='none' opacity='1' fill-rule='evenodd' fill='rgb(100%,100%,100%)' points='582.545,180.32 618.636,108.139 546.455,72.0486 510.364,144.23 ' />
<polygon fill='none' stroke-opacity='1' stroke-width='2px' stroke='rgb(0%,0%,0%)' points='582.545,180.32 618.636,108.139 546.455,72.0486 510.364,144.23 ' />
<path stroke='rgb(0%,0%,0%)' stroke-width='0.5px' opacity='1' fill='none' d='M584.488,131.222 A20.1752,20.1752 0 1 0 545.512,131.222' />
<g transform='translate(560.500000, 90.009188)'>
<text x='0' y='12' font-size='12px' font-style='italic'>h</text>
</g>
<ellipse fill='rgb(0%,0%,0%)' opacity='1' stroke='none' cx='579' cy='140' rx='3.5' ry='3.5' />
<ellipse fill='rgb(0%,0%,0%)' opacity='1' stroke='none' cx='550' cy='140' rx='3.5' ry='3.5' />
<polyline fill='none' stroke-opacity='1' stroke-width='0.5px' stroke='rgb(0%,0%,0%)' points='545.012,120.963 545.012,125.052 ' />
<polygon stroke='none' opacity='1' fill-rule='evenodd' fill='rgb(0%,0%,0%)' points='546.854,124.406 546.645,124.509 546.142,124.733 545.84,124.853 545.535,124.956 545.251,125.028 545.012,125.052 544.796,125.028 544.516,124.956 544.201,124.853 543.879,124.733 543.33,124.509 543.096,124.406 545.012,131.406 546.854,124.406 ' />
<polyline fill='none' stroke-opacity='1' stroke-width='2px' stroke='rgb(0%,0%,0%)' points='113.369,649.497 257.731,649.497 ' />
<g transform='translate(92.368778, 641.496606)'>
<text x='-20' y='12' font-size='12px'><tspan font-style='italic'>G</tspan> / <tspan font-style='italic'>H</tspan></text>
</g>
<g transform='translate(75, 430)'>
<text x='62' y='16' font-size='12px'><tspan font-style='italic'>G</tspan>-equivariant</text>
<text x='0' y='32' font-size='12px'>vector bundle <tspan font-style='italic'>L</tspan>(<tspan font-style='italic'>V</tspan>), &#x03c0;<tspan dy='5px' font-size='10px'>2</tspan><tspan dy='-5px'>: </tspan>(<tspan font-style='italic'>G</tspan>&#xd7;<tspan font-style='italic'>V</tspan>) / <tspan font-style='italic'>H</tspan> &#8594; <tspan font-style='italic'>G</tspan> / <tspan font-style='italic'>H</tspan></text>
</g>
<g transform='translate(481.500000, 430)'>
<text x='0' y='24' font-size='12px'>Representation <tspan font-style='italic'>s</tspan> of <tspan font-style='italic'>H</tspan> on <tspan font-style='italic'>V</tspan></text>
</g>
<polygon stroke='none' opacity='1' fill-rule='evenodd' fill='rgb(100%,100%,100%)' points='77.2783,505.135 149.459,469.044 185.55,541.225 113.369,577.316 ' />
<polygon fill='none' stroke-opacity='1' stroke-width='2px' stroke='rgb(100%,0%,0%)' points='77.2783,505.135 149.459,469.044 185.55,541.225 113.369,577.316 ' />
<path stroke='rgb(0%,0%,0%)' stroke-width='0.5px' opacity='1' fill='none' d='M150.488,528.222 A20.1752,20.1752 0 1 0 111.512,528.222' />
<g transform='translate(127.414027, 487.004663)'>
<text x='0' y='12' font-size='12px' font-style='italic'>h</text>
</g>
<ellipse fill='rgb(0%,0%,0%)' opacity='1' stroke='none' cx='146' cy='537' rx='3.5' ry='3.5' />
<ellipse fill='rgb(0%,0%,0%)' opacity='1' stroke='none' cx='117' cy='537' rx='3.5' ry='3.5' />
<polyline fill='none' stroke-opacity='1' stroke-width='0.5px' stroke='rgb(0%,0%,0%)' points='111.926,517.958 111.926,522.048 ' />
<polygon stroke='none' opacity='1' fill-rule='evenodd' fill='rgb(0%,0%,0%)' points='113.768,521.402 113.559,521.504 113.056,521.729 112.754,521.848 112.449,521.951 112.165,522.023 111.926,522.048 111.71,522.023 111.43,521.951 111.115,521.848 110.793,521.729 110.244,521.504 110.011,521.402 111.926,528.402 113.768,521.402 ' />
<polyline fill='none' stroke-opacity='1' stroke-width='1px' stroke='rgb(0%,0%,0%)' points='131.414,586.338 131.414,629.582 ' />
<polygon stroke='none' opacity='1' fill-rule='evenodd' fill='rgb(0%,0%,0%)' points='134.572,628.474 134.213,628.65 133.351,629.035 132.833,629.239 132.31,629.416 131.824,629.539 131.414,629.582 131.043,629.539 130.563,629.416 130.023,629.239 129.472,629.035 128.53,628.65 128.13,628.474 131.414,640.474 134.572,628.474 ' />
<g transform='translate(146.414027, 605.406109)'>
<text x='0' y='12' font-size='12px'>&#x03c0;<tspan dy='5px' font-size='10px'>2</tspan></text>
</g>
<ellipse fill='rgb(0%,0%,0%)' opacity='1' stroke='none' cx='131' cy='649' rx='3.5' ry='3.5' />
<polygon stroke='none' opacity='1' fill-rule='evenodd' fill='rgb(100%,100%,100%)' points='131.414,505.135 203.595,469.044 239.686,541.225 167.505,577.316 ' />
<polygon fill='none' stroke-opacity='1' stroke-width='2px' stroke='rgb(100%,0%,0%)' points='131.414,505.135 203.595,469.044 239.686,541.225 167.505,577.316 ' />
<path stroke='rgb(0%,0%,0%)' stroke-width='0.5px' opacity='1' fill='none' d='M205.488,528.222 A20.1752,20.1752 0 1 0 166.512,528.222' />
<g transform='translate(181.549774, 487.004663)'>
<text x='0' y='12' font-size='12px' font-style='italic'>h</text>
</g>
<ellipse fill='rgb(0%,0%,0%)' opacity='1' stroke='none' cx='200' cy='537' rx='3.5' ry='3.5' />
<ellipse fill='rgb(0%,0%,0%)' opacity='1' stroke='none' cx='171' cy='537' rx='3.5' ry='3.5' />
<polyline fill='none' stroke-opacity='1' stroke-width='0.5px' stroke='rgb(0%,0%,0%)' points='166.062,517.958 166.062,522.048 ' />
<polygon stroke='none' opacity='1' fill-rule='evenodd' fill='rgb(0%,0%,0%)' points='167.904,521.402 167.695,521.504 167.192,521.729 166.89,521.848 166.585,521.951 166.301,522.023 166.062,522.048 165.846,522.023 165.566,521.951 165.251,521.848 164.929,521.729 164.38,521.504 164.146,521.402 166.062,528.402 167.904,521.402 ' />
<polyline fill='none' stroke-opacity='1' stroke-width='1px' stroke='rgb(0%,0%,0%)' points='185.55,586.338 185.55,629.582 ' />
<polygon stroke='none' opacity='1' fill-rule='evenodd' fill='rgb(0%,0%,0%)' points='188.708,628.474 188.349,628.65 187.487,629.035 186.969,629.239 186.446,629.416 185.96,629.539 185.55,629.582 185.179,629.539 184.699,629.416 184.159,629.239 183.607,629.035 182.666,628.65 182.266,628.474 185.55,640.474 188.708,628.474 ' />
<g transform='translate(200.549774, 605.406109)'>
<text x='0' y='12' font-size='12px'>&#x03c0;<tspan dy='5px' font-size='10px'>2</tspan></text>
</g>
<ellipse fill='rgb(0%,0%,0%)' opacity='1' stroke='none' cx='186' cy='649' rx='3.5' ry='3.5' />
<polygon stroke='none' opacity='1' fill-rule='evenodd' fill='rgb(100%,100%,100%)' points='185.55,505.135 257.731,469.044 293.821,541.225 221.64,577.316 ' />
<polygon fill='none' stroke-opacity='1' stroke-width='2px' stroke='rgb(100%,0%,0%)' points='185.55,505.135 257.731,469.044 293.821,541.225 221.64,577.316 ' />
<path stroke='rgb(0%,0%,0%)' stroke-width='0.5px' opacity='1' fill='none' d='M259.488,528.222 A20.1752,20.1752 0 1 0 220.512,528.222' />
<g transform='translate(235.685520, 487.004663)'>
<text x='0' y='12' font-size='12px' font-style='italic'>h</text>
</g>
<ellipse fill='rgb(0%,0%,0%)' opacity='1' stroke='none' cx='254' cy='537' rx='3.5' ry='3.5' />
<ellipse fill='rgb(0%,0%,0%)' opacity='1' stroke='none' cx='225' cy='537' rx='3.5' ry='3.5' />
<polyline fill='none' stroke-opacity='1' stroke-width='0.5px' stroke='rgb(0%,0%,0%)' points='220.198,517.958 220.198,522.048 ' />
<polygon stroke='none' opacity='1' fill-rule='evenodd' fill='rgb(0%,0%,0%)' points='222.04,521.402 221.83,521.504 221.328,521.729 221.025,521.848 220.721,521.951 220.437,522.023 220.198,522.048 219.981,522.023 219.701,521.951 219.386,521.848 219.065,521.729 218.516,521.504 218.282,521.402 220.198,528.402 222.04,521.402 ' />
<polyline fill='none' stroke-opacity='1' stroke-width='1px' stroke='rgb(0%,0%,0%)' points='239.686,586.338 239.686,629.582 ' />
<polygon stroke='none' opacity='1' fill-rule='evenodd' fill='rgb(0%,0%,0%)' points='242.843,628.474 242.484,628.65 241.623,629.035 241.104,629.239 240.582,629.416 240.095,629.539 239.686,629.582 239.315,629.539 238.835,629.416 238.294,629.239 237.743,629.035 236.802,628.65 236.401,628.474 239.686,640.474 242.843,628.474 ' />
<g transform='translate(254.685520, 605.406109)'>
<text x='0' y='12' font-size='12px'>&#x03c0;<tspan dy='5px' font-size='10px'>2</tspan></text>
</g>
<ellipse fill='rgb(0%,0%,0%)' opacity='1' stroke='none' cx='240' cy='649' rx='3.5' ry='3.5' />
<polygon stroke='none' opacity='1' fill-rule='evenodd' fill='rgb(100%,100%,100%)' points='510.364,505.135 582.545,469.044 618.636,541.225 546.455,577.316 ' />
<polygon fill='none' stroke-opacity='1' stroke-width='2px' stroke='rgb(100%,0%,0%)' points='510.364,505.135 582.545,469.044 618.636,541.225 546.455,577.316 ' />
<path stroke='rgb(0%,0%,0%)' stroke-width='0.5px' opacity='1' fill='none' d='M584.488,528.222 A20.1752,20.1752 0 1 0 545.512,528.222' />
<g transform='translate(560.500000, 487.004663)'>
<text x='0' y='12' font-size='12px' font-style='italic'>h</text>
</g>
<ellipse fill='rgb(0%,0%,0%)' opacity='1' stroke='none' cx='579' cy='537' rx='3.5' ry='3.5' />
<ellipse fill='rgb(0%,0%,0%)' opacity='1' stroke='none' cx='550' cy='537' rx='3.5' ry='3.5' />
<polyline fill='none' stroke-opacity='1' stroke-width='0.5px' stroke='rgb(0%,0%,0%)' points='545.012,517.958 545.012,522.048 ' />
<polygon stroke='none' opacity='1' fill-rule='evenodd' fill='rgb(0%,0%,0%)' points='546.854,521.402 546.645,521.504 546.142,521.729 545.84,521.848 545.535,521.951 545.251,522.023 545.012,522.048 544.796,522.023 544.516,521.951 544.201,521.848 543.879,521.729 543.33,521.504 543.096,521.402 545.012,528.402 546.854,521.402 ' />
<polyline fill='none' stroke-opacity='1' stroke-width='2px' stroke='rgb(0%,0%,0%)' points='311.867,126.184 474.165,126.184 ' />
<polygon stroke='none' opacity='1' fill-rule='evenodd' fill='rgb(0%,0%,0%)' points='472.319,120.921 472.612,121.52 473.254,122.956 473.595,123.82 473.89,124.69 474.095,125.501 474.165,126.184 474.095,126.803 473.89,127.603 473.595,128.503 473.254,129.422 472.612,130.991 472.319,131.658 492.319,126.184 472.319,120.921 ' />
<g transform='translate(396.592760, 102.184389)'>
<text x='0' y='12' font-size='12px'><tspan font-style='italic'>R</tspan></text>
</g>
<g transform='translate(325.092760, 136.434389)'>
<text x='6' y='12' font-size='12px'>Restrict to action of <tspan font-style='italic'>H</tspan></text>
<text x='0' y='28' font-size='12px'>on a single fiber &#x03c0;<tspan dy='5px' font-size='10px'>1</tspan><tspan dy='-10px' font-size='10px'>&#8211;1</tspan><tspan dy='5px'>(</tspan><tspan font-style='italic'>x</tspan>)</text>
</g>
<polyline fill='none' stroke-opacity='1' stroke-width='2px' stroke='rgb(0%,0%,0%)' points='492.319,487.089 330.021,487.089 ' />
<polygon stroke='none' opacity='1' fill-rule='evenodd' fill='rgb(0%,0%,0%)' points='331.867,492.353 331.573,491.754 330.932,490.318 330.591,489.454 330.296,488.583 330.091,487.773 330.021,487.089 330.091,486.471 330.296,485.671 330.591,484.771 330.932,483.852 331.573,482.283 331.867,481.616 311.867,487.089 331.867,492.353 ' />
<g transform='translate(397.092760, 463.089367)'>
<text x='0' y='12' font-size='12px'><tspan font-style='italic'>L</tspan></text>
</g>
<g transform='translate(319.592760, 499.089367)'>
<text x='12' y='12' font-size='12px'>Construct induced bundle</text>
<text x='24' y='32' font-size='12px'><tspan font-style='italic'>h</tspan> &#8901; (<tspan font-style='italic'>g</tspan>, <tspan font-style='italic'>v</tspan>) = (<tspan font-style='italic'>g h</tspan><tspan dy='-5px' font-size='10px'>&#8211;1</tspan><tspan dy='5px'>, </tspan><tspan font-style='italic'>s</tspan>(<tspan font-style='italic'>h</tspan>)<tspan font-style='italic'>v</tspan>)</text>
<text x='24' y='52' font-size='12px'>&#x03c0;<tspan dy='5px' font-size='10px'>2</tspan><tspan dy='-5px'>:</tspan> (<tspan font-style='italic'>G</tspan>&#xd7;<tspan font-style='italic'>V</tspan>) / <tspan font-style='italic'>H</tspan> &#8594; <tspan font-style='italic'>G</tspan> / <tspan font-style='italic'>H</tspan></text>
<text x='24' y='72' font-size='12px'>&#x03c0;<tspan dy='5px' font-size='10px'>2</tspan><tspan dy='-5px'>(</tspan>[(<tspan font-style='italic'>g</tspan>, <tspan font-style='italic'>v</tspan>)]) = <tspan font-style='italic'>g H</tspan></text>
<text x='24' y='92' font-size='12px'><tspan font-style='italic'>g</tspan><tspan dy='5px' font-size='10px'>1</tspan><tspan dy='-5px'> &#8901; </tspan>[(<tspan font-style='italic'>g</tspan>, <tspan font-style='italic'>v</tspan>)] = [(<tspan font-style='italic'>g</tspan><tspan dy='5px' font-size='10px'>1</tspan><tspan dy='-5px' font-style='italic'>g</tspan>, <tspan font-style='italic'>v</tspan>)]</text>
</g>
<g transform='translate(-10,0)'>
<polyline fill='none' stroke-opacity='1' stroke-width='2px' stroke='rgb(0%,0%,0%)' points='564.5,198.365 564.5,414.8 ' />
<polygon stroke='none' opacity='1' fill-rule='evenodd' fill='rgb(0%,0%,0%)' points='569.763,412.954 569.165,413.247 567.728,413.888 566.865,414.229 565.994,414.524 565.183,414.729 564.5,414.8 563.882,414.729 563.082,414.524 562.182,414.229 561.263,413.888 559.694,413.247 559.026,412.954 564.5,432.954 569.763,412.954 ' />
</g>
<g transform='matrix(1,0,0,-1,-40,631.319)'>
<polyline fill='none' stroke-opacity='1' stroke-width='2px' stroke='rgb(0%,0%,0%)' points='564.5,198.365 564.5,414.8 ' />
<polygon stroke='none' opacity='1' fill-rule='evenodd' fill='rgb(0%,0%,0%)' points='569.763,412.954 569.165,413.247 567.728,413.888 566.865,414.229 565.994,414.524 565.183,414.729 564.5,414.8 563.882,414.729 563.082,414.524 562.182,414.229 561.263,413.888 559.694,413.247 559.026,412.954 564.5,432.954 569.763,412.954 ' />
</g>
<g transform='translate(572.400000, 297.159502)'>
<text x='-3' y='12' font-size='12px'>Intertwiner  <tspan font-style='italic'>i*</tspan></text>
<text x='-10' y='32' font-size='12px'><tspan font-style='italic'>i*</tspan> : &#x03c0;<tspan dy='5px' font-size='10px'>1</tspan><tspan dy='-10px' font-size='10px'>&#8211;1</tspan><tspan dy='5px'>(</tspan><tspan font-style='italic'>x</tspan>) &#8594; <tspan font-style='italic'>V</tspan></text>
<text x='-5' y='52' font-size='12px'><tspan font-style='italic'>i* h</tspan> = <tspan font-style='italic'>h i*</tspan></text>

<text x='-143' y='12' font-size='12px'>Intertwiner  <tspan font-style='italic'>i</tspan></text>
<text x='-150' y='32' font-size='12px'><tspan font-style='italic'>i</tspan> :  <tspan font-style='italic'>V</tspan> &#8594;&#x03c0;<tspan dy='5px' font-size='10px'>1</tspan><tspan dy='-10px' font-size='10px'>&#8211;1</tspan><tspan dy='5px'>(</tspan><tspan font-style='italic'>x</tspan>)</text>
<text x='-135' y='52' font-size='12px'><tspan font-style='italic'>i h</tspan> = <tspan font-style='italic'>h i</tspan></text>
</g>
<g transform='translate(10,0)'>
<polyline fill='none' stroke-opacity='1' stroke-width='2px' stroke='rgb(0%,0%,0%)' points='185.55,270.546 185.55,414.8 ' />
<polygon stroke='none' opacity='1' fill-rule='evenodd' fill='rgb(0%,0%,0%)' points='190.813,412.954 190.214,413.247 188.778,413.888 187.915,414.229 187.044,414.524 186.233,414.729 185.55,414.8 184.931,414.729 184.131,414.524 183.231,414.229 182.313,413.888 180.744,413.247 180.076,412.954 185.55,432.954 190.813,412.954 ' />
</g>
<g transform='matrix(1,0,0,-1,40,703.5)'>
<polyline fill='none' stroke-opacity='1' stroke-width='2px' stroke='rgb(0%,0%,0%)' points='185.55,270.546 185.55,414.8 ' />
<polygon stroke='none' opacity='1' fill-rule='evenodd' fill='rgb(0%,0%,0%)' points='190.813,412.954 190.214,413.247 188.778,413.888 187.915,414.229 187.044,414.524 186.233,414.729 185.55,414.8 184.931,414.729 184.131,414.524 183.231,414.229 182.313,413.888 180.744,413.247 180.076,412.954 185.55,432.954 190.813,412.954 ' />
</g>
<g transform='translate(76.749774, 303.250000)'>
<text x='8' y='6' font-size='12px'>Vector bundle</text>
<text x='0' y='22' font-size='12px'>morphism (<tspan font-style='italic'>f*</tspan>, <tspan font-style='italic'>m*</tspan>)</text>
<text x='16' y='42' font-size='12px'><tspan font-style='italic'>f*</tspan> : <tspan font-style='italic'>F</tspan> &#8594; <tspan font-style='italic'>L</tspan>(<tspan font-style='italic'>V</tspan>)</text>
<text x='16' y='62' font-size='12px'><tspan font-style='italic'>m*</tspan> : <tspan font-style='italic'>M</tspan> &#8594; <tspan font-style='italic'>G</tspan> / <tspan font-style='italic'>H</tspan></text>
<text x='16' y='82' font-size='12px'><tspan font-style='italic'>m*</tspan> &#x03c0;<tspan dy='5px' font-size='10px'>1</tspan><tspan dy='-5px'> = &#x03c0;</tspan><tspan dy='5px' font-size='10px'>2</tspan> <tspan dy='-5px' font-style='italic'>f*</tspan></text>
<text x='16' y='102' font-size='12px'><tspan font-style='italic'>f* g</tspan> = <tspan font-style='italic'>g f*</tspan></text>

<text x='173' y='6' font-size='12px'>Vector bundle</text>
<text x='165' y='22' font-size='12px'>morphism (<tspan font-style='italic'>f</tspan>, <tspan font-style='italic'>m</tspan>)</text>
<text x='181' y='42' font-size='12px'><tspan font-style='italic'>f</tspan> : <tspan font-style='italic'>L</tspan>(<tspan font-style='italic'>V</tspan>) &#8594; <tspan font-style='italic'>F</tspan></text>
<text x='181' y='62' font-size='12px'><tspan font-style='italic'>m</tspan> : <tspan font-style='italic'>G</tspan> / <tspan font-style='italic'>H</tspan> &#8594; <tspan font-style='italic'>M</tspan></text>
<text x='181' y='82' font-size='12px'><tspan font-style='italic'>m</tspan> &#x03c0;<tspan dy='5px' font-size='10px'>2</tspan><tspan dy='-5px'> = &#x03c0;</tspan><tspan dy='5px' font-size='10px'>1</tspan> <tspan dy='-5px' font-style='italic'>f</tspan></text>
<text x='181' y='102' font-size='12px'><tspan font-style='italic'>f g</tspan> = <tspan font-style='italic'>g f</tspan></text>
</g>
</g>
</svg>

In the diagram above, on the top left we have a generic $G$-equivariant vector bundle over $M$, $F\in Vect(M,G)$, with projection $\pi_1:F\to M$, and a chosen point $x\in M$ whose stabilizer subgroup is $H$.  The functor $R$ maps $F$ to a representation of $H$ on the fiber over $x$, $\pi_1^{-1}(x)$, shown on the top right.

On the bottom right, we have a generic representation of $H$ on a vector space $V$.  The morphisms of $Rep(H)$ are intertwiners, so we are interested in intertwiners such as $i:V\to \pi_1^{-1}(x)$.  The functor $L$, the induced bundle construction, maps a generic representation of $H$ to a $G$-equivariant vector bundle $(G\times V)/H$, shown on the bottom left.  This bundle has a projection $\pi_2: (G\times V)/H \to G/H$, $\pi_2([(g,v)])=g H$.  Since $M \cong G/H$, this bundle is in $Vect(M,G)$.  And we are interested in the morphisms of $Vect(M,G)$, such as $(f,m)$ where $f:L(V)\to F$ and $m:G/H\to M$.

We will impose a restriction to a _subcategory_ of $Vect(M,G)$ consisting _only_ of morphisms that preserve the point $x\in M$.  When we deal with bundles over $G/H \cong M$, we will use the obvious bijection $g H \to g\cdot x$, and accordingly restrict ourselves to vector bundle morphisms that map $x$ to the coset $e H$ or _vice versa_.

We are assuming that $G$ acts transitively on $M$, so given any $y\in M$ there exists at least one element of $G$, say $k(y)$, such that $k(y)\cdot x = y$.  We will now assume that some definite function $k:M\to G$ has been chosen with this property, and for convenience we will further assume that $k(x)=e$, the identity element in $G$.  The group element $k(y)$ gives us a specific way to use the action of $G$ on $M$ to get from our chosen point $x$ to some other point $y$ --- and equally, to use the action of $G$ on the whole bundle $F$ to get from the fiber over $x$ to the fiber over $y$.

Now, to show that $L$ and $R$ are adjoint functors, we need to construct a bijection between the intertwiners $i:V\to \pi_1^{-1}(x)$ and the $G$-equivariant vector bundle morphisms $(f,m)$, where $f:L(V)\to F$ and $m:G/H\to M$.

Given an intertwiner $i:V\to \pi_1^{-1}(x)$, we start by defining $m:G/H\to M$ by:

$$m(g H)=g\cdot x$$

which is independent of $i$, and is just the obvious bijection between $G/H$ and $M$.  Next, we define $f:L(V)\to F$ by:

$$f([(g,v)]) = g\cdot i(v)$$

In other words, given the equivalence class $[(g,v)]$ we use the intertwiner $i$ to take $v\in V$ to $\pi_1^{-1}(x)$, and then the action of $G$ on $F$ to take the result to the fiber $\pi_1^{-1}(g\cdot x)$.  This satisfies the compatibility condition on the projections:

$$\pi_1(f([(g,v)])) = g\cdot x = m(g H) = m(\pi_2([(g,v)]))$$

We also need to check that $f$ commutes with the actions of $G$ on the respective bundles:

$$f(g_1\cdot [(g,v)]) = f([(g_1 g,v)]) = (g_1 g)\cdot i(v) = g_1\cdot f([(g,v)])$$

Next, given a $G$-equivariant vector bundle morphism $(f,m)$, where $f:L(V)\to F$ and $m:G/H\to M$ with $m(e H)=x$, we define an intertwiner $i:V\to \pi_1^{-1}(x)$ by:

$$i(v)=f([(e,v)])$$

We know $i$ will map to $\pi_1^{-1}(x)$ because $f$ must map $[(e,v)]$ to a point in the fiber over $m(\pi_2([(e,v)]))=m(e H)=x$.

We check that this is an intertwiner for the representations of $H$ on the respective vector spaces:

$$i(s(h)v)=f([(e,s(h)v)])=f([(h,v)])=f(h\cdot[(e,v)])=h\cdot i(v)$$

We can also demonstrate a bijection between intertwiners and $G$-equivariant vector bundle morphisms in the other direction:  intertwiners $i^*:\pi_1^{-1}(x)\to V$ and vector bundle morphisms $(f^*,m^*)$, where $f^*:F\to L(V)$ and $m^*:M\to G/H$.

Given an intertwiner $i^*:\pi_1^{-1}(x)\to V$, we define $m^*:M\to G/H$ as:

$$m^*(y) = k(y) H$$

We define the map $f^* : F \to L(V)$ by:

$$f^*(w) = [(k(\pi_1(w)), i^*(k(\pi_1(w))^{-1}\cdot w) )]$$

for each $w\in F$.  Because $k(\pi_1(w))\cdot x = \pi_1(w)$, $k(\pi_1(w))^{-1}$ will map the entire fiber to which $w$ belongs to $\pi_1^{-1}(x)$, the domain of the intertwiner $i^*$.  And we have:

$$\pi_2(f^*(w)) = k(\pi_1(w)) H = m^*(\pi_1(w))$$

The map $f^*$ is a linear map between the fibers $\pi_1^{-1}(y)$ and $\pi_2^{-1}(m^*(y))$, because, along with the linearity of $i^*$, the vector space structure on the fibers of $L(V)$ is _defined_ so all maps of the form $v\to [(g,v)]$ are linear.  So, $m^*$ and $f^*$ together give us a vector bundle morphism from $F$ to $L(V)$.

In order to be a morphism in the category of $G$-equivariant vector bundles, $f^*$ should also commute with the action of $G$.  We have:

$$f^*(g\cdot w) = [(k(\pi_1(g\cdot w)), i^*(k(\pi_1(g\cdot w))^{-1} g\cdot w) )] = [(k(g\cdot \pi_1(w)), i^*(k(g\cdot \pi_1(w))^{-1} g\cdot w) )]$$

Let's abbreviate $\pi_1(w)$ as $y$ and define $h=k(g\cdot y)^{-1} g k(y)$, which takes $x$ to $x$ and so must lie in $H$.  Then we have:

$$f^*(g\cdot w) = [(k(g\cdot y), i^*(h k(y)^{-1}\cdot w) )] = [(k(g\cdot y), s(h) i^*(k(y)^{-1}\cdot w) )] = [(k(g\cdot y) h, i^*(k(y)^{-1}\cdot w) )]$$
$$ = [(g k(y) , i^*(k(y)^{-1}\cdot w) )] = g\cdot [(k(y) , i^*(k(y)^{-1}\cdot w) )] = g\cdot f^*(w)$$

Suppose we're given a $G$-invariant vector bundle morphism $(f^*,m^*)$, where $f^*:F\to L(V)$ and $m^*:M\to G/H$, with $m^*(x)=e H$.

We make use of the linear bijection $\phi_e:V\to E_{e H}$, defined by $\phi_e(v)=[(e,v)]$.  We introduced these linear bijections $\phi_g$ when initially describing the induced bundle construction. We define $i^*:\pi_1^{-1}(x)\to V$ by:

$$i^*(w) = \phi_e^{-1}(f^*(w))$$

We check that this is an intertwiner between the relevant representations of $H$:

$$i^*(h\cdot w) = \phi_e^{-1}(f^*(h\cdot w))= \phi_e^{-1}(h\cdot f^*(w))$$

Suppose $f^*(w)=[(e,v)]$ for some $v\in V$.  Then $i^*(w) = v$, and :

$$h\cdot f^*(w) = [(h,v)] = [(e,s(h)v)]$$

$$i^*(h\cdot w) = \phi_e^{-1}([(e,s(h)v)]) = s(h)v = s(h) i^*(w)$$

#Related issues#

[[Bill Lawvere]] noted a structural similarity between induced representations and quantification. See blog [discussion](http://golem.ph.utexas.edu/category/2007/10/concrete_groups_and_axiomatic.html#c012917).

If the modules over a group are considered as comodules over the function Hopf algebra over the group, then one can instead consider the induction for comodules. See [[cotensor product]]. 

#References#

This blog entry contains related discussion:

* John Baez, [Unitary Representations of the Poincare Group](http://golem.ph.utexas.edu/category/2009/03/unitary_representations_of_the.html#comments)

The above text is taken from these comments

* Greg Egan _[Induced representations](http://golem.ph.utexas.edu/category/2009/03/unitary_representations_of_the.html#c023252)_

* John Baez _[Reply](http://golem.ph.utexas.edu/category/2009/03/unitary_representations_of_the.html#c023258)_