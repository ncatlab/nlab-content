

The term **moduli space** is essentially a synonym for [[classifying space]]. People tend to say "classifying space" when in the content of [[topology]], and they tend to say _moduli space_ when in a context of [[complex geometry]] or [[algebraic geometry]].

The term possibly originates with Riemann, who was the first to study what are now called moduli spaces of [[Riemann surface]]s. A "modulus" here is a _parameter_ that parameterizes Riemann surfaces.

More precisely, when a moduli space actually does exist as a genuine space (or [[scheme]]), it is called for emphasis a **fine moduli space**. 

Those classifying "spaces" that are called moduli spaces are typically [[orbifold]]s, hence modeled not just as spaces but as [[groupoid]]s with extra structure. These are typically conceived as [[stack]]s: these are then called **moduli stack**s. Typically these are demanded to be [[Deligne-Mumford stack]]s.

So the term _fine moduli space_ mainly indicates that a given object that might be a [[Deligne-Mumford stack]] is actually just a plain [[scheme]]. But there is also the notion of **coarse moduli space**, which is a kind of conceptual hack designed to be able to keep thinking about what really wants to be a [[stack]] still as a plain [[sheaf]]:

A **coarse moduli space** for a [[presheaf]] $(Sch/\mathbb{C})^{op} \to Set$ on complex [[scheme]]s is a [[scheme]] $M \in Sch/\mathbb{C}$ equipped with a morphism 

$$
  \Psi_M : F \to h_M
  \,,
$$ 

where $h$ denotes the [[Yoneda embedding]], such that 

a) $F(Spec(\mathbb{C})) \to h_M(Spec \mathbb{C}) = hom(Spec \mathbb{C}, M)$ is a [[bijection]]
 
b) given $M'$ and $\Psi_{M'} : F \to h_{M'}$ then there exists unique $M \to M'$ such that $\array{ F && \stackrel{\Psi_{M'}}{\to}&& h_{M'} \\ & {}_{\Psi_M}\searrow && \nearrow \\ && h_M} $

So a coarse moduli space is one that at least has the right underlying set of points as the _right_ moduli stack has: as long as we don't look at families but just at single things, it does give the right information.


#related entries#

A bit of elementary exposition of these ideas is at 

* [[basic ideas of moduli stacks of curves and Gromov-Witten theory]]

[[!redirects fine moduli space]]
[[!redirects coarse moduli space]]
[[!redirects moduli stack]]
