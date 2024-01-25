# A Note about Creating Cobweb Plots in Mathematica 13.1

There is another logistic plot called "CobwebPlot". It plots the phase space trajectory of a specific function combined with the graph of the function itself. However, the "CobwebPlot" requires online repository support. A simple demo is shown below :

```
=CobwebPlot[x |-> 3 Sin[x], 2, 10, {0, Pi}]
```

If someone want to make the plot interactive, see the code example below:

```
Manipulate[
=CobwebPlot[x |-> x/2 + (x/2 + 1/4) (1 - Cos[\[Pi] x]), n, m, {0, 20}, Frame -> True, Axes -> True, Epilog -> {Text[n, {n, -1/2}], Yellow, Opacity[0.5], Rectangle[{1, 1}]}], {{n, 7}, 1, 20, 1}, {{m, 5}, 1, 20, 1}
]
```

