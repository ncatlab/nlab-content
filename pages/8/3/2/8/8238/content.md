
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A _tower_ is a [[diagram]] of the shape of the [[poset]] of [[natural numbers]]

$$
  \cdots \to X_2 \to X_1 \to X_0 
  \,.
$$


A [[limit]] over a diagram of this form is called a [[sequential limit]]/[[directed limit]].


Different contexts lead to different notions of morphism of towers, so it is important to consider what category of towers is appropriate for any given use of these objects. In addition to [[Postnikov towers]], and related uses in decomposing homotopy types, towers also occur as a simple type of [[pro-object]] in a category.  In that situation the morphisms considered between towers are usually pro-morphisms.

In [[homotopy theory]] in the presence of [[(infinity,1)-limits]]/[[(infinity,1)-colimits]], every tower is a [[tower of homotopy fibers]].


## The pro-category of towers
 {#TheProCategoryOfTowers}

### Definition

The tower diagram shape $\mathbb{N}_{\geq} = \{\cdots 3\to 2 \to 1 \to 0\}$ is evidently a small [[cofiltered category]]. As such it makes sense to consider _pro-morphisms_ between tower diagrams: 



+-- {: .num_defn #ProCategoryOfTowers}
###### Definition


For any small category $\mathcal{C}$, the [[full subcategory]]

$$
  i
   \;\colon\;
  Tow_{pro}(\mathcal{C})
    \overset{}{\hookrightarrow}
  Pro(\mathcal{C})
    \hookrightarrow
  PSh(\mathcal{C})
$$

of the category $Pro(\mathcal{C})$ of [[pro-objects]] in $\mathcal{C}$ on those that have presentation by formal [[sequential limits]] (formal limits over tower diagrams) is the **pro-category of towers** $Tow_{pro}(\mathcal{C})$ in $\mathcal{C}$.

=--

(e.g. [Blanc 96, def. 2.5](#Blanc96))

For $X_\bullet \colon \mathbb{N}_{\geq} \longrightarrow \mathcal{C}$ a tower diagram, we write

$$
  \underset{\longleftarrow}{\lim}^f X_\bullet \in Tow_{pro}(\mathcal{C}) \hookrightarrow Pro(\mathcal{C}) 
$$

for its formal cofiltered limit, i.e.

$$
  \underset{\longleftarrow}{\lim}^f
   \;\colon\;
  Tow(\mathcal{C})
    \longrightarrow
  Top_{pro}(\mathcal{C})
  \,.
$$



### Properties


Notice that generally we have that morphisms between formal cofiltered limits (pro-objects) of shapes $\mathcal{K}_1$ and $\mathcal{K}_2$, respectively, are represented as cofiltered limits of systems of morphisms indeced on a single cofiltered category $\mathcal{K}$ equipped with [[final functors]] to $\mathcal{K}_1$ and $\mathcal{K}_2$, respectively. (See at _[[ind-object]]_ [this prop.](ind-object#MorphismsRepresentedByCofilteredSystemsOfMorphisms)).

The following says that in the case that both shapes are towers, then also $\mathcal{K}$ may always be chosen to be of tower shape: 

+-- {: .num_prop #ProMorphismsBetweenTowerDiagrams}
###### Proposition

For $X_\bullet$ and $Y_\bullet$ two tower diagrams in $\mathcal{C}$, then every morphism

$$  
   \phi
     \;\colon\;
   \underset{\longleftarrow}{\lim}^f X_\bullet
     \longrightarrow
   \underset{\longleftarrow}{\lim}^f Y_\bullet
$$

between their formal cofiltered limits (every pro-morphism between the diagrams) in $Tow_{pro}(\mathcal{C}) \hookrightarrow Pro(\mathcal{C})$ is represented by component morphisms

$$
  \phi_{k} \;\colon\; X_{h(k)} \longrightarrow X_k
$$

making [[commuting diagrams]]

$$
  \array{
     X_{h(k+1)} &\overset{\phi_{k+1}}{\longrightarrow}& Y_{k+1}
     \\
     \downarrow
       &&
     \downarrow
     \\
     X_{h(k)}
       &\underset{\phi_k}{\longrightarrow}&  
     Y_k
  }
$$

i.e. by a [[natural transformation]] $\phi_\bullet$ between

$$
  \mathbb{N}_{\geq} \overset{h}{\longrightarrow} \mathbb{N}_{\geq} \overset{X_\bullet}{\longrightarrow} \mathcal{C}
$$

and

$$
  \mathbb{N}_{\geq} \overset{Y_\bullet}{\longrightarrow} \mathcal{C}
$$

as 

$$
  \phi \simeq \underset{\longleftarrow}{\lim}^f (\phi_\bullet)
  \,.
$$

=--

(e.g. [Blanc 96, p. 6](#Blanc96), [Libman, p.4](#Libman))


+-- {: .num_prop #FiniteLimitsInProCategoryOfTowers}
###### Proposition

The pro-category of towers $Tow_{pro}(\mathcal{C})$ (def. \ref{ProCategoryOfTowers}) has all [[finite limits]] and [[finite colimits]]. Moreover these are presented by the degreewise finite limits of any representing diagram of towers, via prop. \ref{ProMorphismsBetweenTowerDiagrams}.

=--

([Blanc 96, pop. 2.7](#Blanc96))


## Examples

* [[Postnikov tower]]

* [[Whitehead tower]]

* [[chromatic tower]]

## Related concepts

* [[filtered object in an (infinity,1)-category]]

## References

* {#Blanc96} [[David Blanc]], _Colimits for the pro-category of towers of simplicial sets_, Cahiers de Topologie et G&#233;om&#233;trie Diff&#233;rentielle Cat&#233;goriques (1996) Volume: 37, Issue: 4, page 258-278 ([numdam](http://www.numdam.org/item?id=CTGDC_1996__37_4_258_0))

* {#Libman} [[Assaf Libman]], _Tower techniques for cofacial resolutions_,  Hopf archive ([pdf](http://hopf.math.purdue.edu/Libman/towers.pdf))

[[!redirects tower diagram]]
[[!redirects towers]]
[[!redirects tower diagrams]]

[[!redirects cotower]]
[[!redirects cotowers]]

[[!redirects co-tower]]
[[!redirects co-towers]]

[[!redirects cotower diagram]]
[[!redirects cotower diagrams]]

[[!redirects co-tower diagram]]
[[!redirects co-tower diagrams]]

[[!redirects pro-category of towers]]
[[!redirects pro-categories of towers]]

