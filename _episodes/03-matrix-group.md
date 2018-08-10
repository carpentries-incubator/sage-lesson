---
title: Elements of programming and 3D graphics
teaching: 30
exercises: 0
questions:
- "..."
objectives:
- "..."
---
The following is a list of points in 3D, that we wish to plot - they are actually the vertices of an icosahedron, $\tau$ is the golden ratio we had above $1/2(1+\sqrt{5})$

#TODO: question - could go to Hamiltonian cycles now?


~~~
tau = 1.619

icos_vertex_list = [[1,0,tau], [-1,0,tau], [1,0,-tau], [-1,0,-tau], [0, tau, 1], [0, tau, -1], [0, -tau, 1], [0, -tau, -1], [tau, 1, 0], [tau, -1, 0], [-tau, 1, 0], [-tau, -1, 0]]

point3d(icos_vertex_list, size=50)
~~~
{: .source .python}




<iframe srcdoc="
<html>
<head>
  <style>
    * {
      margin: 0;
      padding: 0;
      overflow: hidden;
    }
    body, html {      
      height: 100%;
      width: 100%;
    }
  </style>
  <script type=&quot;text/javascript&quot; src=&quot;/nbextensions/jsmol/JSmol.min.js&quot;></script>
</head>
<body>
  <script type=&quot;text/javascript&quot;>
    var script = [
  'data &quot;model list&quot;',
  '10',
  'empty',
  'Xx -3.0 -4.0 -3.0',
  'Xx 0.0 -4.0 -3.0',
  'Xx 3.0 -4.0 -3.0',
  'Xx 4.0 -3.0 -3.0',
  'Xx 4.0 0.0 -3.0',
  'Xx 4.0 3.0 -3.0',
  'Xx -4.0 -3.0 -3.0',
  'Xx -4.0 -3.0 0.0',
  'Xx -4.0 -3.0 3.0',
  'Xx 5.5 5.5 5.5',
  'end &quot;model list&quot;; show data',
  'select *',
  'wireframe off; spacefill off',
  'set labelOffset 0 0',
  'background [255,255,255]',
  'spin OFF',
  'moveto 0 -764 -346 -545 76.39',
  'centerAt absolute {0 0 0}',
  'zoom 100',
  'frank OFF',
  'set perspectivedepth ON',
  'draw point_1 DIAMETER 50 {1.85299567634 0.0 3.0}',
  'color $point_1  [102,102,255]',
  'draw point_2 DIAMETER 50 {-1.85299567634 0.0 3.0}',
  'color $point_2  [102,102,255]',
  'draw point_3 DIAMETER 50 {1.85299567634 0.0 -3.0}',
  'color $point_3  [102,102,255]',
  'draw point_4 DIAMETER 50 {-1.85299567634 0.0 -3.0}',
  'color $point_4  [102,102,255]',
  'draw point_5 DIAMETER 50 {0.0 3.0 1.85299567634}',
  'color $point_5  [102,102,255]',
  'draw point_6 DIAMETER 50 {0.0 3.0 -1.85299567634}',
  'color $point_6  [102,102,255]',
  'draw point_7 DIAMETER 50 {0.0 -3.0 1.85299567634}',
  'color $point_7  [102,102,255]',
  'draw point_8 DIAMETER 50 {0.0 -3.0 -1.85299567634}',
  'color $point_8  [102,102,255]',
  'draw point_9 DIAMETER 50 {3.0 1.85299567634 0.0}',
  'color $point_9  [102,102,255]',
  'draw point_10 DIAMETER 50 {3.0 -1.85299567634 0.0}',
  'color $point_10  [102,102,255]',
  'draw point_11 DIAMETER 50 {-3.0 1.85299567634 0.0}',
  'color $point_11  [102,102,255]',
  'draw point_12 DIAMETER 50 {-3.0 -1.85299567634 0.0}',
  'color $point_12  [102,102,255]',
  'draw line_13 diameter 1 curve {-3.0 -3.0 -3.0}  {-3.0 3.0 -3.0} ',
  'color $line_13 translucent 0.5 [0,0,0]',
  'draw line_14 diameter 1 curve {-3.0 3.0 -3.0}  {3.0 3.0 -3.0} ',
  'color $line_14 translucent 0.5 [0,0,0]',
  'draw line_15 diameter 1 curve {3.0 3.0 -3.0}  {3.0 -3.0 -3.0} ',
  'color $line_15 translucent 0.5 [0,0,0]',
  'draw line_16 diameter 1 curve {3.0 -3.0 -3.0}  {-3.0 -3.0 -3.0} ',
  'color $line_16 translucent 0.5 [0,0,0]',
  'draw line_17 diameter 1 curve {-3.0 -3.0 -3.0}  {-3.0 -3.0 3.0} ',
  'color $line_17 translucent 0.5 [0,0,0]',
  'draw line_18 diameter 1 curve {-3.0 -3.0 3.0}  {-3.0 3.0 3.0} ',
  'color $line_18 translucent 0.5 [0,0,0]',
  'draw line_19 diameter 1 curve {-3.0 3.0 3.0}  {3.0 3.0 3.0} ',
  'color $line_19 translucent 0.5 [0,0,0]',
  'draw line_20 diameter 1 curve {3.0 3.0 3.0}  {3.0 -3.0 3.0} ',
  'color $line_20 translucent 0.5 [0,0,0]',
  'draw line_21 diameter 1 curve {3.0 -3.0 3.0}  {-3.0 -3.0 3.0} ',
  'color $line_21 translucent 0.5 [0,0,0]',
  'draw line_22 diameter 1 curve {-3.0 -3.0 3.0} ',
  'color $line_22 translucent 0.5 [0,0,0]',
  'draw line_23 diameter 1 curve {-3.0 3.0 -3.0}  {-3.0 3.0 3.0} ',
  'color $line_23 translucent 0.5 [0,0,0]',
  'draw line_24 diameter 1 curve {3.0 -3.0 -3.0}  {3.0 -3.0 3.0} ',
  'color $line_24 translucent 0.5 [0,0,0]',
  'draw line_25 diameter 1 curve {3.0 3.0 -3.0}  {3.0 3.0 3.0} ',
  'color $line_25 translucent 0.5 [0,0,0]',
  'select atomno = 1',
  'color atom  [76,76,76]',
  'label &quot;-1.6&quot;',
  'select atomno = 2',
  'color atom  [76,76,76]',
  'label &quot;0.0&quot;',
  'select atomno = 3',
  'color atom  [76,76,76]',
  'label &quot;1.6&quot;',
  'select atomno = 4',
  'color atom  [76,76,76]',
  'label &quot;-1.6&quot;',
  'select atomno = 5',
  'color atom  [76,76,76]',
  'label &quot;0.0&quot;',
  'select atomno = 6',
  'color atom  [76,76,76]',
  'label &quot;1.6&quot;',
  'select atomno = 7',
  'color atom  [76,76,76]',
  'label &quot;-1.6&quot;',
  'select atomno = 8',
  'color atom  [76,76,76]',
  'label &quot;0.0&quot;',
  'select atomno = 9',
  'color atom  [76,76,76]',
  'label &quot;1.6&quot;',
  'isosurface fullylit; pmesh o* fullylit; set antialiasdisplay on;',
].join('\n');;
    var Info = {
      width: '100%',
      height: '500',
      debug: false,
      disableInitialConsole: true,   // very slow when used with inline mesh
      color: '#3131ff',
      addSelectionOptions: false,
      use: 'HTML5',
      j2sPath: '/nbextensions/jsmol/j2s',
      script: script,
    };
    var jmolApplet0 = Jmol.getApplet('jmolApplet0', Info);
  </script>
