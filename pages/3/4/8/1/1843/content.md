#Contents#
* automatic table of contents goes here
{:toc}

# Idea #

Recall that the [[electromagnetic field]] is modeled as a cocycle in degree 2 ordinary [[differential cohomology]] and that this mathematical model is fixed by the fact that charged particles that trace out 1-dimensional trajectories couple to the electromagnetic field by an action functional that sends each trajectory to the holonomy of a $U(1)$-[[connection on a bundle|connection]] on it

When replacing particles with 1-dimensional trajectories by 2-particles with 2-dimensional trajectories, one accordingly expects that they may couple to a higher degree background field given by a degree 3 ordinary differential cocycle.

In [[string theory]] this situation arises and the corresponding background field appears, where it is called the _Kalb-Ramond field_  

Often it is also simply called the **$B$-field** , after the standard symbol used for the 2-forms $(B_i \in \Omega^2(U_i))$ on patches $U_i$ of a [[cover]] of spacetime that encode the field in analogy to how a collection of 1-forms $(A_i \in \Omega^1(U_i))$ encodes the [[electromagnetic field]].

Just as a degree 2 [[Deligne cohomology|Deligne cocycle]] is equivalently encoded in a $U(1)$-[[principal bundle]] [[connection on a bundle|with connection]], a degree 3 [[Deligne cohomology|Deligne cocycle]] is equivalently encoded in a $U(1)$-[[bundle gerbe]] with connection. The study of [[bundle gerbe]]s was largely motivated and driven by the desire to understand the Kalb-Ramond field.

One more degree higher the corresponding field is the [[supergravity C-field]].

# Mathematical model from (formal) physical input #

The derivation of the fact that the Kalb-Ramond field that is locally given by a 2-form is globally really a degree 3 [[Deligne cohomology|Deligne cocycle]] proceeds in itself in entire analogy with the corresponding discussion of the [[electromagnetic field]]:

* **classical background** The field strength 3-form $H \in \Omega^3(X)$ is required to be closed, $d H_3 = 0$.

* **quantum coupling** The gauge interaction with the quantum string is required to yield a well-defined surface holomomy in $U(1)$ from locally integrating the 2-forms $B_i \in \Omega^2(U_2)$ with $d B_i = H|_{U_i}$ over its 2-dimensional trajectory.


  $$
    hol(\Sigma)
    =
    \prod_{f} \exp(i \int_f \Sigma^* B_{\rho(f)})
    \prod_{e \subset f}
    \exp(i \int_{e} \Sigma^* A_{\rho(f) \rho(e)})
    \prod_{v \subset e \subset f}
    \exp(i \lambda_{\rho(f) \rho(e) \rho(v)})
  $$

  that this is well defined requires that

  $$
    \lambda_{i j k} - \lambda_{i j l} +
    \lambda_{i k l} - \lambda_{j k l}
    = 0 \;mod \, 2\pi
  $$

  which says that $(B_i, A_{i j}, \lambda_{i j k})$ is indeed a degree 3 [[Deligne cohomology|Deligne cocycle]].

#References#

One of the earliest articles that make the differential cohomological nature of the Kalb-Ramond field fully explicit is

* Dan Freed, E. Witten, _Anomalies in String Theory with D-Branes_ ([arXiv](http://arxiv.org/abs/hep-th/9907189))

which uses [[Cech cohomology]]-[[Deligne cohomology|Deligne]]-cocycles.


[[!redirects Kalb--Ramond field]]
[[!redirects Kalb–Ramond field]]