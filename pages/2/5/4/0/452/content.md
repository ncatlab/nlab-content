
#Definition:#   
 A **crossed module**,  $(C,G,\delta )$,  consists of groups  $C$  and  $G$  with a [[left action]] of  $G$  on  $C $,  written  $(g,c) \rightarrow  {}^{g}c$  for  $g \in  G$, $ c \in  C $,  and a group homomorphism  $\delta  : C \rightarrow  G$  satisfying the following conditions:
   
CM1)   for all  $c \in  C$  and  $g \in  G$,  
$$\delta (^{g}c) =g\delta(c)g^{-1},$$                       
CM2)  for all  $c_1, c_2 \in  C$,   
 $$^{\delta (c_2)}c_1 = c_2 c_1 c_2^{-1}.  $$                                  
(CM2 is called the **Peiffer identity**.)

#Examples#

* Any normal subgroup $N$ of a group $G$ gives rise to a crossed module $(N,G,inc)$ where $inc: N\to G$ is the inclusion map.

* Any $G$-module, $M$, gives rise to a crossed module $(M,G,0)$ with $0(m) = 1_G$ for all $m \in M$.

#Remarks:#

A crossed module gives rise to a [[2-group]] and vice-versa.