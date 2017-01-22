---
title: Orbits
teaching: 30
exercises: 0
questions:
- "..."
objectives:
- "..."
---

Make an icosahedron by picking a seed vector on a 5-fold axis


~~~
icosahedron_dupl = []
T5 = vector([0,1,1.618]) 
seed = T5
for i in range(counteven):
    icosahedron_dupl.append(g_even[i] * seed)



# now delete duplicates - do ito golden ratio, or round or convert to set etc

icosahedron_dupl

icosahedron = []


# define function take orbit
~~~
{: .source .python}

~~~
---------------------------------------------------------------------------
NameError Traceback (most recent call last)
<ipython-input-1-23df852badd3> in <module>()
  2 T5 = vector([Integer(0),Integer(1),RealNumber('1.618')])
  3 seed = T5
----> 4 for i in range(counteven):
  5 icosahedron_dupl.append(g_even[i] * seed)
  6 

NameError: name 'counteven' is not defined
~~~
{: .error}
Make a dodecahedron by picking a seed vector on a 3-fold axis


~~~
dodecahedron = []
T3 = vector([1,1,1]) 
seed = T3
for i in range(counteven):
    dodecahedron.append(g_even[i] * seed)



# now delete duplicates - do ito golden ratio, or round or convert to set etc
# define function take orbit
~~~
{: .source .python}

~~~
---------------------------------------------------------------------------
NameError Traceback (most recent call last)
<ipython-input-2-19e7573373b6> in <module>()
  2 T3 = vector([Integer(1),Integer(1),Integer(1)])
  3 seed = T3
----> 4 for i in range(counteven):
  5 dodecahedron.append(g_even[i] * seed)
  6 

NameError: name 'counteven' is not defined
~~~
{: .error}
Make a icosidodecahedron by picking a seed vector on a 2-fold axis


~~~
icosidodecahedron = []
T2 = vector([1,0,0]) 
seed = T2
for i in range(counteven):
    icosidodecahedron.append(g_even[i] * seed)

# plot
# now delete duplicates - do ito golden ratio, or round or convert to set etc


~~~
{: .source .python}

~~~
---------------------------------------------------------------------------
NameError Traceback (most recent call last)
<ipython-input-3-c316e265773c> in <module>()
  2 T2 = vector([Integer(1),Integer(0),Integer(0)])
  3 seed = T2
----> 4 for i in range(counteven):
  5 icosidodecahedron.append(g_even[i] * seed)
  6 

NameError: name 'counteven' is not defined
~~~
{: .error}
