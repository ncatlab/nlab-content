
+-- {: .query}
Freyd's adjoint functor theorem (FAFT) is a fine thing when working classically but at the same time a source of inconstructivity. It ensures that under certain assumptions on a functor F : AA->BB all presheaves of the form BB(F(-),B) or all covariant presheaves of the form BB(B,F(-)) are representable. But for getting a right or left adjoint to F one has to CHOOSE for every B a representing object R(B) or L(B), respectively, i.e. BB(F(-),B) \cong BB(-,R(B)) or BB(B,F(-)) \cong BB(L(B),_), resp. Since BB typically will be large this requires GLOBAL CHOICE, i.e. choice for classes. This principle is independent even from ZFC.

For example using FAFT G.Plotkin has shown that there exist free commutative idempotent monoids in Domains, the so called Plotkin powerdomains. But to explicitate representatives even for a restricted class of domains (SFP objects) has required quite some additional effort and ingenuity.

In geometric topos theory it goes withut saying that a (finite limit preserving) colimit preserving functor between Grothendieck toposes has always a right adjoint. The point is that the solution set condition follows from the assumption that the involved toposes are Grothendieck and thus have small generating families. But for getting the right adjoints one has to use global choice. 

When working relative to a base topos SS one has to employ a fibred version of FAFT for fibrations over SS. The fibred right adjoints will not be split even if the original functors was split. That is one of the reasons why one works with fibrations and cartesian functors instead of split fibrations and split cartesian functors. For proving fibred FAFT one hast to employ strong choice principles on the meta-level, of course. 

It might be interesting to investigate how choice can be avoided in these cases using the work of Ahrens, Kapulkin and Shulman on "Univalent Categories and Rezk completion".

Thomas Streicher
=--