##Idea##
An inverse sequence of groups  satisfies the _Mittag-Leffler condition_ if the images of groups from far down the sequence do not get smaller.

An inverse sequence of groups consists of some groups $G_n$ indexed by the natural numbers  and between them group homomorphisms: if $m \gt n$, there is a homomorphism $p^m_n : G_m \to G_n$ and if $l\gt m  \gt n$ $p^m_np^l_m= pl_n$, so that we really just need the $p^{n+1}_n$s to define everything.


##Definition##
An inverse system $G = \{G_n,p^m_n\}$ is said to _satisfy the Mittag-Leffler condition_ if

for any $n$, there is an $n^\prime \gt n$ such that for any $n^{\prime\prime} \gt n^\prime$, 


$$p^{n^{\prime\prime}}_n(G_{n^{\prime\prime}}) = p^{n^\prime}_n(G_{n^\prime}).$$

##Discussion##

This is the 'classical' form of the condition. It can also be applied in any category where images make sense. 

An inverse sequence is a special type of [[pro-object]] and it is well known and quite easy to show that any Mittag-Leffler pro-object like this is isomorphic to one which is [[essentially epimorphic pro-object|essentially epimorphic]].
