---
title: Display polytopes
teaching: 30
exercises: 0
questions:
- "..."
objectives:
- "..."
---


~~~
point3d(icosahedron, size=100)

~~~
{: .source .python}

~~~
---------------------------------------------------------------------------
TypeError Traceback (most recent call last)
<ipython-input-1-c2abeaa4fd8f> in <module>()
----> 1 point3d(icosahedron, size=Integer(100))

/Applications/SageMath/local/lib/python2.7/site-packages/sage/plot/plot3d/shapes2.pyc in point3d(v, size, **kwds)
   1157 except TypeError:
   1158 # argument is an iterator
-> 1159 v = list(v)
   1160 l = len(v)
   1161 

TypeError: 'function' object is not iterable
~~~
{: .error}


~~~
icosahedron=[v.change_ring(RDF) for v in icosahedron]
~~~
{: .source .python}

~~~
---------------------------------------------------------------------------
TypeError Traceback (most recent call last)
<ipython-input-2-1f12cb25ad56> in <module>()
----> 1 icosahedron=[v.change_ring(RDF) for v in icosahedron]

TypeError: 'function' object is not iterable
~~~
{: .error}


~~~
P=Polyhedron(icosahedron)
plot(P)

~~~
{: .source .python}

~~~
---------------------------------------------------------------------------
TypeError Traceback (most recent call last)
<ipython-input-3-bffb43d38643> in <module>()
----> 1 P=Polyhedron(icosahedron)
  2 plot(P)

/Applications/SageMath/local/lib/python2.7/site-packages/sage/geometry/polyhedron/constructor.pyc in Polyhedron(vertices, rays, lines, ieqs, eqns, ambient_dim, base_ring, minimize, verbose, backend)
496 """
497 # Clean up the arguments
--> 498 vertices = _make_listlist(vertices)
499 rays = _make_listlist(rays)
500 lines= _make_listlist(lines)

/Applications/SageMath/local/lib/python2.7/site-packages/sage/geometry/polyhedron/misc.pyc in _make_listlist(x)
 88 """
 89 if x is None: return []
---> 90 return [list(y) for y in x]
 91 
 92 

TypeError: 'function' object is not iterable
~~~
{: .error}


~~~
point3d(dodecahedron, size=100)

~~~
{: .source .python}

~~~
---------------------------------------------------------------------------
TypeError Traceback (most recent call last)
<ipython-input-4-71b742c5fe83> in <module>()
----> 1 point3d(dodecahedron, size=Integer(100))

/Applications/SageMath/local/lib/python2.7/site-packages/sage/plot/plot3d/shapes2.pyc in point3d(v, size, **kwds)
   1157 except TypeError:
   1158 # argument is an iterator
-> 1159 v = list(v)
   1160 l = len(v)
   1161 

TypeError: 'function' object is not iterable
~~~
{: .error}


~~~
point3d(icosidodecahedron, size=100)
~~~
{: .source .python}

~~~
---------------------------------------------------------------------------
NameError Traceback (most recent call last)
<ipython-input-5-8d3f381b9712> in <module>()
----> 1 point3d(icosidodecahedron, size=Integer(100))

NameError: name 'icosidodecahedron' is not defined
~~~
{: .error}
