Given a [[continuous map]] $\pi : E\to B$ of [[topological spaces]], one constructs the __[[cocylinder]]__ $Cocyl(\pi)$ as the [[pullback]] 
$$\array{
Cocyl(\pi)\to & \mathcal{P}(B)\\
\downarrow & \downarrow\\
E\stackrel{\pi}\to & B
}$$  
where $\mathcal{P}(B)$ is the [[path space]], the space of continuous [[path]]s 
$u:[0,1]\to B$ in $B$, and where $\mathcal{P}(B)\to B$ is the map sending a path $u$ to its value $u(0)$. 
The cocylinder can be realized as a subspace of $E\times \mathcal{P}(B)$ consisting of pairs $(p_0,u)$ where $p_0\in E$ and $u:[0,1]\to \mathcal{P}(B)$ are such that $\pi(p_0)=u(0)$.

A __Hurewicz connection__ is any continuous [[section]] 
$$s:Cocyl(\pi)\to \mathcal{P}(E)$$ 
of the map $\pi_!:\mathcal{P}(E)\to Cocyl(\pi)$ given by $\pi_!(u)=(u(0),\pi\circ u)$. 

A map $\pi:E\to B$ is a __[[Hurewicz fibration]]__ if there exist at least one Hurewicz connection for $\pi_!$. Of course there are many equivalent characterizations. 

If $\pi:E\to B$ is a [[covering space]] where $B$ is [[Hausdorff space|Hausdorff]], then $\pi_!$ is a [[homeomorphism]]; thus in that case the Hurewicz connection is unique. 

If $\pi$ is a smooth principal bundle equipped with a distribution of horizontal spaces forming an [[Ehresmann connection]], than one can define a corresponding smooth Hurewicz connection. 