
> under construction -- These are presently just notes to go along with a talk [here](http://muuk.karlin.mff.cuni.cz/cs/node/13)

This entry is going to become an exposition to the topics of 

1. [[Cartan geometry]];

1. higher dimensional [[supergravity]];

1. [[higher dimensional WZW models]];

1. the completed [[brane scan]];

1. anomaly cancellation in higher WZW models via higher string lifts.

and an indication of how these all naturally flow out of a common source when considered in [[higher differential geometry|higher differential]] [[supergeometry]].


#Contents#
* table of contents
{:toc}

## Cartan geometry

[[smooth manifolds|Smooth manifolds]], such as [[spacetimes]], are modeled on the [[real line]] and its [[products]], the [[Cartesian spaces]] $\mathbb{R}^d$ (see also at _[[geometry of physics -- coordinate systems]]_).

It is clear that here it is crucial that $\mathbb{R}^n$ is regarded with its [[smooth structure]].

But $\mathbb{R}^d$ also has ([[smooth group|smooth]]) _[[group]]_ structure. As such it is the [[translation group]]. In [[Newtonian mechanics]] this group structure plays a key role, as it allows for instance to say what in means that a [[particle]] propagates along a straight [[trajectory]].

With the dawn of [[general relativity]] and its "[[general covariance]]" it was finally understood that this is a bit too naive: [[free field|free]] [[particles]] propagate on straight lines in $\mathbb{R}^n$ only [[infinitesimal object|infinitesimally]]. After every infinitesimal translation, the notion of "straight" needs to be adjusted, due to the "[[force]]" of [[gravity]].

This has a straightforward visualization in 2-dimensions: visualize a bumpy [[surface]] $X$ [[embedding|embedded]] in $\mathbb{R}^3$ (for instance a [[2-sphere]]). Pick a point $x \in X$ and visualize the [[tangent]] [[plane]] to that point, which is an $\mathbb{R}^2$. Now given a [[curve]] in $X$ that emanates from $x$, then one may visualize the plane to be "rolling without sliding" on $X$ such that the point where it touches $X$ follows the curve.

Under this map from curves in the plane to curves in the $X$, straight lines in $\mathbb{R}^2$ now map to [[geodesics]] in $X$. These are the actual paths that free particles in $X$ follow.

The most popular way to formalize this is the modern concept of the [[Levi-Civita connection]] of the [[Riemannian metric]] on $X$ (which in the above example is induced from the canonical one on the embedding space $\mathbb{R}^3$).

But [[Élie Cartan]]'s original way of speaking about [[affine connections]] much closer resembles this picture of a "local model space with group structure" doing "rolling without slipping" over [[spacetime]]. This is now mostly called a _[[Cartan connection]]_.

Here one regards the [[Euclidean group]] $Iso(n)$ of all [[isometries]] of $\mathbb{R}^d$. Inside this is the [[rotation group]] $SO(d) \hookrightarrow Iso(d)$. The [[quotient group]] is [[Cartesian space]]

$$
  \mathbb{R}^d \simeq Iso(d)/SO(d)
  \,.
$$

The structure of "rolling without sliding" is then formalized in the concept of a [[Cartan connection]] by saying 

1. **rolling** -- there is an $Iso(d)$-[[principal connection]] on $X$ (the group $Iso(d)$, via its [[action]]  on $\mathbb{R}^d$, rolls and slides the Cartesian space around);

1. **without sliding** -- such that there is a [[reduction of the structure group]] to $SO(d)$ (this makes the original $Iso(n)$-bundle be have [[associated bundle|associated]] to it the actual $\mathbb{R}^d$-[[fiber bundle]]);

  and such that under this reduction the connection at each point infinitesimally identifies the [[tangent space]] of $X$ with the abstract copy of $\mathbb{R}^d \simeq Iso(d)/SO(d)$.

This has an evident heneralization where we conisder any inclusion $H \hookrightarrow G$ of [[Lie groups]]. If one considers instead of [[Cartesian space]] $\mathbb{R}^d$ the [[Minkowski space]] $\mathbb{R}^{d-1,1}$, then $Iso(d-1,1)$ is the [[Poincaré group]]. and $SO(d-1,1)$ is the [[Lorentz group]]. Now the [[geodesics]] via [[parallel transport]] along a $(SO(d-1,1)\hookrightarrow Iso(d-1,1))$-[[Cartan connection]] reflect the [[force]] of [[gravity]] in the [[theory (physics)|theory]] of [[general relativity]].

Many other combinations $(H \hookrightarrow G)$ may be considered:

[[!include local and global geometry - table]]

## Higher dimensional supergravity

In the contemporary [[physics]] literature this concept of [[Cartan connection]] may seem to play an orphaned role, at least if one compares the number of occurences of the explicit term [[Cartan connection]] in the physics literature over that of "[[Levi-Civita connection]]",and certainly when compared to the number of contemporary articles that speak of [[geodesics]] without any concept of [[connection]] made explicit.

However, this is partly an illusion. Examination of the literature shows that at least as soon as authors consider _[[supergravity]]_, then everything is really secretly formulated in terms of [[supergeometry|super]] [[Cartan geometry]], as only in this formulation is the incorporation of [[fermions]] and  of [[supersymmetry]] really natural.

In fact, higher dimensional supergravity such as [[type II supergravity]], [[heterotic supergravity]] and [[11-dimensional supergravity]] crucially includes [[field (physics)|fields]] which are [[higher gauge fields]] -- the [[B2-field]], the [[B6-field]], the [[C3-field]], the [[C6-field]], and also the [[RR-field]] if one digs deeper. 

The only proposal in the physics literature for how to deal with such higher gauge higher supergravity theories _geometrically_ is the [[D'Auria-Fre formulation of supergravity]]. And this is secretly _[[higher Cartan geometry]]_. 

$$
  \array{
    && Lie\;Algebras
    \\
    &\swarrow && \searrow
    \\
    Lie \; n-algebras
    && && L_\infty-algebras
    \\
    & \searrow && \swarrow
    \\
    && super\; L_\infty-Algebras
  }
  \,.
$$


... [[Chevalley-Eilenberg algebra]]...[[super L-infinity algebra]]... [[super Poincaré Lie algebra]]...

[[super Minkowski spacetime]]:

$\mathbb{R}^{d-1,1\vert N} = \mathfrak{sIso}(d-1,1\vert N)/\mathfrak{so}$

in fact for higher dimensional [[supergravity]] we need [[extended super Minkowski spacetimes]]... To motivate these we now consider WZW models. 


## Higher Wess-Zumino-Witten-type sigma-models

A miracle happens when one passes from [[Lorentzian geometry]] to Lorentzian [[supergeometry]].

### Cohomology

While the [[cohomology]] of [[Cartesian space]] and [[Minkowski spacetime]] is fairly trivial...

...the [[cohomology]] of [[super-Minkowski spacetime]] $\mathbb{R}^{d-1,1\vert N}$ turns out to have "exceptional" cohomology classes of degree $(p+2)$ for some special combinations of

1. the [[dimension]] $d$ of [[spacetime]];

1. the real [[spin representation]] $N$;

1. the degree $(p+2)$ (where, see in a few lines below, $p$ turns out to be the [[dimension]] of a [[super p-brane]] propagating through spacetime).

More precisely, it is the $SO(d-1,1)$-invariant [[group cohomology]] of $Iso(\mathbb{R}^{d-1,1\vert N})$ which has these exceptional cocycles, and hence the [[super Lie algebra|super]] [[Lie algebra cohomology]] of [[super Minkowski spacetime]]. We come to this [below](#TheCompletedBrainScan).


But the thing is: ever since [[Paul Dirac]] it is known that given a [[cocycle]] in  [[differential cohomology]] of degree $(p+2)$ on [[spacetime]] $X$  -- such as a [[line bundle with connection]] representing the [[electromagnetic field]] -- then this serves as the [[background field]] for a [[sigma-model]] describing the propagation of a [[p-brane]] in $X$ which is [[charge|charged]] under this [[higher gauge field]] and feels its [[forces]] -- such as, for $p = 0$, an [[electron]] subect to the [[Lorentz force]].

Moreover, the consideration of [[Dirac monopoles]] and other [[instantons]] and [[black branes]] shows that given any such [[higher gauge field]], it automatically _induces_ [[p-branes]] which are charged under it: the [[p-brane]] [[sigma model]] turns out to give the [[perturbation theory]] for which the [[black branes]] are the [[non-perturbative effects]].

This is how most of the [[p-branes]] in [[superstring theory]] and [[M-theory]] were originally found by looking at [[black brane]] solutions in higher dimesnional [[supergravity]].


More in detail, the higher dimensional analog of the [[Lorentz force]], felt by these [[p-branes]] is given by  [[interaction]] [[action functional]] which is the [[higher parallel transport]] ([[higher volume holonomy]]) of the [[background gauge field]] over the [[worldvolume]] of the [[p-brane]]. This is also known as the _[[WZW term]]_ in _[[higher dimensional WZW theory]]_.

Locally this is a simple phenomenon, and this local picture is what most of the physics textbook will ever consider: 

there is a [[differential form|differwential]] [[curvature form|curvature (p+2)-forom]] $\omega$ on the local model space $G/H$, and if that is like [[Minkowski space]] then it is [[contractible space]] hence there is a "higher [[vector potential]]" $A \in \Omega^{p+1}(G/H)$ such that $\omega = \mathbf{d}A$, and the [[action functional]] in question is just that given by [[integration of differential forms]].

However, already in local model spaces such as [[super Minkowski spacetime]], each $\omega$ may not have such a potentual that is $H$-invariant. Worse, once the [[p-brane]] leaves a given the local model space $G/H \hookrightarrow X$ of [[spacetime]], then one needs a [[higher gauge transformation]] to connect the interaction terms on the two patches. Still worse, these gauge transformation need to glue (need to "[[descent]]" alond the [[cover]] $\coprod_i G/H \to X$) to a globally defined ("non-perturbative", free of [[classical anomalies]]) higher gauge field on all of $X$.

For the traditional 2d [[WZW model]] this was eventually fairly widely appreciated, for [[higher dimensional WZW models]] this is still much of an open secret.

Before proceeding to the explanation of the global higher WZW terms, we consider some [[boundary field theory]] now.


### Brane intersection laws and Brane condensates in extended super-spacetime


We discuss now  a way ([FSS 13](#FSS13)) to find the [[boundary conditions]] and brane condensates via [[homotopy theory]] of [[super L-∞ algebras]] and via the [[cobordism hypothesis]] for [[local prequantum field theory|local prequantum]] [[boundary field theory]].


So given a $(p+2)$-[[infinity-Lie algebroid cohomology|cocycle]] on [[super Minkowski spacetime]], which is just a [[homomorphism]] of [[super L-∞ algebras]] of the form

$$
  \mathbb{R}^{d-1,1 \vert N}
  \stackrel{\mu_{p+2}}{\longrightarrow}
  \mathbf{B}^{p+1} \mathbb{R}
$$

then we discussed how this is the local ("rational") expression for a higher WZW term for a [[sigma-model]] of a [[p-brane]]. A [[field (physics)|field]] configuration of that sigma-model is hence a map as on the left of

$$
  \array{
    \Sigma_{p+1}
    \stackrel{\phi}{\longrightarrow}
    \mathbb{R}^{d-1,1 \vert N}
    \stackrel{\mu_{p+2}}{\longrightarrow}
    \mathbf{B}^{p+1} \mathbb{R}
   }
$$

and the composite is (the [[curvature]] of) the [[local Lagrangian]] of the [[gauge field|gauge]] [[interaction]]. In ([FSS 13](#FSS13)) it is show how to use [[Lie integration]] to produce from this the full higher [[WZW term]]/[[prequantum n-bundle]]/[[interaction]] [[local Lagrangian]]

$$
  \mathbf{L}_{WZW}
  \;\colon\;
  \mathbb{R}^{d-1,1 \vert N}
   \longrightarrow
  \mathbf{B}^{p+1} (\mathbb{R}/\Gamma)_{conn}
$$

But for the moment it is helpful for simplicity to stay at the rational/infinitesimal/$L_\infty$-algebraic level. All what we find here lifts as expected under [[Lie integration]].

So, now according to the [[cobordism hypothesis]] for [[local prequantum field theory|local prequantum]] [[boundary field theory]], a [[boundary condition]] for this Lagrangian is a diagram of the form

$$
  \array{
    && Q &\longrightarrow& \ast
    \\
    && \downarrow &^{\mathllap{\simeq}}\swArrow_{\mathrlap{\kappa}}& \downarrow^{\mathrlap{0}}
    \\
    \Sigma_{p+1}
    &\stackrel{\phi}{\longrightarrow}&
    \mathbb{R}^{d-1,1 \vert N}
    &\stackrel{\mu_{p+2}}{\longrightarrow}&
    \mathbf{B}^{p+1} \mathbb{R}
   }
  \,,
$$

hence is some space $Q$ inside spacetime such that the pullback of the higher [[WZW term]]/[[prequantum n-bundle]]/[[interaction]] [[local Lagrangian]] for the [[bulk field theory|bulk]] [[field (physics)|fields]] to this space is equipped with a choice of gauge trivialization $\kappa$. Moreover, given this then the [[field (physics)|fields]] of the [[sigma-model]] on a [[worldvolume]] $\Sigma_{p+1}$ with [[boundary]] $(\partial \Sigma)_p \hookrightarrow \Sigma_{p+1}$ is a diagram as on the left of

$$
  \array{
    (\partial \Sigma)_{p+1} &\stackrel{\phi_{bdr}}{\longrightarrow}& Q &\longrightarrow& \ast
    \\
    \downarrow && \downarrow &^{\mathllap{\simeq}}\swArrow_{\mathrlap{\kappa}}& \downarrow^{\mathrlap{0}}
    \\
    \Sigma_{p+1}
    &\stackrel{\phi}{\longrightarrow}&
    \mathbb{R}^{d-1,1 \vert N}
    &\stackrel{\mu_{p+2}}{\longrightarrow}&
    \mathbf{B}^{p+1} \mathbb{R}
   }
  \,,
$$

We want to understand what kind of object this $Q$ is that the boundary of the $p$-brane may stick to. To that end, observe that by the [[universal property]] of [[homotopy pullbacks]], we may decompose the diagram on the right into two diagrams, where the intermediate stage is the [[extended super Minkowski spacetime]] ${\widehat{\mathbb{R}}}^{d-1,1 \vert N}$ which, as a [[super L-∞ algebra]], is the [[homotopy fiber]] of $\mu_{p+2}$

$$
  \array{
    (\partial \Sigma)_{p+1} &\stackrel{\phi_{bdr}}{\longrightarrow}& 
    Q &\stackrel{\Phi}{\longrightarrow} & {\widehat{\mathbb{R}}}^{d-1,1 \vert N}
    &\longrightarrow& \ast
    \\
    \downarrow && \downarrow &{}^{\mathllap{\simeq}}\swArrow& \downarrow &^{\mathllap{\simeq}}\swArrow& \downarrow^{\mathrlap{0}}
    \\
    \Sigma_{p+1}
    &\stackrel{\phi}{\longrightarrow}&
    \mathbb{R}^{d-1,1 \vert N}
    &\stackrel{id}{\longrightarrow}&
    \mathbb{R}^{d-1,1 \vert N}
    &\stackrel{\mu_{p+2}}{\longrightarrow}&
    \mathbf{B}^{p+1} \mathbb{R}
   }
  \,.
$$

This is the higher [[infinity-Lie algebra cohomology|L-∞ extension]] classified by the [[cocycle]] in generalization to the familier fact that 2-coycles classify plain [[Lie algebra extensions]].

+-- {: .un_prop }
###### Proposition 

The [[Chevalley-Eilenberg algebras]] of these ${\widehat{\mathbb{R}}}^{d-1,1 \vert N}$ are precisely the dg-algebras used at least since ([D'Auria-Fr&#233; 82](#DAuriaFre82)) in the [[D'Auria-Fré formulation of supergravity]]. 

=--

This is shown in ([FSS 13](#FSS13)) using a characterization of [[homotopy pullbacks]] in a [[model structure for L-infinity algebras]] derived in ([FRS 13b](#FRS13b)).

But now from this we see that on $Q$ there is itself a [[sigma-model]] [[field (physics)|field]] $\Phi$ that exhibits $Q$ itself as a [[brane]], propagating in this [[extended super Minkowski spacetime]]. Or rather: that would exhibit this if there were an [[action functional]] for this sigma model. By repeating the reasoning, this is given in turn by (if it exists nontrivially) a higher WZW term given by a higher [[L-∞ cocycle]] $\mu_{\tilde p + 2}$ of some further degree $\tilde p + 2$.

$$
  \array{
    (\partial \Sigma)_{p+1} &\stackrel{\phi_{bdr}}{\longrightarrow}& 
    \Sigma_{\tilde p + 1} &\stackrel{\Phi}{\longrightarrow} &   
    {\widehat{\mathbb{R}}}^{d-1,1 \vert N}
    &\stackrel{\mu_{\tilde p + 2}}{\longrightarrow}& \mathbf{B}^{\tilde p + 1}
    \\
    \downarrow && \downarrow 
    \\
    \Sigma_{p+1}
    &\stackrel{\phi}{\longrightarrow}&
    \mathbb{R}^{d-1,1 \vert N}
    &\stackrel{id}{\longrightarrow}&
    \mathbb{R}^{d-1,1 \vert N}
    &\stackrel{\mu_{p+2}}{\longrightarrow}&
    \mathbf{B}^{p+1} \mathbb{R}
   }
  \,.
$$

## The completed brane scan
 {#TheCompletedBrainScan}

This gives a curious direct identification between [[L-∞ algebra cohomology]] and brane intersection laws: every $L_\infty$-extension classified by an $L_\infty$-cocycle together with a further cocycle on the extension gives a [[higher WZW sigma-model]] for some [[super p-brane]] wich may end on a super-$\tilde p$-brane. It turns out that this reasoning reproduces the _completed_ [[brane scan]] of [[superstring theory]]/[[M-theory]], including notably the [[D-branes]] of [[type II string theory]] together with the information that the [[fundamental string]] may end on them, as well as the sigma-model for the [[M5-brane]] with its tensor multiplet fields ([FSS 13](#FSS13)) and the information that [[M2-brane]] may end on it. These maps out much of the key statements about [[M-theory]] (and does so in a precise/rigorous way). 

$$
  \array{
     && &\mathfrak{D}(2p)\mathfrak{brane} &&& \mathfrak{D}(2p+1)\mathfrak{brane}
     \\
     &&& \downarrow && & \downarrow
     \\
     && &  \mathfrak{string}_{IIA} && & \mathfrak{string}_{IIB}
     \\
     && & \searrow && \swarrow
     \\
     \mathfrak{sdstring} & && \mathbb{R}^{10 \vert N=(1,1)} &  & \mathbb{R}^{10 \vert N=(2,0)}  &&& \mathfrak{string}_{het}
     \\
     & \searrow &  && \downarrow && & \swarrow
     \\
     && \mathbb{R}^{6 \vert N=(2,0)} && \mathbb{R}^{10 \vert N=2} && \mathbb{R}^{10 \vert N=(1,0)} 
     \\
     && & \searrow & \downarrow & \swarrow
     \\
     && && \mathbb{R}^{0\vert N} &\leftarrow& \mathbb{R}^{11\vert N=1} &\leftarrow& \mathfrak{m}2\mathfrak{brane} &\leftarrow& \mathfrak{m}5\mathfrak{brane} 
  }
$$


[[!include brane scan]]


**Proposition**

We may construct the  [[prequantum n-bundle|prequantum (p+1)-bundle]] 

$$
  \mathbf{L}_{WZW}
  \;\colon\;
  {\widehat \mathbb{R}}^{d-1,1\vert N}
  \stackrel{\mathbf{L}_{WZW}}{\longrightarrow}
  \mathbf{B}^{p+1} (\mathbb{R}/\Gamma)_{conn}
$$

for all [[super p-brane]] [[sigma-models]] via a kind of [[Lie integration]]. ([FSS13](#FSS13))



## Anomaly-free higher sigma-models via higher string-lifts of Cartan connections



All would be done and said if [[spacetime]] were fixed to be a give [[extended super Minkowski spacetime]]. 

But of course the key now is that in [[supergravity]] instead spacetime $X$ only locally looks this way, and globally is a [[Cartan connection]] for the [[super Poincaré group]] or its higher analogs  acting on an [[extended super Minkowski spacetime]].


What we need to solve the gluing problem for the higher WZW term and hence cancel its [[classical anomaly]] is that on $X$ itself there is a WZW term

$$
  \mathbf{L}_{WZW}^{global} \colon X \longrightarrow \mathbf{B}^{p+1}(\mathbb{R}/\Gamma)_{conn}
$$

such that for a given [[cover]] by local model space as given by the [[Cartan connection]] [[background gauge field]] of [[gravity]] and [[B-field]], [[C-field]], etc; this restricts to the canonical one described above, i.e. we need a [[commuting diagram]] of the form

$$
  \array{
    {\widehat \mathbb{R}}^{d-1,1\vert N}
    \\
    \downarrow & \searrow^{\mathrlap{\stackrel{\mathbf{L}_{WZW}}}
    \\
    X 
    &
      \stackrel{\mathbf{L}_{WZW}^{global}}{\longrightarrow} 
    & 
    \mathbf{B}^{p+1} (\mathbb{R}/\Gamma)_{conn}
  }
  \,.
$$

> I claim that the solution to this globalization problem works as follows, though I have not written this down in full detail yet. Notice that while I write super-Minkowski spacetimes here just for the heck of it, this may be considered much more generally in [[higher Cartan geometry]].

Consider the restriction of the WZW term to any [[formal disk]] (this is [[synthetic geometry|synthetically]] the $L_\infty$-algebra, really), in the sense discussed at _[[Lie differentiation]]_.

$$
  \mathbf{L}_{WZW}^{formal}
  \;\colon\;
  {\widehat{\mathbb{D}}}^{d-1,1\vert N}
  \hookrightarrow
  {\widehat \mathbb{R}}^{d-1,1\vert N}
  \stackrel{\mathbf{L}_{WZW}}{\longrightarrow}
  \mathbf{B}^{p+1} (\mathbb{R}/\Gamma)_{conn}
$$


Consider then the [[quantomorphism n-group]] of this formal WZW term ([FRS 13a](#FRS13a)), defined by sitting in the [[homotopy fiber sequence]]

$$
  QuantMorph(\mathbf{L}_{WZW}^{formal})
   \longrightarrow
  \mathbf{Aut}(\mathbb{D}^{d-1,1\vert N})
  \simeq
  GL(d\vert N)
   \stackrel{\mathbf{L}_{WZW}^{forma} \circ (-)}{\longrightarrow}
  (\mathbf{B}^{p+1} (\mathbb{R}/\Gamma))\mathbf{Conn}(\mathbb{D}^{d-1,1\vert N})
$$

where the rightmost term is the [[differential concretification]] of the [[mapping stack]] $[\mathbf{B}^{p+1}(\mathbb{R}/\Gamma)_{conn}$, hence the higher [[moduli stack of connections]] on the given [[formal disk]] inside [[extended super Minkowski spacetime]].

Intuitively this [[smooth super ∞-group|smooth super]] [[∞-group]] looks as follows ([FRS 13a](#FRS13a)):

$$
  QuantMorph(\mathbf{L}_{WZW}^{formal})
  \;=\;
   \left\{
     \array{
        \mathbb{D}^{d-1,1\vert N} && \stackrel{\simeq}{\longrightarrow} &&
        \mathbb{D}^{d-1,1\vert N}
        \\
        & {}_{\mathllap{\mathbf{L}_{WZW}^{formal}}}\searrow 
        &\simeq& \swarrow_{\mathrlap{\mathbf{L}_{WZW}^{formal}}}
        \\
        && 
        \mathbf{B}^{p+1} (\mathbb{R}/\Gamma)_{conn}
     }
   \right\}
$$

An element in this group is precisely the datum needed to change [[tangent spaces]] in a [[Cartan connection]] while carrying also the WZWZ term along! See also at _[[parameterized WZW model]]_.

By the discussion in ([FRS 13a](#FRS13a)), this is the general higher and super-analog of [[string 2-group]], [[fivebrane 6-group]], [[ninebrane 10-group]]. Hence it makes sense to give it a name like so:

$$
  p Brane(d\vert N)
  \coloneqq
  QuantMorph(\mathbf{L}_{WZW}^{formal})
$$

Now the claim is that the [[obstruction]] to globally anomlay free super $p$-brane WZW models with respect to a given supergravity Cartan backround
is a "super $p$-brane"-structure, hence a lift

$$
  \array{
    && \mathbf{B}(p Brane(d\vert N))
    \\
    & {}^{\mathllap{\widehat {\tau}_X}}\nearrow & \downarrow
    \\
    X &\stackrel{\tau_X}{\longrightarrow} & \mathbf{B}GL(d,N)
  }
$$

of the map that classifies the [[frame bundle]] as discussed at _[[differential cohesion]]_ in the section _[Differential cohesion -- Frame bundles](differential+cohesion#GLnTangentBundles)_.

By the above picture of $p Brane(d\vert N)$ it should be plausbile that this is precisely the data needed to carry the WZW turn around with Cartan's "rolling without slipping".

## References

* {#DAuriaFre82} [[Riccardo D'Auria]], [[Pietro Fré]] _Geometric supergravity in $D = 11$ and its hidden supergroup_, Nuclear Physics B201 (1982) 101-140  ([[GeometricSupergravity.pdf:file]])
 

* {#CastellaniDAuriaFre91} [[Leonardo Castellani]], [[Riccardo D'Auria]], [[Pietro Fré]], _[[Supergravity and Superstrings - A Geometric Perspective]]_, World Scientific (1991)

* {#FRS13a} [[Domenico Fiorenza]], [[Chris Rogers]], [[Urs Schreiber]] _[[schreiber:Higher geometric prequantum theory]]_


* {#FRS13b} [[Domenico Fiorenza]], [[Chris Rogers]], [[Urs Schreiber]], _[[schreiber:L-∞ algebras of local observables from higher prequantum bundles]]_, Homology, Homotopy and Applications, Volume 16 (2014) Number 2, p. 107 &#8211; 142 ([arXiv:1304.6292](http://arxiv.org/abs/1304.6292))


* {#FSS13} [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]] _[[schreiber:The brane bouquet]]_, International Journal of Geometric Methods in Modern Physics, Vol. 12 (2015) 1550018 ([arXiv:1308.5264](http://arxiv.org/abs/1308.5264))