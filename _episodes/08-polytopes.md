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
<ipython-input-1-ac7152bff65d> in <module>()
----> 1 point3d(icosahedron, size=Integer(100))

/home/raniere/src/sagemath/local/lib/python2.7/site-packages/sage/plot/plot3d/shapes2.pyc in point3d(v, size, **kwds)
   1126 except TypeError:
   1127 # argument is an iterator
-> 1128 v = list(v)
   1129 l = len(v)
   1130 

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
<ipython-input-2-1b3d6e6c9ee0> in <module>()
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
<ipython-input-3-ca2e0cfea00f> in <module>()
----> 1 P=Polyhedron(icosahedron)
  2 plot(P)

/home/raniere/src/sagemath/src/sage/misc/lazy_import.pyx in sage.misc.lazy_import.LazyImport.__call__ (/home/raniere/src/sagemath/src/build/cythonized/sage/misc/lazy_import.c:3646)()
387 True
388 """
--> 389 return self._get_object()(*args, **kwds)
390 
391 def __repr__(self):

/home/raniere/src/sagemath/local/lib/python2.7/site-packages/sage/misc/decorators.pyc in wrapper(*args, **kwds)
710 kwds[new_name] = kwds[old_name]
711 del kwds[old_name]
--> 712 return func(*args, **kwds)
713 
714 return wrapper

/home/raniere/src/sagemath/local/lib/python2.7/site-packages/sage/geometry/polyhedron/constructor.pyc in Polyhedron(vertices, rays, lines, ieqs, eqns, ambient_dim, base_ring, minimize, verbose, backend)
366 """
367 # Clean up the arguments
--> 368 vertices = _make_listlist(vertices)
369 rays = _make_listlist(rays)
370 lines= _make_listlist(lines)

/home/raniere/src/sagemath/local/lib/python2.7/site-packages/sage/geometry/polyhedron/misc.pyc in _make_listlist(x)
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
<ipython-input-4-d68179445688> in <module>()
----> 1 point3d(dodecahedron, size=Integer(100))

/home/raniere/src/sagemath/local/lib/python2.7/site-packages/sage/plot/plot3d/shapes2.pyc in point3d(v, size, **kwds)
   1126 except TypeError:
   1127 # argument is an iterator
-> 1128 v = list(v)
   1129 l = len(v)
   1130 

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
<ipython-input-5-48adc3c484d9> in <module>()
----> 1 point3d(icosidodecahedron, size=Integer(100))

NameError: name 'icosidodecahedron' is not defined
~~~
{: .error}
