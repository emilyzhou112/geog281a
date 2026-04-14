# __The Openshaw Effect__

Understanding the influence of scale in actual geographical research is as important as understanding the concept of scale itself. To demonstrate this, we draw on an experiment conducted by Openshaw et al. in the 1970s that explores the modifiable areal unit problem (MAUP). 

## __The Modifiable Areal Unit Problem__

What is an intuitive way to think about MAUP? Since the area over which data is collected is continuous, there are many different ways it can be partitioned into areal units for analysis. In fact, there are theoretically infinite ways to divide a study area, even though data are typically reported using only one particular set of units. These units can also be aggregated into larger units in many alternative ways. This is the modifiable areal unit problem, identified by Yule and Kendall (1950), who emphasized that results depend on the choice of spatial units.

The MAUP consists of two interrelated problems:

- __Scale problem__: results change when data are aggregated into larger spatial units
- __Aggregation problem__: results change when the same number of units are grouped differently

Although scale differences are the most obvious manifestation, the aggregation problem is equally important: even when the number of zones stays the same, different ways of grouping the base units can lead to different results.

We can also distinguish between two types of spatial arrangements:

- __Zoning systems__: contiguous areas (what we typically use in spatial analysis)
- __Grouping systems__: non-contiguous areas

A zoning system can be seen as a special case of a grouping system with an added contiguity constraint. Since most spatial analyses rely on contiguous regions, we focus primarily on zoning systems, while using grouping systems for comparison.

## __Openshaw’s First Experiment__

In the 1970s, Openshaw et al. conducted a series of experiments to illustrate the significance of MAUP. The first experiment examines how correlation coefficients change under different areal aggregations using data from Iowa, USA.

The basic areal units are the ninety-nine counties of Iowa. For each unit, there are two measures, the dependent variable is the percentage vote for Republican candidates in the congressional election of 1968 and the independent variable is the percentage of population over sixty-years old recorded in the 1970 US census.  At the county level, the correlation between these variables is __0. 3466__ over the set of ninety-nine counties. This value is specific to this particular set of spatial units.

In the __first part__ of this experiment, Openshaw aggregates the 99 counties into six larger units in different ways where differences between these results and the original county-level correlation reflect the scale problem and differences across the alternative six-zone aggregations reflect the aggregation problem  The key finding is that correlations vary substantially depending on how the aggregation is done. The “official” aggregation (congressional districts) produces a lower correlation than the county-level value, while other aggregations produce higher correlations. This leads to an important (and slightly uncomfortable) implication: __If a researcher wants a higher correlation, they can often obtain one simply by choosing a different zoning system.__

<a href="../../assets/scale51.png" class="zoomable">
  <img src="../../assets/scale51.png" style="width: 100%;">
</a>

__Table 1__: Some effects on the correlation coefficient of different areal arrangements
of the lowa counties into six zones.

In the __second part__ of the experiment, Openshaw moves beyond a few selected aggregations and instead systematically explores the full range of possible outcomes. Using an automatic zoning algorithm, he generates many alternative ways of aggregating the Iowa counties into different numbers of zones or groups. This allows him to approximate the maximum and minimum possible correlation coefficients at each scale. The results show that at coarser scales, when counties are aggregated into a small number of zones, the correlation can vary across a very wide range, even spanning from strongly negative to strongly positive values. As the number of zones increases and the scale becomes finer, this range of possible correlations narrows.

<a href="../../assets/scale52.png" class="zoomable">
  <img src="../../assets/scale52.png" style="width: 100%;">
</a>

__Table 2__: Maximum and minimum values of the correlation coefficient.

At the same time, clear differences emerge between zoning systems (which enforce contiguity) and grouping systems (which do not). Zoning systems tend to produce distributions of correlation coefficients with less spread and less bias relative to the original county-level correlation. This pattern can be explained by the interaction between spatial autocorrelation in the data and the contiguity constraint imposed by zoning. Because nearby areas tend to be similar, grouping contiguous units preserves some of the underlying spatial structure, limiting how extreme the resulting correlations can become. Overall, this part of the experiment demonstrates that __while aggregation can produce a wide range of results, the extent of this variability depends on both the scale of aggregation and the spatial structure imposed by the aggregation scheme__. 

In the __third part__ of the experiment, Openshaw shifts the focus from correlation coefficients to a more fundamental question: how aggregation changes the underlying variation in the data. When smaller spatial units are aggregated into larger ones, some of the original variability is inevitably lost. This can be understood by decomposing total variation into within-zone and between-zone components. As aggregation occurs, the variation within zones is averaged out and effectively disappears, leaving only the variation between zones. As a result, the total observable variation decreases as the level of aggregation increases. This loss of variation provides an important mechanism through which aggregation affects statistical relationships, including correlation coefficients.

