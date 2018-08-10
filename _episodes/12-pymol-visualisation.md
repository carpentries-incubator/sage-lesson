---
title: More advanced Caspar-Klug orbits and pymol visualisation
teaching: 30
exercises: 0
questions:
- "..."
objectives:
- "..."
---


~~~
seeds = [[ 0.904721509025590, 0.0879675935421300, 0.416822136685000], 
[0.979660168810660, 0.0952540054366200, 0.176614348770000], 
[0.894764055651420, 0.317512115546100, 0.313979842320000],
[0.986175314321600, 0.165705309322800, 0]]
seeds

T4capsid = []

for seed in seeds:
    for i in range(count_even):
        T4capsid.append(g_even[i] * seed)
        
point3d(T4capsid, size=100)
        
        
~~~
{: .source .python}

~~~
---------------------------------------------------------------------------
NameError Traceback (most recent call last)
<ipython-input-1-871835d35841> in <module>()
  8 
  9 for seed in seeds:
---> 10 for i in range(count_even):
 11 T4capsid.append(g_even[i] * seed)
 12 

NameError: name 'count_even' is not defined
~~~
{: .error}
