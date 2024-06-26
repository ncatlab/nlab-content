
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Setup and definition ##

Given a [[continuous map]] $\pi \colo E \to B$ of [[topological spaces]], one constructs the __[[mapping cocylinder]]__ $Cocyl(\pi)$ as the [[pullback]] 

$$
  \array{
    Cocyl(\pi) 
      &\overset{pr_{\mathcal{P}(B)}}\longrightarrow 
    & \mathcal{P}(B)
    \\
    \mathllap{{}^{\pr_E}}\Big\downarrow && \Big\downarrow
    \\
    E & \underset{\pi}\longrightarrow & B
  }
$$  

where $\mathcal{P}(B)$ is the [[path object|path space]] in [[Top]], the space of continuous [[interval object|path]]s 
$u:[0,1]\to B$ in $B$, and where $\mathcal{P}(B)\to B$ is the map sending a path $u$ to its value $u(0)$. 
The cocylinder can be realized as a subspace of $E\times \mathcal{P}(B)$ consisting of pairs $(e,u)$ where $e\in E$ and $u:[0,1]\to B$ are such that $\pi(e)=u(0)$.

+-- {: .num_defn}
###### Definition

A __Hurewicz connection__ is any continuous [[section]] 
$$s:Cocyl(\pi)\to \mathcal{P}(E)$$ 
of the map $\pi_!:\mathcal{P}(E)\to Cocyl(\pi)$ given by $\pi_!(u)=(u(0),\pi\circ u)$. 

=--


## Characterization of Hurewicz fibrations ##

+-- {: .num_theorem }
###### Theorem

A map $\pi:E\to B$ is a __[[Hurewicz fibration]]__ iff there exists at least one Hurewicz connection for $\pi_!$. 

=--


+-- {: .proof}
###### Proof

To see that consider the following diagram 
$$\begin{matrix}
Y& \stackrel{\theta}\to & Cocyl(\pi) &\overset{pr_E}\to & E\\
\sigma_0\downarrow&&\sigma_0\downarrow&&\downarrow \pi\\
Y\times I&\stackrel{\theta\times I}\underset{}{\to}& Cocyl(\pi)\times I& \underset{ev}\to &B
\end{matrix}$$
where $pr_E: Cocyl(\pi)\to E$ is the restriction of the projection $E\times B^I\to E$ to the factor $E$ and the map $Cocyl(\pi)\times I\to B$ is the evaluation $(e,u,t)\mapsto u(t)$ for $(e,u)\in Cocyl(\pi)$. The right-hand square is commutative and this square defines a homotopy lifting problem. If $\pi$ is a fibration this **universal** homotopy lifting problem has a solution, say $\tilde{s}:Cocyl(p)\times I\to E$. By the hom-mapping space adjunction (exponential law) this map corresponds to some map $s:Cocyl(\pi)\to \mathcal{P}(E)$. One can easily check that this map is a section of $\pi_!$. 

Conversely, let a Hurewicz connection $s$ exist, and fill the right-hand square of the diagram with diagonal $\tilde{s}$ obtained by hom-mapping space adjunction. Let the data for the general homotopy lifting problem be given: $\tilde{f}:Y\to E$, $F:Y\times I\to B$ with $F_0 = p\circ \tilde{f}:Y\to E$; let furthermore $F':Y\to \mathcal{P}(B)$ be the map obtained from $F$ by the hom-mapping space adjunction. By the universal property of the cocylinder (as a pullback), there is a unique mapping $\theta: Y\to Cocyl(\pi)$ such that $pr_{\mathcal{P}(B)}\circ\theta=F':Y\to \mathcal{P}(B)$ and $pr_E\circ\theta =\tilde{f}:Y\to E$. Now notice that the by composing the horizontal lines we obtain $\tilde{f}$ upstairs and $F$ downstairs, hence the external square is the square giving the homotopy lifting problem for this pair. The lifting is then given by $\tilde{s}\circ (\theta\times id_I):Y\times I\to E$. Simple checking finishes the proof. 

=--


Of course there are many other equivalent characterizations of Hurewicz fibrations. 


## Special cases and properties ##

If $\pi:E\to B$ is a [[covering space]] where $B$ is [[Hausdorff space|Hausdorff]], then $\pi_!$ is a [[homeomorphism]]; thus in that case the Hurewicz connection is unique. 

If $\pi$ is a smooth principal bundle equipped with a distribution of horizontal spaces forming an [[Ehresmann connection]], then one can define a corresponding "smooth" Hurewicz connection in the sense that the Ehresmann connection provides a continuous choice of smooth path lifting, with prescribed initial point, of a smooth path in the base. This can be expressed in terms as a continuous section of $\pi_!^{smooth}:\mathcal{P}^{smooth}(E)\to Cocyl^{smooth}(\pi)$ where the subspaces of smooth paths are used. 

## References

The original article:

* [[Witold Hurewicz]], _On the concept of fiber space_, Proc. Nat. Acad. Sci. USA __41__ (1955) 956-961 &lbrack;[PNAS pdf](http://www.pnas.org/content/41/11/956.full.pdf), MR0073987 (17,519e)&rbrack;

Review:

* [[James Eells]], Jr.: *Fibring spaces of maps*, in: Richard Anderson (ed.) *Symposium on infinite-dimensional topology*, Annals of Mathematics Studies **69**, Princeton University Press (1972, 2016) 43-57 &lbrack;[ISBN:9780691080871](https://press.princeton.edu/books/paperback/9780691080871/symposium-on-infinite-dimensional-topology-am-69-volume-69), [[Eells-FibringSpaces.pdf:file]]&rbrack;


[[!redirects Hurewicz connections]]
