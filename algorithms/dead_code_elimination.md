Remove nodes whose output values are unused.

1. Find unused nodes

```
For all nodes:
    If the node is a leaf node and its output values are not outputs of the model:
        Mark as "unused"
    If the node is not a leaf node and all its outputs are connected to unused nodes:
        Mark as "unused"
```

2. Remove unused nodes

```
Remove all nodes marked as "unused"
```

NOTE: But this is exactly the same idea as "remove one". Can we do better?
