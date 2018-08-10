---
title: IDD
teaching: 30
exercises: 0
questions:
- "..."
objectives:
- "..."
---

Show IDD is a root system.


~~~
IDD=icosidodecahedron

for points in IDD:
    if not (-points in IDD):
        print("first axiom violated")

for points in IDD:
    for refl in IDD:
        tmp = reflection_matrix(refl[1], n2=refl[2], n3=refl[3]) * points
        if not (tmp in IDD):
            print("second axiom violated", tmp)


~~~
{: .source .python}

~~~
---------------------------------------------------------------------------
NameError Traceback (most recent call last)
<ipython-input-1-a4505ffd1166> in <module>()
----> 1 IDD=icosidodecahedron
  2 
  3 for points in IDD:
  4 if not (-points in IDD):
  5 print("first axiom violated")

NameError: name 'icosidodecahedron' is not defined
~~~
{: .error}
