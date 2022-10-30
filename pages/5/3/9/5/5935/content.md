
> this is a subentry of [[cohesive (infinity,1)-topos]]. See there for background and context

> under construction

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohesive $\infty$-Toposes
+--{: .hide}
[[!include cohesive infinity-toposes - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

We discuss how a [[cohesive (∞,1)-topos]] that is equipped with a notion of [[cohesive (∞,1)-topos|infinitesimal cohesion]] induces a notion of [[geometry (for structured (∞,1)-toposes)]], hence intrinsically defines a  [[higher geometry]] with a good notion of cohesively [[structured (∞,1)-topos]]es that suitably adapts and generalizes the notion of [[locally ringed space]] and [[locally ringed topos]]es.

Every [[(∞,1)-topos]] $\mathbf{H}$ is (in a tautological but useful way), the [[classifying topos]] (see there for details) for a [[theory]] $\mathbb{T}$ of [[local algebra|local]] [[∞-algebra over an (∞,1)-algebraic theory|∞-algebras]]. 

This means that for $\mathcal{X}$ any [[(∞,1)-topos]] and 

$$
  A : (\mathcal{O}_{\mathcal{X}} \dashv R) : \mathcal{X} \stackrel{\overset{\mathcal{O}_{\mathcal{X}}}{\leftarrow}}{\underset{R}{\to}} \mathbf{H}
$$

a [[geometric morphism]], we may think of the [[exact functor|left exact]] and cover-preserving (hence "local") functor
$$
  \mathcal{O}_{\mathcal{X}} 
    : 
  \mathcal{C}_{\mathbb{T}}
   \stackrel{j}{\to}
  \mathbf{H}
    \stackrel{\mathcal{O}_{\mathcal{X}}}{\to}
  \mathcal{X}
$$ 

given by the composition of the [[(∞,1)-Yoneda embedding]] of the [[syntactic site]] $\mathcal{C}_{\mathbb{T}}$ of $\mathbb{T}$ with the [[inverse image]] $\mathcal{O}_{\mathcal{X}}$ as exhibiting a [[structure sheaf]] of [[local algebra|local]] $\mathbb{T}$-[[∞-algebra over an (∞,1)-algebraic theory|∞-algebras]] in $\mathcal{X}$.

For this general abstract construction to indeed accurately model a notion of [[higher geometry]], this setup needs to be equipped with a suitable choice of admissible morphisms between such $\infty$-structure sheaves: not every morphis of [[classifying topos|classifying]] [[geometric morphism]]s qualifies as morphism of locally $\mathbb{T}$-algebra-ed $(\infty,1)$-toposes. This extra datum is encoded by a choice of morphisms in $\mathbf{H}$ that qualify as [[open map]]s in a suitable sense. Such a choice then gives rise to a genuine notion of [[geometry (for structured (∞,1)-toposes)]].

We discuss below how in the case that $\mathbf{H}$ is a [[cohesive (∞,1)-topos]] equipped with [[cohesive (∞,1)-topos -- infinitesimal cohesion|infinitesimal cohesion]] these [[open map]]s are canonically and intrinsically induced: they are the [[formally etale morphism]]s with respect to the given notion of infinitesimal cohesion.

## Definition

### Locally structured $\infty$-toposes

Therefore we can give the following abstract characterization of _local_ morphisms of "locally algebra-ed $\infty$"-toposes (I'll use the latter term -- supposed to remind us that it generalizes the notion of _locally ringed topos_ -- tentatively for the moment, until I maybe settle for a better term). I would like to know if there is still nicer and way to think of the following.

So for $\mathbf{H}$ our given cohesive $\infty$-topos we regard it as the classifying $\infty$-topos for some theory of local T-algebras. Then given any $\infty$-topos $\mathcal{X}$ a _T-structure sheaf_ on $\mathcal{X}$ is a geometric morphism

$$
   A : \mathcal{X} \to \mathbf{H}
$$

whose inverse image we write $\mathcal{O}_X$. 

We then want to identify "&#233;tale" morphisms in $\mathbf{H}$ and declare that a morphism of locally T-algebra-ed $\infty$-toposes $(f, \alpha) : (\mathcal{X}, \mathcal{O}_{\mathcal{X}}) \to (\mathcal{Y}, \mathcal{O}_{\mathcal{Y}})$

$$
   \array{
       \mathcal{X} 
        \\
        \uparrow  & \nwarrow^{\mathrlap{\mathcal{O}_{\mathcal{X}}}}
        \\
        {}^{\mathllap{f^*}}\uparrow        &{}^{\mathllap{\alpha}}\neArrow& \mathbf{H}
        \\
       \uparrow & \swarrow_{\mathrlap{\mathcal{O}_{\mathcal{Y}}}}
        \\
        \mathcal{Y}
   }
$$

is a geometric transformation as indicated, such that  on &#233;tale morphisms $p : Y \to X$ in $\mathbf{H}$  all its component naturality squares

$$
  \array{
        f^* \mathcal{O}_{\mathcal{X}}(Y) &\stackrel{\alpha_Y}{\to}& 
         \mathcal{O}_{\mathcal{Y}}
        \\
        \downarrow && \downarrow
        \\
        f^* \mathcal{O}_{\mathcal{X}}(X)
         &\stackrel{\alpha_X}{\to}&
         \mathcal{O}_{\mathcal{Y}}
   }
$$

are pullback squares. 

In view of the above this looks like it might be a hint for a more powerful description: because the Rosenberg-Kontsevich characterization of the (formally) &#233;tale morphism $Y \to X$ is of the same, but converse form: given an infinitesimal cohesive neighbourhood

$$
  i : \mathbf{H} \to \mathbf{H}_{\mathrm{th}}
$$

we have canonically given a natural transformation

$$
  \phi : i_! \Rightarrow i_*
$$

looking like

$$
  \array{
    & \nearrow \searrow^{\mathrlap{i_!}}
     \\
     \mathbf{H}
     & \Downarrow^{\phi}&
     \mathbf{H}_{th}
     \\
     & \searrow \nearrow_{\mathrlap{i_*}}
  }
$$

and we say $Y \to X$ is (formally) &#233;tale if its comonents naturality squares under $\phi$

$$
  \array{
      i_! X &\stackrel{\phi_Y}{\to}& i_! Y
      \\
     \downarrow && \downarrow
     \\
      i_* X &\stackrel{\phi_Y}{\to}& i_* Y
  }
$$

are pullbacks.

So in total we are looking at diagrams of the form

$$
   \array{
       \mathcal{X} 
        \\
        \uparrow  & \nwarrow^{\mathrlap{\mathcal{O}_{\mathcal{X}}}}
       & & \nearrow \searrow^{\mathrlap{i_!}}
        \\
        {}^{\mathllap{f^*}}\uparrow        &{}^{\mathllap{\alpha}}\neArrow& \mathbf{H}
        &\Downarrow^{\phi}& \mathbf{H}_{th}
        \\
       \uparrow & \swarrow_{\mathrlap{\mathcal{O}_{\mathcal{Y}}}}
       && \searrow \nearrow_{\mathrlap{i_*}}
        \\
        \mathcal{Y}
   }
$$

and demand the compatibility condition that those morphisms in $\mathbf{H}$ that have cartesian components under $\phi$ also have cartesian components under $\alpha$.

(...)




## References

* [[Jacob Lurie]], _[[Structured Spaces]]_
  {#Lurie}


[[!redirects cohesive (infinity,1)-topos -- structure ∞-sheaves]]
[[!redirects cohesive (∞,1)-topos -- structure ∞-sheaves]]
