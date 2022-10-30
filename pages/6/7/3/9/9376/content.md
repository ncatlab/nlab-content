

## Idea

We discuss the refinement of the traditional notion of _[[Atiyah Lie groupoids]]_ (the [[Lie groupoids]] which are the [[Lie integration]] of [[Atiyah Lie algebroids]] of $G$-[[principal bundles]]) from [[differential geometry]] to [[higher differential geometry]] and generally to [[higher geometry]].

Briefly, for $G$ an [[∞-group]] in an [[(∞,1)-topos]] and $P \to X$ a $G$-[[principal ∞-bundle]], its _higher Atiyah groupoid_ is the [[groupoid object in an (∞,1)-category|groupoid object]] $At(P)$ such that the

* object of [[objects]] is $X$;

* object of [[morphisms]] is the collection of all $G$-equivariant maps between all pairs of [[fibers]] of $P$.

In these vague words this is precisely the same description as for the traditional Atiyah groupoid. Definition \ref{HigherAtiyahGroupoid} below makes precise what this means in [[higher geometry]].

Besides generalizing the traditional definition to [[homotopy theory]], the notion of higher Atiyah groupoids also generalizes from [[concrete objects]] such as [[Lie groups]] to general objects in an [[(∞,1)-topos]] (general [[(∞,1)-stacks]], not necessarily "supported on points"), notably to _[[moduli ∞-stacks]]_ for [[cocycles]] in [[differential cohomology]]. For instance if we assume that the ambient [[(∞,1)-topos]] $\mathbf{H}$ is [[cohesive (∞,1)-topos|cohesive]] and consider $\mathbb{G} \in \mathrm{Grp}(\mathbf{H})$  a _[[sylleptic ∞-group]]_, then there is the [[moduli ∞-stack]] $\mathbf{B}\mathbb{G}_{\mathrm{conn}}$ of _$\mathbb{G}$-[[princical ∞-connections]]_ and this is itself again a [[group object in an (∞,1)-category|group object]]. 
A $(\mathbf{B}\mathbb{G}_{\mathrm{conn}})$-[[principal ∞-bundle]] is equivalently a $(\mathbf{B}^2\mathbb{G})$-[[principal ∞-connection]] "without cruving". For instance if $\mathbb{G} = U(1)$ is the [[circle group]] in [[smooth ∞-groupoids]], then 
$\mathbf{B}(\mathbf{B}\mathbb{G}_{\mathrm{conn}})$ classifies [[circle 2-bundle with connection]] without 2-form part: in parts of the literazire this is known as "[[bundle gerbes]] with connevitve structure but without curving".

So the general definition considered here Assigns a higher Atiyah groupoid to a "bundle gerbe with connective structure but no curving". It turns out that this is the _[[Courant 2-groupoid]]_ which [[Lie integration|Lie integrates]] the [[standard Courant Lie 2-algebroid]] traditionally induced by this data.

The  notion of higher Atiyah groupoids is more general still: the definition does not really require that the object fed into the construction is a plain [[principal ∞-bundle]]. It could for notably be a genuine [[principal ∞-connection]] (hence "_with_ curving"). We show below that the corresponding higher Atiyah groupoid is that groupoid object whose [[∞-group of bisections]] is the [[quantomorphism n-group]] of the principal $\infty$-connection regarded as a [[prequantum n-bundle]].

In summary, the [[higher geometry|higher geometric]] generalization of the notion of Atiyah groupoids unifies all three of the traditional notion of [[Atiyah groupoid]], of [[Courant 2-groupoid]] and of [[quantomorphism group]] and refines each of these to [[higher geometry]].

## Definition

Let $\mathbf{H}$ be an [[(∞,1)-topos]]. Let $G \in Grp(\mathbf{H})$ be a [[group object in an (∞,1)-category|group object]] in $\mathbf{H}$, an [[∞-group]].

We define now for every $G$-[[principal ∞-bundle]] $P \to X$ in $\mathbf{H}$ a _[[groupoid object in an (∞,1)-category|groupoid object]]_ $At(P) \in Grpd(\mathbf{H})$ in $\mathbf{H}$. In order to do so we invoke two basic facts.

+-- {: .num_prop #EffectiveEpisAreEquivalentlyGroupoids}
###### Proposition

The construction of forming the [[Cech nerve]] of a [[morphism]] consitutes an [[equivalence of (∞,1)-categories]] from that of [[1-epimorphisms]] to that of [[groupoid objects in an (∞,1)-category|groupoid objects]] in $\mathbf{H}$:

$$
  (\mathbf{H}^{\Delta^1})_{1epi}
  \stackrel{\simeq}{\to}
  Grpd(\mathbf{H})
 \,.
$$

=--

This is a refined version of one of the [[Giraud-Rezk-Lurie axioms]] characterizing [[(∞,1)-topos]], discussed at _[[groupoid object in an (∞,1)-category]]_.

+-- {: .num_remark}
###### Remark

In terms of traditional terminology in the literature on [[topological stacks]]/[[differentiable stacks]] etc, this says that a groupoid object in $\mathbf{H}$ is equivalently an object $X \in \mathbf{H}$ which is equipped with an [[atlas]] $X_0 \to X$.

=--

Write $\mathbf{B}G \in \mathbf{H}$ for the [[delooping]] of $G$ in $\mathbf{H}$ (the [[moduli ∞-stack]] of $G$-[[principal ∞-bundles]], as the following proposition asserts:

+-- {: .num_prop #ClassificationOfGPrincipalBundles}
###### Proposition

The operation of forming [[(∞,1)-fibers]] ([[homotopy fibers]]) constitutes an [[equivalence of ∞-groupoids]]

$$
  fib 
  \;\colon\;
  \mathbf{H}(X, \mathbf{B}G)
  \to 
  G Bund(X)
  \,.
$$

=--

This is discussed at _[[principal ∞-bundle]]_.

Using these two facts we now set:

+-- {: .num_defn #HigherAtiyahGroupoid}
###### Definition

For $P \to X$ a $G$-[[principal ∞-bundle]] in $\mathbf{H}$, its **Atiyah groupoid** is the [[groupoid object in an (∞,1)-category|groupoid object]] $At \in \mathrm{Grpd}(\mathbf{H}) \simeq (\mathbf{H}^{\Delta^1})_{1epi}$ which is the [[1-image]] projection of the classifying map $g \colon X \to \mathbf{B}G$:

$$
  g 
  \;\colon\;
  X
   \stackrel{}{\to}
  At(P) \coloneqq im_1(g)
  \hookrightarrow
  \mathbf{B}G
  \,.
$$  

=--

+-- {: .num_remark}
###### Remark

By the discussion at _[[1-image]]_, the 1-image projection of any morphism $f \colon X \to Y$ in an [[(∞,1)-topos]] is equivalently given as the canonical map given by the [[(∞,1)-colimit]] over the [[Cech nerve]]

$$
  X \to im_1(f) \simeq \underset{\rightarrow}{\lim} (X^{\times^{\bullet+1}_Y})
  \,.
$$

This means that regarded as an object of $Grpd(\mathbf{H})$, the Atiyah groupoid $At(P)$ _is_ simply the [[Cech nerve]] of the classifying map.

=--


## Examples

### The traditional Atiyah Lie groupoid

We discuss how the traditional notion of [[Atiyah groupoids]] in traditional [[differential geometry]] is a special case of highet Atiyah groupoids as discussed here.






