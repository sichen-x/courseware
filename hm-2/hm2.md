# Data structures and big O

## 1 Graph

Implement class Node and class Graph in a file named graph.py. Implement a directed un-weighted in your Graph class.

Note, a path is represented as a list of nodes in order such as path from `Node A` to `Node C` via `Node C`.

is represented as a list with `Node`s:

```
[Node({'A',['B']}), Node({'B',['C','D']}), Node({'C',['E','F']})]
```

Note, that the `{'A',['B']}` is used to exemplify, in the program it would be represented as ``[Node 1, Node 2, Node 3]``.

**All functions operate on and return** `Node` object, a list of `Nodes`, or `self`. The two exceptions are `__str__` and `print_path` methods that return specified string representation of `Node` object.


Description of classes and required methods is bellow:

```
class Node:
  """
  class constructor should take one argument:
    dictionary with a name of the node as a key and a list of nodes it is connected to as value.
  For example
  >>>Node({'A':['B','C']})

  Note 1,
    that the node may not have any connections, thus empty list is a legal dictionary value.
  >>>Node({'A':[]})

  Note 2,
    any other input to the node should result in an error.
  """

  def ___str__(self):
    """
    returns string representation
    >>>{"node:[vertex, vertex]}
    """

class Graph:

  def __init__(.....):
    """
    The constructor accepts a list of valid nodes, if no list is given, the graph is instantiated empty.
    """

  def add(self, node):
    """
    adds the node to the graph
    """

  def delete(self, node):
    """
    deletes given node from the graph
    """

  def find_path_dfs(self, start_node, end):
    """
    return one path between start and end
    search is performed Depth-First
    """

  def find_path_bi(self, start_node, end_node):
    """
    return one path between start and end
    search is performed Bidirectional
    [Node 1, Node 2, Node 3]
    """

  def find_all_paths(self, start_node, end_node):
    """
    returns a list with all paths between start and end, the list is empty if no path is found. Use traversal method of your choice.
    """

  def find_shortest_path(self, start_node, end_node):
    """
    returns the shortest path between start and end, or None if no path was found.
    """

  def has_route(self, start_node, end_node):
    """
    design an algorithm to return True if there is at least one path between
    start_node and end_node, otherwise returns False
    """

  def print_path(self, path):
    """
    Given the path 'A' to 'B' to 'C', print the path in following format:
    'A'->'B'->'C'
    The node names have to come in order
    """
  def __str__(self):
    """
    returns a list representation with each node
    >>>[{'A':['B','C']},{'D':['B','C']},{'B':['C','E']}]
    """

```

Example of creating graph and nodes then adding them.


```
g = Graph()
node_1 = Node({'A':['B','C']})
g.add(node_1)
node_2 = Node({'B':['C','D']})
g.add(node_2)
node_3 = Node({'C':['D']})
g.add(node_3)
g.add( Node({'D':['C']}))
```


## 2 Write a test case that verifies the correctness of your implementation
This is actually good starting point! You must implement following test classes.

Note 1, you will need to manually construct graphs and node dictionaries for testing. One way to simplify is to make them module level and reuse in various tests.

NOTE 2: more clarification for testing implementation will be provided.

```
def test_empty_node:
  """
  tests creation of empty node
  """

def test_error_node:
    """
    tests creation of bad node
    Node({'a':'a'})
    have to pass since the test is written to test error
    """

def test_good_node:
    """
    tests creation of bad node
    Node({'A':['B','C']})
    """

def test_node_str:
  """
  test that node representation of string is
  "{'name':['list','of','vertex']}"
  """

def test_empty_graph:
  """
  tests creation of empty graph
  """

def test_graph_with_list:
  """
  tests creation of the graph with a list of nodes
  node_list = []
  node_list.append(Node({'A':['B','C']}))
  node_list.append(Node({'B':['C','D']}))
  node_list.append(Node({'C':['D']}))
  node_list.append(Node({'D':['C']}))
  Graph(node_list)
  """

def test_graph_with_list_fail:
  """
  tests creation of the graph with a list
  node_list = ["slippery list"]
  node_list.append(Node({'A':"['B','C']"}))
  node_list.append(Node({'B':['C','D']}))
  node_list.append(Node({'C':['D']}))
  node_list.append(Node({'D':['C']}))
  Graph(node_list)
  error should be raised
  """  

def test_add_to_graph:
  """
  create graph and add nodes in a loop
  """

def test_graph_str:
  """
  test string representation of the graphs
  should be
  "[{'A':"['B','C']"}, {'B':['C','D']}, {'C':['D']}]"
  """

def test_find_path_dfs:
  """
  you should test with graphs that have 0, 1, 3 paths
  """

def test_find_path_bi:
  """
  you should test with graphs that have 0, 1, 3 paths
  """

 def test_find_all_paths:
  """
  you should test with graphs that have 0, 1, 3 paths
  """

def test_find_shortest_path:
  """
  you should test with graphs that have 0, 1, 3 paths
  """

def test_has_route:
  """
  you should test with graphs that have 0, 1, 3 paths
  """

```

The test should run each of the functions and produce result output. To run the test it has to be sufficient to call it in command line as:

```
PYTHONPATH=. python -m pytest -v test_graph.py
```

## 3 Big O
Write a script that produces a single plot file named big_o.png with the following functions

* O(1)
* O(log n)
* O(n log n )
* O(n)
* O(n^2)
* O(2^n)

The last two functions should be plotted in logarithmic scale.


# Deliverables
1) file graph.py with the implementation of Graph and Node classes, file test_graph.py with the test implementation  
2) test_graph.py containing test implementations from 2.
3) script for plotting and plot itself in png format representing solution to 3

# How to submit

Use the invitation link bellow to create the repo:
https://classroom.github.com/a/QzX979hN
