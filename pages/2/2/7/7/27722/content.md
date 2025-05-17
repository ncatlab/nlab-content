
\tableofcontents

> Draft -- page under development. Help in completing it is welcome.



## Motivations and idea

The original motivations and applications for the *Scott adjunction* come from [[model theory]] &lbrack;[Henry 2019](#Henry2019)&rbrack;, but a lot of its scientific placing and naming choices have a [[geometry|geometric]] flavour. 




### Geometric intuition

####Rudiments on the Scott topology

> To be written. Reproduce parts of Sec 1 of [Di Liberti 2022](#DiLiberti22) and mention categorification.

The set of points of a locale has both a canonical topology and canonical partial order. The first of these structures gives raise to the sometimes called Isbell adjunction [cite towards higher topology], which related locales to topological spaces.

[Insert here statement of the adjunction]

The duality between sober spaces and locales with enough points is a very celebrated result in the theory of dualities, and many other dualities of topological kind happen as sub dualities of this one.

For the second structure, let us recall a couple of properties of such partial order. Let O be a locale. Then its poset of points has directed joins, and every morphism of locales induces a directed join preserving morphism of posets. Thus we obtain a (2-) functor from the (2-)category of locales to that of posets with directed joins.

It is natural to wonder wether this process can be reversed, i.e. whether we can associate a locale to a directed poset with joins, hoping for assigning a topology to each reasonable poset.

In the 1980s Scott defined the Scott topology of a good enough poset, which assigns to a poset with directed joins a topological space. Yet, an analysis of this construction yields precisely what we are looking for. For P a locale, and T the booleans, the poset Pos(P,T) is precisely the opens of the Scott topology over P, and provides a locale associated to our posets.

[Insert here statement of the adjunction]

#### Higher Topology



### Logical aspects

> To be written. Free geometric theory associated to an accessible category with directed colimits. Recap of the intro of Formal Model Theory & Higher Topology. 

> Mention formal model theory and Create separate entries for it.

## Applications

> To be written. Focus on [Henry 2019](#Henry2019).

 


## References

* {#Henry2019} [[Simon Henry]]: *An abstract elementary class non-axiomatizable in $L_{\infty, \kappa}$*, The Journal of Symbolic Logic **84** 3 (2019) 1240-1251  &lbrack;[arXiv:1812.00652](https://arxiv.org/abs/1812.00652), [doi:10.1017/jsl.2019.25](https://doi.org/10.1017/jsl.2019.25)&rbrack;


* [[Ivan Di Liberti]]: *The Scott adjunction* &lbrack;[arXiv:2009.07320](https://arxiv.org/abs/2009.07320)&rbrack;

* [[Ivan Di Liberti]]: *General facts on the Scott Adjunction*, Applied Categorical Structures **30** (2022) 569–591 &lbrack;[arXiv:2009.14023](https://arxiv.org/abs/2009.14023), [doi:10.1007/s10485-021-09666-6](https://doi.org/10.1007/s10485-021-09666-6)&rbrack;

* {#DiLiberti22} [[Ivan Di Liberti]]: *Towards higher topology*, Journal of Pure and Applied Algebra **226** 3 (2022) 106838 &lbrack;[arXiv:2009.14145](https://arxiv.org/abs/2009.14145), [doi:10.1016/j.jpaa.2021.106838](https://doi.org/10.1016/j.jpaa.2021.106838)&rbrack;

* [[Ivan Di Liberti]]: *Formal model theory and higher topology*, Mathematical Logic Quarterly **70** 1 (2024) &lbrack;[arXiv:2010.00319](https://arxiv.org/abs/2010.00319), [doi:10.1002/malq.202300006](https://doi.org/10.1002/malq.202300006)&rbrack;


[[!redirects Scott adjunction]]

