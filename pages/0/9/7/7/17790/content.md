
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Linear algebra
+-- {: .hide}
[[!include homotopy - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

The _tensor product_ of two vector spaces is a new vector space with the property that [[bilinear maps]] out of the [[Cartesian product]] of the two spaces are equivalently [[linear maps]] out of the tensor product.

The tensor product of vector spaces is just the special case of the [[tensor product of modules]] over some [[ring]] $R$ for the case that this ring happens to be a [[field]].

The tensor product of vector spaces makes the [[category]] [[Vect]] of all [[vector spaces]] into a [[monoidal category]], in fact a [[distributive monoidal category]].
 
## Definition

+-- {: .num_defn #TensorProductOfVectorSpaces} 
###### Definition

Given two [[vector spaces]] over some [[field]] $k$,  $V_1, V_2 \in Vect_k$, their [[tensor product of vector spaces]] is the vector space denoted

$$
  V_1 \otimes_k V_2 \in Vect
$$

whose elements are [[equivalence classes]] of formal linear combinations of [[tuples]] $(v_1,v_2)$ with $v_i \in V_i$, for the [[equivalence relation]] given by

$$
  (k v_1 , v_2) \;\sim\; k( v_1 , v_2) \;\sim\; (v_1, k v_2)
$$

$$
  (v_1 + v'_1 , v_2) \; \sim \; (v_1,v_2) + (v'_1, v_2)
$$

$$
  (v_1 , v_2 + v'_2) \; \sim \; (v_1,v_2) + (v_1, v'_2)
$$

More abstractly this means that the [[tensor product of vector spaces]] is the vector space characterized by the fact that

1. it receives a [[bilinear map]]
   
   $$
     V_1 \times V_2 \longrightarrow V_1 \otimes V_2
   $$

   (out of the [[Cartesian product]] of the underlying sets)

1. any other [[bilinear map]] of the form

   $$
     V_1 \times V_2 \longrightarrow V_3
   $$

   factors through the above bilinear map via a unique [[linear map]]

   $$
     \array{
        V_1 \times V_2 &\overset{bilinear}{\longrightarrow}& V_3
        \\
        \downarrow & \nearrow_{\mathrlap{\exists ! \, linear}}
         \\
         V_1 \otimes_k V_2
     }
   $$

=--


## References

* *Tensor Products*, §III.89 in: *The Princeton Companion to Mathematics* (2009) &lbrack;[doi:10.1515/9781400830398.301a](https://doi.org/10.1515/9781400830398.301a)&rbrack;


## Related concepts

* [[tensor product of modules]]

* [[tensor product of chain complexes]]

* [[tensor product of vector bundles]]

* [[graded vector space]]

* [[inductive tensor product]]

[[!redirects tensor products of vector spaces]]
