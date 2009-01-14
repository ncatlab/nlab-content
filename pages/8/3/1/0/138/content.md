#Idea#

_Hypercover_ is another word for 
[[acyclic fibration]] in 
[[model category|model categories]] of _higher structures_ such as 
[[globular set|globular sets]] and [[simplicial set|simplicial sets]] and the
[[infinity-category|infinity-categories]] and
[[omega-category|omega-categories]] based on them.

#Origin of the term#

The term _hypercover_ originates in the fact that for
$\pi : Y \to X$ any [[regular epimorphism]], hence an 
ordinary [[cover]], the [[simplicial set|simplicial object]]

$$
  Y^\bullet
  :=
  (\cdots \to Y \times_X Y \times_X Y \stackrel{\stackrel{\to}{\to}}{\to} Y \times_X Y \stackrel{\to}{\to} Y)
$$

is an acyclic fibration

$$
  Y^\bullet \to X
$$

over $X$ of simplicial objects, but not all acyclic fibrations
arise this way: a generic hypercover of simplicial objects
is obtained by starting with a cover $Y \to X$, then choosing
a cover of the fiber product $Y \times_X Y$, and so on.


#Characterization by lifting property#

Hypercovers are usually (for instance in the [[model structure on simplicial sets]] characterized as being those
morphisms $\pi : Y \to X$ for which all images 
$\pi(\partial C^n)$
of boundaries $\partial C^n$ of standard $n$-cells 
[[globe|globes]] $C^n = G^n$ or [[simplex|simplices]],
$C^n = \Delta^n$) every $n$-cell filling this boundary in 
$X$ lifts to $Y$.

Diagrammatically this means: $f : Y \to X$ is a hypercover
if for all commuting diagrams

$$
  \array{
    \partial C^n &\to & Y
    \\
    \downarrow && \downarrow^\pi
    \\
    C^n &\to& X
  }
$$

there exists a diagonal lift

$$
  \array{
    \partial C^n &\to & Y
    \\
    \downarrow &{}^{\exists}\nearrow& \downarrow^\pi
    \\
    C^n &\to& X
  }
  \,.
$$

#Hypercovers in different model categories#

In the context of the [[model structure on simplicial sets]], these are the hypercovers proper. In the context of 
the [[folk model structure]] on 
[[strict omega-category|strict omega-categories]]
this are the 
$\omega$-functors which are [[k-surjectivity|k-surjective]]
for all $k$.

#Relation to fibrations#

The condition on hypercovers, being _acyclic fibrations_ is closely related to the condition on _fibrations_. Usually the lifting property for fibrations is obtained from that for hypercovers by removing in the boundary $\partial C^n$ of the standard $n$-cell one face.

For instance the definition of a hypercover of simplicial sets becomes that of a [[Kan fibration]] if the full boundary $\partial \Delta$ is replaced by a [[horn]] $\Lambda^k[n]$.

In the globular set by replacing the inclusion $\partial G^n \hookrightarrow G^n$ of the boundary of the standard $n$-[[globe]] into the $n$-globe with the inclusion $G^{n-1} \hookrightarrow G^n$ of the standard $(n-1)$-globe (which is one-half of the full boundary), the above lifting condition is that of fibrations in the [[folk model structure]] on [[omega-groupoid|omega-groupoids]].