</body>
</html>
" 
        width="100%"
        height="500"
        style="border: 0;">
</iframe>



For next step you need to use some programming language, as doing this interactively is not productive. First we need to introduce some notions, namely ranges, loops and conditional statements.


~~~
for n in range(1,6):
    print(n)
~~~
{: .source .python}

~~~
1
2
3
4
5

~~~
{: .output}
We now do a double loop over two variables with a non-trivial 'function'. This gives the 'allowed' triangulation numbers in Caspar-Klug theory. Note that we define this as a set, so that the order does not matter and duplicates do not occur. 


~~~
l=set([])
for h in range(0,6):
    for k in range(0,6):
        l.add(h^2+h*k+k^2)
l
~~~
{: .source .python}



~~~
{0, 1, 3, 4, 7, 9, 12, 13, 16, 19, 21, 25, 27, 28, 31, 37, 39, 48, 49, 61, 75}
~~~
{: .output}


Now let us loop over a larger range, and combine this with an if statement. We are generating large numbers of 'allowed' triangulation numbers. But say, we are only interested in finding potential $(h,k)$ pairs that give rise to the largest known triangulation in a virus, which for now (2018) is $499$ for Cafeteria roenbergensis virus (https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5511168/). 


~~~
for h in range(0,20):
    for k in range(h,20):
        t = h^2+h*k+k^2
        if t == 499:
            print(h, k)