However, Openshaw goes further by showing that aggregation does not affect all variables equally. This leads to the concept of differential loss of variation, which refers to the fact that different variables may lose variation at different rates when aggregated. Because correlation depends on the relative variation of the variables involved, unequal losses of variation can lead to changes in correlation that are difficult to predict. For instance, if one variable loses more variation than another, the apparent strength of their relationship may increase or decrease depending on the direction of this imbalance. Importantly, the experiment shows that __there is no consistent or systematic relationship between correlation coefficients and the loss of variation. Instead, the observed outcomes depend on a complex interaction between spatial structure, autocorrelation, and the way aggregation redistributes variation across variables.__ This helps explain why the results of earlier parts of the experiment appear so variable and reinforces the broader point that statistical relationships in spatial data are highly sensitive to how space is partitioned.

## __Reanalysis of Openshaw’s First Experiment__

Following the methodology described by Openshaw in the original chapter, we recreated the experiment in R. Due to data availability constraints, we are unable to reproduce Openshaw’s exact results. Instead of congressional election data, we use presidential election data, which yields a baseline correlation coefficient of approximately __0.22__. Using this as our starting point, we conducted 1000 simulations for both zoning and grouping systems and visualized the resulting loss of variation under different aggregation schemes. Despite differences in the data, the patterns we observe closely match Openshaw’s original findings.

If you are interested in the details of Openshaw’s first experiment, including the implementation of the zoning algorithm, you can explore our R-based implementation. The GitHub repository containing all materials needed to reproduce the experiment can also be found __[here](https://github.com/giscience-research/Learn-MAUP)__.

<a href="https://giscience-research.github.io/Learn-MAUP/" target="_blank">
 <strong>Click here to open in full page</strong>
</a>

<iframe
  src="https://giscience-research.github.io/Learn-MAUP/"
  width="1300"
  height="500"
  style="border:0;">
</iframe>

Taken together, the first experiment demonstrates that statistical results in spatial analysis are highly sensitive to how data are aggregated. Even when using the same underlying data, simply changing the scale or the way spatial units are grouped can produce dramatically different correlation coefficients. At coarser scales, a wide range of outcomes is possible, while at finer scales results become more constrained, though not necessarily stable. Differences between zoning and grouping systems further highlight that spatial structure plays an important role in shaping these outcomes.

At a deeper level, the experiment reveals that these variations are driven by the loss of variation that occurs during aggregation, and more importantly, by the unequal (differential) loss of variation across variables. Because this loss is neither consistent nor predictable, there is no systematic relationship between aggregation and correlation. 

## __Standard and Non-Standard Error__

As a brief pivot, and also to situate our discussion of scale within the broader context of uncertainty quantification in GIScience, we now briefly turn to the idea of non-standard error.

As researchers, we face at least two major sources of uncertainty when conducting geographic analyses. First, uncertainty arises from sampling. If we repeat the same analysis using different samples, we would observe variation in the results. This variability is known as __standard error__, and it is something we are generally familiar with.

<div align="center">
    <img src="../../assets/scale-se.gif" alt="mapscale" width="800" height="800">
</div>

__Figure 1__: Illustration of standard error.

There is, however, a second type of uncertainty that arises not from the data, but from the decisions we make in designing and conducting our analyses. This is known as __non-standard error__. Non-standard error exists because there is rarely a single, agreed-upon way to conduct a geographic analysis. Instead, multiple reasonable analytical choices are often available, leading to a branching set of possible analytical paths. Once a particular path is selected, we obtain an estimate and a corresponding standard error. But if we hold the data fixed and instead vary these analytical choices, the resulting estimates may change. The variation across these alternative paths is what we refer to as non-standard error.

<div align="center">
    <img src="../../assets/scale-nse.gif" alt="mapscale" width="800" height="800">
</div>

__Figure 2__: Illustration of non-standard error.

Openshaw’s formulation of the modifiable areal unit problem can be understood as a localized and concrete example of non-standard error. To put it simply, their demonstration of how changes in the zoning system alone, which is one of many possible analytical decisions, can produce correlation coefficients ranging from −1 to +1, is a simulated measure of non-standard error.

Geographic analysis involves many such decisions, with scale being only one of them. If scale alone can produce such large variations in results, it follows that other analytical choices may have similarly significant effects. This implies that we are often working within a large “decision space,” where different combinations of choices can lead to different outcomes. __Whether we fully understand, explore, and report this range of possible outcomes plays a critical role in the validity of our conclusions.__ This, in turn, highlights the importance of conducting sensitivity analyses and being mindful of the implications of the decisions we make throughout the research process.
