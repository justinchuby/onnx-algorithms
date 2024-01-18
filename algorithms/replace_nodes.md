# Replace a set of nodes

In the following example, we want to replace the subgraph in orange that produces an input to `n4`
with a subgraph in blue, only for the node `n4`. One idea would be to
take the subgraph that is bounded by `v1`, `v2` and `v3` and replace it with the subgraph on the left
(in blue), but it would be inccorect because `v3` is used by other nodes (in gray).

Instead, we connect the new graph and use `v1`, `v2` as inputs, and replace the input to `n4` (`v3`) to `v_new`.

![image](https://github.com/justinchuby/onnx-algorithms/assets/11205048/f68eceb3-788a-48a8-9081-195de966d2d3)
