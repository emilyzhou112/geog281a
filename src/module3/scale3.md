# __Scope and the Science of Scaling__

We’ve talked a lot about scale and emphasized how important it is to recognize that it is a critical decision in spatial analysis. But sometimes recognizing this is not enough. A related, and more forward-looking perspective, is to acknowledge and embrace the concept of __scope__. As another pivot here, we will illustrate this with an example from landscape ecology by Frazier (2023). This is not to say that focusing on scale is useless, but rather to provide an alternative, more effective way of thinking when using scale as a metric. When simply choosing a scale is insufficient for answering a question, we should measure scale more carefully using scope, so that we can compare studies and actually build generalizable knowledge.

## __The Problem of Scaling in Landscape Ecology__

Scientists have long recognized that local experiments cannot be extrapolated directly to larger-scale questions. This is especially true in landscape ecology, where landscapes are patchy and heterogeneous. One solution is to advance the science of scaling to permit the prediction and inference of quantities measured at one scale to another. In fact, ecologists have engaged in multi-scale analyses for more than a century, and landscape ecologists have fully embraced this concept through research on the scale dependency of relationships, processes, and landscape metrics. We have also observed empirical evidence of scaling for certain landscape components, particularly spatial pattern metrics, with studies showing that some metrics scale predictably as measurement resolution changes. 

However, the tradeoff is that we do not know why these relationships occur, or whether they are driven by underlying processes or simply reflect the fractal nature of landscapes. More importantly, this approach often does not produce generalizable knowledge and makes replication difficult. __This is exactly the frustration that Openshaw reveals: results change dramatically with aggregation, but we lack a systematic way to compare or interpret those changes.__

## __Introducing Scope__

Frazier (2023) proposes that, at least in landscape ecology, advancing a science of scaling (and addressing the kinds of concerns highlighted by Openshaw) will benefit from acknowledging and embracing the concept of scope. While scale refers to the relative size or extent of something and has dimensions, __scope is a dimensionless ratio of the range (extent) to the resolution (grain)__. While grain and extent are each important on their own, their ratio is even more valuable for extending results into applications of scaling theory. It is this extent-to-grain ratio that provides insight into the robustness of a study.

From a physical standpoint, this ratio turns dimensional quantities into dimensionless ones so that values can be compared on a relative scale. From a practical standpoint, the extent-to-grain ratio determines which processes can be reflected in the results. For example, if the extent-to-grain ratio is too small, boundary effects may dominate, leading to questionable metric computations or truncated patterns. Many metrics are quite sensitive to scope, particularly those involving edge/perimeter measures or length-to-area relationships, and simply reporting scope can provide insight into the applicability of the findings. In this sense, __scope helps us understand why results change with scale, which is something Openshaw demonstrated empirically but did not fully formalize.__

Beyond this, scope also provides a key way to facilitate replication and assess the comparability of different experiments. Research is replicable if the same (or very similar) methods can be applied to new data and produce similar results. However, replication is often complicated by a lack of consistency in the scales at which multi-scale studies are undertaken, making meaningful comparisons difficult or even impossible. Studies conducted in different geographic areas may be more reliably compared if they operate at the same (or similar) scope. This also directly addresses the problem raised by Openshaw: __if different zoning systems produce different results, how do we know which results are comparable? Scope can probably provide one answer.__

## __Scope in Practice__

As an example, Frazier uses a set of forest maps from the United States and simplifies them into binary forest vs. non-forest maps. From these, they compute landscape metrics such as number of patches, shape of patches, and largest patch size. They then manipulate scale in two ways: by changing grain (resolution) and extent (study area), creating multiple combinations of “scale setups.” These combinations correspond to different scopes: for example, a large extent with fine grain produces a large scope, while a small extent with coarse grain produces a small scope. 

<div align="center">
    <img src="../../assets/scale-scope.png" alt="mapscale" width="700" height="700">
</div>

__Figure 1__: Scopes for three extents and five grains with letters indicating which extent-grain ratios are equal in scope. The
smallest/largest extent was not computed for the largest/smallest grain as there were no comparable scopes. Scope A is 111,111, B is 27,778, C is 6944, D is 1736, and E is 434. Ridgeline plots for b number of patches, c landscape shape index, d largest patch
index are colored according to scope. Plot colors match the scope colors in (a)

The key finding is that __results cluster by scope, not by grain or extent individually__. Metrics such as number of patches may vary widely across different scales, but become much more similar when the extent-to-grain ratio is the same. This leads to an important insight:

> It is not grain or extent individually that matters most, but their relationship. 

If we connect this back to Openshaw, we can reinterpret his findings in a new way. Openshaw shows that results change dramatically with aggregation. Frazier’s contribution is to suggest that there is actually structure within that instability that we just were not measuring it correctly. That structure is captured by scope.

Following this, several practical steps can help advance the science of scaling through scope: 

- __First__, researchers should set scope based on the phenomenon being studied, rather than relying solely on available data. 
- __Second__, studies should report both grain and extent quantitatively so that scope can be calculated and compared across studies. 
- __Third__, researchers should undertake comparisons and replications based on scope. Replications sit at the core of the scientific method, yet geography faces particular challenges due to spatial context and analytical choices. By comparing studies conducted at similar scopes, we can better assess whether findings are robust, comparable, and generalizable.