~~~
{: .source .python}

~~~
(7, 18)

~~~
{: .output}
So there is a unique pair (up to chirality).

In the following example, we check that there is only one unordered 5-tuple of nonegative integers such that one of these integers is 1, and the sum of their squares is 60 (those familiar with group theory will recognise that this gives the dimensions of irreducible representations of the icosahedral group). This also uses a couple of nested for loops combined with  an if statement to show the uniquess of the solution 'by brute force'/enumeration. 


~~~
order = 60

for i1 in range(1,8):
    for i2 in range(i1,8):
        for i3 in range(i2,8):
             for i4 in range(i3,8):
                    if (1^2+i1^2+i2^2+i3^2+i4^2==order):
                        print(1, i1, i2, i3, i4)
~~~
{: .source .python}

~~~
(1, 3, 3, 4, 5)

~~~
{: .output}
Find the adjacencies of vertices. Which distances occur?


~~~
for i in range(0,1):
    for j in range(0,12):
        print(round(norm(vector(icos_vertex_list[i])-vector(icos_vertex_list[j])),2))
~~~
{: .source .python}

~~~
0.0
2.0
3.24
3.81
2.0
3.24
2.0
3.24
2.0
2.0
3.24
3.24

~~~
{: .output}
Find all those with distance (squared) 2


~~~
adj=[]
for i in range(0,len(icos_vertex_list)):
    adj.append([])
    for j in range(0,12):
        if round(norm(vector(icos_vertex_list[i])-vector(icos_vertex_list[j])),2)==2.00:
            adj[i].append(j)
    print(adj[i])
~~~
{: .source .python}

~~~
[1, 4, 6, 8, 9]
[0, 4, 6, 10, 11]
[3, 5, 7, 8, 9]
[2, 5, 7, 10, 11]
[0, 1, 5, 8, 10]
[2, 3, 4, 8, 10]
[0, 1, 7, 9, 11]
[2, 3, 6, 9, 11]
[0, 2, 4, 5, 9]
[0, 2, 6, 7, 8]
[1, 3, 4, 5, 11]
[1, 3, 6, 7, 10]

~~~
{: .output}
Getting the list of edges


~~~
icos_edges = []
for i in range(0,len(adj)):
    for j in range(0,len(adj[i])):
        icos_edges.append( line3d( [icos_vertex_list[i], icos_vertex_list[adj[i][j]]], thickness=10) )
~~~
{: .source .python}


~~~
vertices = point3d(icos_vertex_list, size=100)
icosahedron = vertices
for edge in icos_edges:
    icosahedron = icosahedron + edge
~~~
{: .source .python}


~~~
show(icosahedron)
~~~
{: .source .python}



<iframe srcdoc="
<html>
<head>
  <style>
    * {
      margin: 0;
      padding: 0;
      overflow: hidden;
    }
    body, html {      
      height: 100%;
      width: 100%;
    }
  </style>
  <script type=&quot;text/javascript&quot; src=&quot;/nbextensions/jsmol/JSmol.min.js&quot;></script>
