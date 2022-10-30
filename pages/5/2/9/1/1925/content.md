##Idea##

Heap is an algebraic structure which is basically
equivalent to group when one forgets which element is unit.
Similar notions are [[zoranskoda:affine space|affine space]], principal homogeneous space and so on. However, the notion of a heap has a directness and simplicity in the sense that it is an algebraic structure with only one ternary operation satisfying a short list of axioms. If we start with a group the ternary operation is defined via $(a,b,c)\mapsto ab^{-1}c$. 
We interpret that operation as shifting $a$ by the (right)
translation in the group which translates $b$ into $c$. 
There is also a dual version, [[quantum heap]]. 

##Definition##

A heap $(H,t)$ is a pair of the nonempty set $H$
and a ternary operation $t : H \times H \times H$ satisfying
relations

$$ t(b,b,c) = c = t(c,b,b)$$

$$ t(a,b,t(c,d,e)) = t(t(a,b,c),d,e) $$

##Automorphism group##

If we constructed a heap from a group, that the original group can be recovered up to isomorphism from its associated heap as an automorphism group of the heap. 
Let $(H,t)$ be a heap. We construct the automorphism
group of it. The elements of $Aut(H)$ will be set bijections
of the form $t(\cdot,a,b): H \rightarrow H$
where $a,b \in H$, and $\cdot$ is a place-holder and 
$Aut(H)$ becomes a group with respect to the composition 
(composing to the right):
\[ t(\cdot,c,d) \cdot_{Aut(H)} t(\cdot, a,b) =
 t(t(\cdot,c,d),a,b) = t(\cdot,c,t(d,a,b)). \]
The last expression proves that the result of the composition
is in $Aut(H)$, rather then only in symmetric group of $H$.
If that is (what is most sensible) taken as

the definition then the identity above is axiom for the action.
The inverse map (and inverse in the group
of $t(\cdot,a,b)$ is $t(\cdot,b,a)$ by the axioms
and the unit of the group is identity isomorphism $t(\cdot, x,x)$
where $x$ is any element of $H$. 
Thus $Aut(H)$ is a subgroup of the symmetric group of $H$.

The following are equivalent

(i) bijections $t(\cdot,a,b)$ and $t(\cdot,a',b')$ are
the same maps,

(ii) $t(a,a',b') = b$,

(iii) $t(b,b',a') = a$.

Proof. (ii) follows from (i) and $t(a,a,b) = b$.

(iii) follows from (ii) by applying $t(\cdot,b',a')$ on the
right. Similarly (ii) follows from (iii).

(i) follows from (ii) by the calculation:
\[ t(x,a',b') = t(t(x,a,a),a',b')= t(x,a,t(a,a',b'))
 = t(x,a,b).\]

One should conclude noticing that 
the defining action of $Aut(H)$ is transitive
(by $t(a,a,b) = b$) and  free (if $t(a,b,c) = a$ then
by the previous statement $t(x,b,c) = x$ for each $x$, and in particular $t(b,b,c) = b$ and also $t(b,b,c) = c$.

##References##

* G.M. Bergman, A.O. Hausknecht,
_Cogroups and co-rings in categories of associative rings_, 
Ch.IV, paragraph 22, p.95ff  -- Providence, R.I. : AMS 1996.

