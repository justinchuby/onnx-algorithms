# Fold constants

(1) Mark constant foldable nodes

```
For all nodes in graph:
    if (node is Constant) or (parent of node is foldable) or (node is Shape and parent shape is known) or (node is {Shape -> Size} and parent rank is known) or (node is Size and parent shape is known):
        Mark node as "foldable"
```

(2) Fold all foldable subgraphs

```
For all graph in connected foldable subgraphs:
    Evaluate the expression
    Replace the subgraph with the result of the evaluation as a Constant node
```
