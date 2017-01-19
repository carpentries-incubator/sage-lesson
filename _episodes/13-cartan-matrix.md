---
title: Cartan matrix and Perron-Frobenius eigenvector
teaching: 30
exercises: 0
questions:
- "..."
objectives:
- "..."
---


~~~
# define Cartan matrix - function of arbitrary number of vectors?

# find eigenvalues using SAGE routine

# find the Perron-Frobenius eigenvalue

def Cartan_matrix(Delta, symbolic=False):
    """
    Return the Cartan matrix for a simple system
    
    INPUT:
    
    - ``Delta`` -- list of vectors or any iterable that can be turned into a vector
    - 

    EXAMPLES::

        sage: Delta = ((1, 0, 0)), ((0, 1, 0)), ((0, 0, 1))
        sage: C = Cartan_matrix(Delta)
        sage: C
        [2 0 0]
        [0 2 0]
        [0 0 2]
    """
    Delta=[vector(v) for v in Delta]

    M = matrix([[2 / w.dot_product(w) * v.dot_product(w) for w in Delta] for v in Delta])
    
    if symbolic:
        M = M.apply_map(expand)
        
    return M
~~~
{: .source .python}


~~~
Delta = ((0, 1, 0)), ((-1/4*(1+sqrt(5)), -1/2, 1/4*(1-sqrt(5)))), ((1, 0, 0))

Delta

C = Cartan_matrix(Delta, symbolic=True)
C
~~~
{: .source .python}



~~~
[                 2                 -1                  0]
[                -1                  2 -1/2*sqrt(5) - 1/2]
[                 0 -1/2*sqrt(5) - 1/2                  2]
~~~
{: .output}




~~~
E = C.eigenvectors_right()
E

  
A=QQbar(E[1][1][0][2])
A
E
~~~
{: .source .python}



~~~
[(-1/2*sqrt(2*sqrt(5) + 10) + 2,
  [(1, 1/2*sqrt(2*sqrt(5) + 10), 1/2*sqrt(5) + 1/2)],
  1),
 (1/2*sqrt(2*sqrt(5) + 10) + 2,
  [(1, -1/2*sqrt(2*sqrt(5) + 10), 1/2*sqrt(5) + 1/2)],
  1),
 (2, [(1, 0, -1/2*sqrt(5) + 1/2)], 1)]
~~~
{: .output}




~~~
# find PF eigenvector i.e. all coefficients of the same sign
for i in range(3):
    tmp = E[i][1][0]
    if all (x * tmp[0] > 0 for x in tmp):
        print(tmp)
 
~~~
{: .source .python}

~~~
(1, 1/2*sqrt(2*sqrt(5) + 10), 1/2*sqrt(5) + 1/2)

~~~
{: .output}


~~~
# find duals to roots (weights), construct two vectors from two-colouring of the graph and the PF evec just found; orthonormalise and project root system into this plane

~~~
{: .source .python}
