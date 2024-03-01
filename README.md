#TSAI Assignment 6

## Formulas to remember:

h1 = w1*i1 + w2*i2		
h2 = w3*i1 + w4*i2		
a_h1 = σ(h1) = 1/(1 + exp(-h1))		
a_h2 = σ(h2)		
o1 = w5*a_h1 + w6*a_h2		
o2 = w7*a_h1 + w8*a_h2		
a_o1 = σ(o1)		
a_o2 = σ(o2)		
E_total = E1 + E2		
E1 = ½ * (t1 - a_o1)²		
E2 = ½ * (t2 - a_o2)²

We get ∂E_total/∂w5 and expand it:-

∂E_total/∂w5 = ∂(E1 + E2)/∂w5					
∂E_total/∂w5 = ∂E1/∂w5					
∂E_total/∂w5 = ∂E1/∂w5 = ∂E1/∂a_o1*∂a_o1/∂o1*∂o1/∂w5	

In this we know that:

∂E1/∂a_o1 =  ∂(½ * (t1 - a_o1)²)/∂a_o1 = (a_01 - t1)					
∂a_o1/∂o1 =  ∂(σ(o1))/∂o1 = a_o1 * (1 - a_o1)					
∂o1/∂w5 = a_h1

Replace in equation and we get:-

∂E_total/∂w5 = (a_01 - t1) * a_o1 * (1 - a_o1) *  a_h1	

Similarly:- 

∂E_total/∂w6 = (a_01 - t1) * a_o1 * (1 - a_o1) *  a_h2					
∂E_total/∂w7 = (a_02 - t2) * a_o2 * (1 - a_o2) *  a_h1					
∂E_total/∂w8 = (a_02 - t2) * a_o2 * (1 - a_o2) *  a_h2	

Now to get ∂E_total/∂w1

∂E1/∂a_h1 = (a_01 - t1) * a_o1 * (1 - a_o1) * w5								
∂E2/∂a_h1 = (a_02 - t2) * a_o2 * (1 - a_o2) * w7					

Expanding:-

∂E_total/∂a_h1 = (a_01 - t1) * a_o1 * (1 - a_o1) * w5 +  (a_02 - t2) * a_o2 * (1 - a_o2) * w7								
∂E_total/∂a_h2 = (a_01 - t1) * a_o1 * (1 - a_o1) * w6 +  (a_02 - t2) * a_o2 * (1 - a_o2) * w8		

From which we get:

∂E_total/∂w1 = ∂E_total/∂a_h1 * ∂a_h1/∂h1 * ∂h1/∂w1					
∂E_total/∂w2 = ∂E_total/∂a_h1 * ∂a_h1/∂h1 * ∂h1/∂w2					
∂E_total/∂w3 = ∂E_total/∂a_h2 * ∂a_h2/∂h2 * ∂h2/∂w3	

Expanding:-

∂E_total/∂w1 = ((a_01 - t1) * a_o1 * (1 - a_o1) * w5 +  (a_02 - t2) * a_o2 * (1 - a_o2) * w7) * a_h1 * (1 - a_h1) * i1												
∂E_total/∂w2 = ((a_01 - t1) * a_o1 * (1 - a_o1) * w5 +  (a_02 - t2) * a_o2 * (1 - a_o2) * w7) * a_h1 * (1 - a_h1) * i2												
∂E_total/∂w3 = ((a_01 - t1) * a_o1 * (1 - a_o1) * w6 +  (a_02 - t2) * a_o2 * (1 - a_o2) * w8) * a_h2 * (1 - a_h2) * i1												
∂E_total/∂w4 = ((a_01 - t1) * a_o1 * (1 - a_o1) * w6 +  (a_02 - t2) * a_o2 * (1 - a_o2) * w8) * a_h2 * (1 - a_h2) * i2									
			