</head>
<body>
  <script type=&quot;text/javascript&quot;>
    var script = [
  'data &quot;model list&quot;',
  '10',
  'empty',
  'Xx -3.0 -4.0 -3.0',
  'Xx 0.0 -4.0 -3.0',
  'Xx 3.0 -4.0 -3.0',
  'Xx 4.0 -3.0 -3.0',
  'Xx 4.0 0.0 -3.0',
  'Xx 4.0 3.0 -3.0',
  'Xx -4.0 -3.0 -3.0',
  'Xx -4.0 -3.0 0.0',
  'Xx -4.0 -3.0 3.0',
  'Xx 5.5 5.5 5.5',
  'end &quot;model list&quot;; show data',
  'select *',
  'wireframe off; spacefill off',
  'set labelOffset 0 0',
  'background [255,255,255]',
  'spin OFF',
  'moveto 0 -764 -346 -545 76.39',
  'centerAt absolute {0 0 0}',
  'zoom 100',
  'frank OFF',
  'set perspectivedepth ON',
  'draw point_1 DIAMETER 100 {1.85299567634 0.0 3.0}',
  'color $point_1  [102,102,255]',
  'draw point_2 DIAMETER 100 {-1.85299567634 0.0 3.0}',
  'color $point_2  [102,102,255]',
  'draw point_3 DIAMETER 100 {1.85299567634 0.0 -3.0}',
  'color $point_3  [102,102,255]',
  'draw point_4 DIAMETER 100 {-1.85299567634 0.0 -3.0}',
  'color $point_4  [102,102,255]',
  'draw point_5 DIAMETER 100 {0.0 3.0 1.85299567634}',
  'color $point_5  [102,102,255]',
  'draw point_6 DIAMETER 100 {0.0 3.0 -1.85299567634}',
  'color $point_6  [102,102,255]',
  'draw point_7 DIAMETER 100 {0.0 -3.0 1.85299567634}',
  'color $point_7  [102,102,255]',
  'draw point_8 DIAMETER 100 {0.0 -3.0 -1.85299567634}',
  'color $point_8  [102,102,255]',
  'draw point_9 DIAMETER 100 {3.0 1.85299567634 0.0}',
  'color $point_9  [102,102,255]',
  'draw point_10 DIAMETER 100 {3.0 -1.85299567634 0.0}',
  'color $point_10  [102,102,255]',
  'draw point_11 DIAMETER 100 {-3.0 1.85299567634 0.0}',
  'color $point_11  [102,102,255]',
  'draw point_12 DIAMETER 100 {-3.0 -1.85299567634 0.0}',
  'color $point_12  [102,102,255]',
  'draw line_13 diameter 10 curve {1.85299567634 0.0 3.0}  {-1.85299567634 0.0 3.0} ',
  'color $line_13  [102,102,255]',
  'draw line_14 diameter 10 curve {1.85299567634 0.0 3.0}  {0.0 3.0 1.85299567634} ',
  'color $line_14  [102,102,255]',
  'draw line_15 diameter 10 curve {1.85299567634 0.0 3.0}  {0.0 -3.0 1.85299567634} ',
  'color $line_15  [102,102,255]',
  'draw line_16 diameter 10 curve {1.85299567634 0.0 3.0}  {3.0 1.85299567634 0.0} ',
  'color $line_16  [102,102,255]',
  'draw line_17 diameter 10 curve {1.85299567634 0.0 3.0}  {3.0 -1.85299567634 0.0} ',
  'color $line_17  [102,102,255]',
  'draw line_18 diameter 10 curve {-1.85299567634 0.0 3.0}  {1.85299567634 0.0 3.0} ',
  'color $line_18  [102,102,255]',
  'draw line_19 diameter 10 curve {-1.85299567634 0.0 3.0}  {0.0 3.0 1.85299567634} ',
  'color $line_19  [102,102,255]',
  'draw line_20 diameter 10 curve {-1.85299567634 0.0 3.0}  {0.0 -3.0 1.85299567634} ',
  'color $line_20  [102,102,255]',
  'draw line_21 diameter 10 curve {-1.85299567634 0.0 3.0}  {-3.0 1.85299567634 0.0} ',
  'color $line_21  [102,102,255]',
  'draw line_22 diameter 10 curve {-1.85299567634 0.0 3.0}  {-3.0 -1.85299567634 0.0} ',
  'color $line_22  [102,102,255]',
  'draw line_23 diameter 10 curve {1.85299567634 0.0 -3.0}  {-1.85299567634 0.0 -3.0} ',
  'color $line_23  [102,102,255]',
  'draw line_24 diameter 10 curve {1.85299567634 0.0 -3.0}  {0.0 3.0 -1.85299567634} ',
  'color $line_24  [102,102,255]',
  'draw line_25 diameter 10 curve {1.85299567634 0.0 -3.0}  {0.0 -3.0 -1.85299567634} ',
  'color $line_25  [102,102,255]',
  'draw line_26 diameter 10 curve {1.85299567634 0.0 -3.0}  {3.0 1.85299567634 0.0} ',
  'color $line_26  [102,102,255]',
  'draw line_27 diameter 10 curve {1.85299567634 0.0 -3.0}  {3.0 -1.85299567634 0.0} ',
  'color $line_27  [102,102,255]',
  'draw line_28 diameter 10 curve {-1.85299567634 0.0 -3.0}  {1.85299567634 0.0 -3.0} ',
  'color $line_28  [102,102,255]',
  'draw line_29 diameter 10 curve {-1.85299567634 0.0 -3.0}  {0.0 3.0 -1.85299567634} ',
  'color $line_29  [102,102,255]',
  'draw line_30 diameter 10 curve {-1.85299567634 0.0 -3.0}  {0.0 -3.0 -1.85299567634} ',
  'color $line_30  [102,102,255]',
  'draw line_31 diameter 10 curve {-1.85299567634 0.0 -3.0}  {-3.0 1.85299567634 0.0} ',
  'color $line_31  [102,102,255]',
  'draw line_32 diameter 10 curve {-1.85299567634 0.0 -3.0}  {-3.0 -1.85299567634 0.0} ',
  'color $line_32  [102,102,255]',
  'draw line_33 diameter 10 curve {0.0 3.0 1.85299567634}  {1.85299567634 0.0 3.0} ',
  'color $line_33  [102,102,255]',
  'draw line_34 diameter 10 curve {0.0 3.0 1.85299567634}  {-1.85299567634 0.0 3.0} ',
  'color $line_34  [102,102,255]',
  'draw line_35 diameter 10 curve {0.0 3.0 1.85299567634}  {0.0 3.0 -1.85299567634} ',
  'color $line_35  [102,102,255]',
  'draw line_36 diameter 10 curve {0.0 3.0 1.85299567634}  {3.0 1.85299567634 0.0} ',
  'color $line_36  [102,102,255]',
  'draw line_37 diameter 10 curve {0.0 3.0 1.85299567634}  {-3.0 1.85299567634 0.0} ',
  'color $line_37  [102,102,255]',
  'draw line_38 diameter 10 curve {0.0 3.0 -1.85299567634}  {1.85299567634 0.0 -3.0} ',
  'color $line_38  [102,102,255]',
  'draw line_39 diameter 10 curve {0.0 3.0 -1.85299567634}  {-1.85299567634 0.0 -3.0} ',
  'color $line_39  [102,102,255]',
  'draw line_40 diameter 10 curve {0.0 3.0 -1.85299567634}  {0.0 3.0 1.85299567634} ',
  'color $line_40  [102,102,255]',
  'draw line_41 diameter 10 curve {0.0 3.0 -1.85299567634}  {3.0 1.85299567634 0.0} ',
  'color $line_41  [102,102,255]',
  'draw line_42 diameter 10 curve {0.0 3.0 -1.85299567634}  {-3.0 1.85299567634 0.0} ',
  'color $line_42  [102,102,255]',
  'draw line_43 diameter 10 curve {0.0 -3.0 1.85299567634}  {1.85299567634 0.0 3.0} ',
  'color $line_43  [102,102,255]',
  'draw line_44 diameter 10 curve {0.0 -3.0 1.85299567634}  {-1.85299567634 0.0 3.0} ',
  'color $line_44  [102,102,255]',
  'draw line_45 diameter 10 curve {0.0 -3.0 1.85299567634}  {0.0 -3.0 -1.85299567634} ',
  'color $line_45  [102,102,255]',
  'draw line_46 diameter 10 curve {0.0 -3.0 1.85299567634}  {3.0 -1.85299567634 0.0} ',
  'color $line_46  [102,102,255]',
  'draw line_47 diameter 10 curve {0.0 -3.0 1.85299567634}  {-3.0 -1.85299567634 0.0} ',
  'color $line_47  [102,102,255]',
  'draw line_48 diameter 10 curve {0.0 -3.0 -1.85299567634}  {1.85299567634 0.0 -3.0} ',
  'color $line_48  [102,102,255]',
  'draw line_49 diameter 10 curve {0.0 -3.0 -1.85299567634}  {-1.85299567634 0.0 -3.0} ',
  'color $line_49  [102,102,255]',
  'draw line_50 diameter 10 curve {0.0 -3.0 -1.85299567634}  {0.0 -3.0 1.85299567634} ',
  'color $line_50  [102,102,255]',
  'draw line_51 diameter 10 curve {0.0 -3.0 -1.85299567634}  {3.0 -1.85299567634 0.0} ',
  'color $line_51  [102,102,255]',
  'draw line_52 diameter 10 curve {0.0 -3.0 -1.85299567634}  {-3.0 -1.85299567634 0.0} ',
  'color $line_52  [102,102,255]',
  'draw line_53 diameter 10 curve {3.0 1.85299567634 0.0}  {1.85299567634 0.0 3.0} ',
  'color $line_53  [102,102,255]',
  'draw line_54 diameter 10 curve {3.0 1.85299567634 0.0}  {1.85299567634 0.0 -3.0} ',
  'color $line_54  [102,102,255]',
  'draw line_55 diameter 10 curve {3.0 1.85299567634 0.0}  {0.0 3.0 1.85299567634} ',
  'color $line_55  [102,102,255]',
  'draw line_56 diameter 10 curve {3.0 1.85299567634 0.0}  {0.0 3.0 -1.85299567634} ',
  'color $line_56  [102,102,255]',
  'draw line_57 diameter 10 curve {3.0 1.85299567634 0.0}  {3.0 -1.85299567634 0.0} ',
  'color $line_57  [102,102,255]',
  'draw line_58 diameter 10 curve {3.0 -1.85299567634 0.0}  {1.85299567634 0.0 3.0} ',
  'color $line_58  [102,102,255]',
  'draw line_59 diameter 10 curve {3.0 -1.85299567634 0.0}  {1.85299567634 0.0 -3.0} ',
  'color $line_59  [102,102,255]',
  'draw line_60 diameter 10 curve {3.0 -1.85299567634 0.0}  {0.0 -3.0 1.85299567634} ',
  'color $line_60  [102,102,255]',
  'draw line_61 diameter 10 curve {3.0 -1.85299567634 0.0}  {0.0 -3.0 -1.85299567634} ',
  'color $line_61  [102,102,255]',
  'draw line_62 diameter 10 curve {3.0 -1.85299567634 0.0}  {3.0 1.85299567634 0.0} ',
  'color $line_62  [102,102,255]',
  'draw line_63 diameter 10 curve {-3.0 1.85299567634 0.0}  {-1.85299567634 0.0 3.0} ',
  'color $line_63  [102,102,255]',
  'draw line_64 diameter 10 curve {-3.0 1.85299567634 0.0}  {-1.85299567634 0.0 -3.0} ',
  'color $line_64  [102,102,255]',
  'draw line_65 diameter 10 curve {-3.0 1.85299567634 0.0}  {0.0 3.0 1.85299567634} ',
  'color $line_65  [102,102,255]',
  'draw line_66 diameter 10 curve {-3.0 1.85299567634 0.0}  {0.0 3.0 -1.85299567634} ',
  'color $line_66  [102,102,255]',
  'draw line_67 diameter 10 curve {-3.0 1.85299567634 0.0}  {-3.0 -1.85299567634 0.0} ',
  'color $line_67  [102,102,255]',
  'draw line_68 diameter 10 curve {-3.0 -1.85299567634 0.0}  {-1.85299567634 0.0 3.0} ',
  'color $line_68  [102,102,255]',
  'draw line_69 diameter 10 curve {-3.0 -1.85299567634 0.0}  {-1.85299567634 0.0 -3.0} ',
  'color $line_69  [102,102,255]',
  'draw line_70 diameter 10 curve {-3.0 -1.85299567634 0.0}  {0.0 -3.0 1.85299567634} ',
  'color $line_70  [102,102,255]',
  'draw line_71 diameter 10 curve {-3.0 -1.85299567634 0.0}  {0.0 -3.0 -1.85299567634} ',
  'color $line_71  [102,102,255]',
  'draw line_72 diameter 10 curve {-3.0 -1.85299567634 0.0}  {-3.0 1.85299567634 0.0} ',
  'color $line_72  [102,102,255]',
  'draw line_73 diameter 1 curve {-3.0 -3.0 -3.0}  {-3.0 3.0 -3.0} ',
  'color $line_73 translucent 0.5 [0,0,0]',
  'draw line_74 diameter 1 curve {-3.0 3.0 -3.0}  {3.0 3.0 -3.0} ',
  'color $line_74 translucent 0.5 [0,0,0]',
  'draw line_75 diameter 1 curve {3.0 3.0 -3.0}  {3.0 -3.0 -3.0} ',
  'color $line_75 translucent 0.5 [0,0,0]',
  'draw line_76 diameter 1 curve {3.0 -3.0 -3.0}  {-3.0 -3.0 -3.0} ',
  'color $line_76 translucent 0.5 [0,0,0]',
  'draw line_77 diameter 1 curve {-3.0 -3.0 -3.0}  {-3.0 -3.0 3.0} ',
  'color $line_77 translucent 0.5 [0,0,0]',
  'draw line_78 diameter 1 curve {-3.0 -3.0 3.0}  {-3.0 3.0 3.0} ',
  'color $line_78 translucent 0.5 [0,0,0]',
  'draw line_79 diameter 1 curve {-3.0 3.0 3.0}  {3.0 3.0 3.0} ',
  'color $line_79 translucent 0.5 [0,0,0]',
  'draw line_80 diameter 1 curve {3.0 3.0 3.0}  {3.0 -3.0 3.0} ',
  'color $line_80 translucent 0.5 [0,0,0]',
  'draw line_81 diameter 1 curve {3.0 -3.0 3.0}  {-3.0 -3.0 3.0} ',
  'color $line_81 translucent 0.5 [0,0,0]',
  'draw line_82 diameter 1 curve {-3.0 -3.0 3.0} ',
  'color $line_82 translucent 0.5 [0,0,0]',
  'draw line_83 diameter 1 curve {-3.0 3.0 -3.0}  {-3.0 3.0 3.0} ',
  'color $line_83 translucent 0.5 [0,0,0]',
  'draw line_84 diameter 1 curve {3.0 -3.0 -3.0}  {3.0 -3.0 3.0} ',
  'color $line_84 translucent 0.5 [0,0,0]',
  'draw line_85 diameter 1 curve {3.0 3.0 -3.0}  {3.0 3.0 3.0} ',
  'color $line_85 translucent 0.5 [0,0,0]',
  'select atomno = 1',
  'color atom  [76,76,76]',
  'label &quot;-1.6&quot;',
  'select atomno = 2',
  'color atom  [76,76,76]',
  'label &quot;0.0&quot;',
  'select atomno = 3',
  'color atom  [76,76,76]',
  'label &quot;1.6&quot;',
  'select atomno = 4',
  'color atom  [76,76,76]',
  'label &quot;-1.6&quot;',
  'select atomno = 5',
  'color atom  [76,76,76]',
  'label &quot;0.0&quot;',
  'select atomno = 6',
  'color atom  [76,76,76]',
  'label &quot;1.6&quot;',
  'select atomno = 7',
  'color atom  [76,76,76]',
  'label &quot;-1.6&quot;',
  'select atomno = 8',
  'color atom  [76,76,76]',
  'label &quot;0.0&quot;',
  'select atomno = 9',
  'color atom  [76,76,76]',
  'label &quot;1.6&quot;',
  'isosurface fullylit; pmesh o* fullylit; set antialiasdisplay on;',
].join('\n');;
    var Info = {
      width: '100%',
      height: '500',
      debug: false,
      disableInitialConsole: true,   // very slow when used with inline mesh
      color: '#3131ff',
      addSelectionOptions: false,
      use: 'HTML5',
      j2sPath: '/nbextensions/jsmol/j2s',
      script: script,
    };
    var jmolApplet0 = Jmol.getApplet('jmolApplet0', Info);
  </script>
</body>
</html>
" 
        width="100%"
        height="500"
        style="border: 0;">
</iframe>


