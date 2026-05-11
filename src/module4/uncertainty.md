# __Knowing an Uncertain World__

As we move toward the end of the course, we have already spent time thinking about how geographic phenomena are conceptualized, represented, interpreted, and analyzed. A final step in that sequence is validation: how do we know whether our representations, analyses, and conclusions are trustworthy? Once we ask that question, we immediately have to confront __uncertainty__. Validation is not only about checking whether something is right or wrong; it is also about understanding how confident we can be, where that confidence breaks down, and what kinds of uncertainty remain.

The desire for certainty is deeply familiar. Perfect knowledge has long been one of humanity’s ideals, because knowing something for certain makes action easier. In GIS and other geospatial technologies, this desire for certainty becomes especially important. Being right can matter enormously, and in some applications it can quite literally be a matter of life and death. If a flood-risk model, emergency evacuation map, disease exposure surface, or infrastructure database is wrong, the consequences are not just technical; they can shape decisions that affect people and places.

Much of GIScience has therefore focused on uncertainty as a problem of geographic information: error, inaccuracy, imprecision, ambiguity, vagueness, and related issues in spatial data and their products. This work is essential, but it is not the whole story. Geospatial data are not geography itself; __they are representations of geography__ (as we've repeatedly learned about in previous lessons). They are produced through choices about measurement, classification, scale, abstraction, modeling, and visualization. Because of this, uncertainty is not only something that enters when data are bad or users make mistakes. Uncertainty is built into the process of producing geographic knowledge.

So this week, __we will treat uncertainty as a condition of GIScience that has to be understood and communicated__. We will begin with a broader philosophical and epistemological discussion of uncertainty. We need to understand uncertainty from a narrow technical issue into an epistemological issue. We will then turn to the distinctive complications of uncertainty in GIScience In the second part of the lesson, we will move into a more structured deconstruction of uncertainty types and examine how uncertainty can be identified, organized, and quantified in practice.

## __Uncertainty and Knowledge Production__

When we talk about uncertainty, we often begin with familiar problems: incomplete data, inaccurate measurements, imprecise boundaries, or invalid information. These are important, but they do not capture the full range of uncertainty involved in producing geographic knowledge. Some forms of uncertainty are not simply caused by bad data. They come from the broader problem of what we can know, how we know it, and where knowledge itself reaches its limits.

We can think about several forms of __“not knowing.”__

- Some things are unknown because we have not yet observed them. 
- Some things are not understood because we lack the right theory or method. 
- Some things remain undiscussed because they are taken for granted, politically sensitive, or institutionally ignored. 
- Some things are deliberately hidden, distorted, or avoided because they are inconvenient to know. 

These forms of ignorance can affect both experts and non-experts. In principle, many of them are correctable: better data, better methods, better theory, more training, more transparency, or more open discussion could reduce them.

But there is a more difficult category: __that which cannot be fully known__. Here, uncertainty is not simply the result of poor information. It may come from logical, mathematical, physical, linguistic, or conceptual limits. We can call this __intrinsic uncertainty__: uncertainty that is built into the nature of knowledge production rather than uncertainty that can be eliminated by collecting more data.

### __Uncomputability and Undecidability__

One example comes from mathematics and computer science. Gödel’s incompleteness theorem shows that within any sufficiently complex formal system, there will be statements that cannot be proven either true or false from within that system. Related ideas of uncomputability and undecidability show that some problems cannot be solved by a general algorithm. This matters for GIScience because GIS depends heavily on computation, algorithms, models, and formal representations. Even formal systems, which seem like the most certain kind of knowledge system, have limits.

### __Chaos and Complexity__

In physics and environmental modeling, complex systems may be deterministic but still unpredictable in practice or even in principle over the long term. Chaos theory and complex nonlinear systems exemplify why the future may be unknowable, even if we understand some governing rules. This is important for geographic research because many geographic phenomena, such as urban growth, climate impacts, disease spread, flooding, migration, land-use change, are complex, nonlinear, and dynamic. Even when we understand some of the governing processes, the future may remain uncertain.

### __Vagueness and Classification__

A third example comes from vagueness and classification. The __sorites paradox__ asks: if one grain of sand is not a heap, and adding one grain at a time never clearly creates a heap, when exactly does a heap begin? This may sound abstract, but it is directly relevant to GIScience. Many geographic categories work this way. How many trees make a forest? How many buildings make a town? Where exactly does an urban area end and a rural area begin? Where is the boundary between suitable and unsuitable, vulnerable and not vulnerable, high risk and low risk?

This connects back to our earlier discussions of representation and spatial relationships. Many GIS operations require discrete categories, crisp boundaries, and stable objects, but the world is often continuous, heterogeneous, and dynamic. When we classify places as forest/non-forest, urban/rural, vulnerable/not vulnerable, or suitable/not suitable, we impose sharp distinctions on phenomena that may not have sharp boundaries. 

## __Uncertainty and Modes of Geospatial Knowledge Production__

Let us bring the discussion of uncertainty more directly into GIS practice. Geographic knowledge is not produced in only one way. Sometimes we begin with available data and ask what patterns or explanations can be derived from them. Sometimes we begin with a method and collect the data required by that method. Sometimes we begin with a desired product or model and work backward to identify the methods and data needed to produce it. Each of these workflows produces knowledge differently, but none of them escapes uncertainty

### __Data Driven Approach__

In a data-driven approach, the data come first. The characteristics of the available data determine what methods can be applied and what kind of final product can be produced.

```
Data → Method → Product
```

The uncertainty here comes from trying to infer explanations, patterns, or models from the data. This is a form of __abductive reasoning__, or reasoning toward the best explanation. The challenge is that the same spatial pattern may have multiple possible explanations, and the data alone may not uniquely identify which explanation is correct.

For example, a cluster of high asthma rates might be explained by air pollution, housing age, socioeconomic inequality, healthcare access, reporting differences, or some combination of these factors. The spatial pattern is real, but its meaning is not automatically given by the data. We still have to interpret it, and that interpretive step introduces uncertainty.

### __Method Driven Approach__

In a method-driven approach, the method comes first. We begin with a standardized model or procedure, and that method determines what data are needed, what format they must take, and what kind of product can be generated.

```
Method → Data → Product
```

This approach may seem more secure because it relies on an established procedure. But method-driven knowledge still contains uncertainty. A method imposes requirements on the data, and the quality of the final product depends partly on how well the available data meet those requirements. When data come from different sources, with different resolutions, dates, classification schemes, and reliability, even a standardized method can produce uncertain results.

For example, a suitability model may require slope, land cover, distance to roads, and flood risk. Each layer may have different spatial resolution, temporal currency, classification uncertainty, and source reliability. The method may be clearly defined, but the result is not automatically certain because the input layers do not all carry the same quality or meaning.

### __Product Driven Approach__: 

In a product-driven approach, the desired product comes first. We begin with a target output, such as a map, model, simulation, or decision-support product, and then select the methods and data needed to create it.

```
Product → Method → Data
```

The uncertainty here comes from fitting a desired model or product to the world. Models depend on assumptions about what matters, what can be ignored, and how geographic processes work. But those assumptions may need to change when new information appears, or when the model is applied to a different place or time. This connects to __nonmonotonic reasoning__, where conclusions are provisional and may have to be revised as additional information becomes available.

For example, an urban growth model built for one region may not work well in another because zoning laws, land markets, transportation systems, infrastructure constraints, environmental conditions, and cultural preferences differ. The model may be internally logical, but that does not guarantee that it fits every geographic context. The uncertainty lies in the gap between the desired product and the complexity of the world it is meant to represent.

## __The Spatial Specialty of Uncertainty__ 

Regardless of which mode of knowledge production we begin with, GIScience still faces a more basic problem: geospatial data are never geography itself. They are representations of geography. This brings us back to the idea we introduced during the cartography lesson: __the map is not the territory__. In a GIScience context, this means that geospatial data do not give us direct access to the world. This is why uncertainty is not a marginal issue in GIScience. 

Goodchild (2020) lists several reasons why geographic data cannot perfectly represent the world.

- First, __measurement is never perfect__. Any attempt to measure location inherits the limitations of the instrument being used, whether that instrument is an older surveying tool or a modern GPS. 
- Second, many geographic categories are __not strictly replicable__. If two experts independently create a soil map of the same place, they may not produce identical maps. This does not necessarily mean one expert is wrong. It may mean that soil types, land cover, land use, and similar categories involve interpretation.
- Third, geospatial data are __scale-dependent__. Every dataset involves choices about what to include, what to leave out, what to simplify, and at what level of detail the world should be represented.

These issues also remind us that __spatial uncertainty is not exactly the same as uncertainty in many non-spatial datasets__. In some fields, uncertainty can often be modeled through relatively simple statistical assumptions, such as normally distributed error. Spatial data are more complicated because location, scale, adjacency, and spatial dependence matter. Uncertainty is also about where that error occurs, how it relates to nearby errors, and how it moves through spatial analysis.

__Maps Look too Certain__

One important complication is that maps often look more certain than they really are. As we've learned, cartography has long presented the world as clean, ordered, and simplified: every feature appears in its proper place, every boundary looks crisp, and every category seems stable. This visual clarity gives maps authority, but it can also make uncertainty invisible. A map may look objective and precise, while behind it are choices about data sources, scale, classification, symbolization, generalization, and model assumptions. This connects directly back to our earlier discussions of representation: maps do not simply show the world; they actively construct a version of it.

__Errors Cluster in Space__

A second complication is spatial autocorrelation. Because nearby things tend to be more similar than distant things, nearby errors may also be similar. Spatial errors are often not randomly scattered across space. Instead, errors in nearby locations may be related because they come from the same instrument, data source, interpolation method, or classification process. A digital elevation model, for example, may contain errors of several meters. If every elevation error were independent from its neighbors, calculating slope from adjacent elevation values would be extremely unreliable. But because nearby elevation errors may be similar, relative differences over short distances can sometimes be more reliable than absolute elevation values. The key point is that spatial uncertainty has structure.

__Data Carry Histories__

This makes __provenance__ especially important. To understand uncertainty, we need to know where a dataset came from, how it was produced, what instruments or sources were used, what errors may have been introduced, and whether multiple datasets share the same underlying sources. This matters when combining datasets. Two flood-risk datasets, for example, may appear to offer independent evidence, but if they both rely on the same elevation model, they may share the same underlying elevation uncertainties. Comparing them does not fully validate one against the other. Without provenance information, we may overestimate how independent or reliable our evidence really is.

__Models Propagate Uncertainty__

Uncertainty does not stop with data. It also enters through models. Models contain uncertainty from their input data, but also from missing variables, uncertain parameters, calibration problems, and structural assumptions. A model output may look like a final answer, but it is actually the result of uncertain data passing through uncertain assumptions.

This point is developed clearly in Longley et al.’s uncertainty framework. Figure X presents uncertainty as a sequence of filters between the real world and GIS-based knowledge. The first filter is __conception__: how we define the geographic phenomenon in the first place. Before mapping a forest, neighborhood, flood zone, or vulnerable population, we must decide what counts as that thing, where its boundaries are, and what unit of analysis is appropriate. The second filter is __measurement and representation__: how that concept is translated into data through instruments, classifications, spatial resolution, raster or vector models, and generalized boundaries. The third filter is __analysis__: how GIS operations such as overlay, buffering, interpolation, aggregation, and modeling further transform the data and propagate earlier uncertainties. The main lesson is that uncertainty is **cumulative**. A final GIS map or model output may look clean and precise, but it carries uncertainty from earlier stages of the workflow.

## __New Directions of Uncertainty Research__

To end this part of the uncertainty lesson, it is important to note that several recent developments in GIScience make uncertainty even more important. As geospatial data become larger, more diverse, more automated, and more central to scientific and policy decisions, we need to ask new questions about how uncertainty is produced, detected, modeled, and communicated.

### __Uncertainty in Data Science__

One major challenge comes from the rise of spatial data science, machine learning, artificial intelligence, and data-driven discovery. These approaches often encourage us to “let the data speak for themselves.” But from a GIScience perspective, geographic data never speak from nowhere. Spatial data are shaped by spatial dependence, spatial heterogeneity, spatial resolution, scale, and representation. These principles affect what patterns can be found, what patterns are meaningful, and what patterns may be artifacts of the data or method.

This raises two important concerns. First, spatial data science should not search blindly for patterns without incorporating geographic principles. Not all patterns are equally plausible, and not all detected patterns are meaningful. Second, because all geospatial data are uncertain, machine learning and AI must also confront the specific structure of spatial uncertainty. If the input data contain measurement error, classification uncertainty, spatial autocorrelation, or uneven provenance, then the patterns detected by an algorithm may also be uncertain.

One way to think about this is to ask whether spatial analysis should begin not with one dataset, but with multiple possible versions of geographic reality. Each version could represent a plausible state of the world given known uncertainties. We could then ask: do the same patterns appear across these different realizations, or are the results sensitive to uncertainty in the data? This shifts the question from simply “What pattern did the algorithm find?” to “How robust is this pattern under spatial uncertainty?”

### __New Data Sources__

A second challenge comes from the rise of new geospatial data sources. Traditional data sources, such as censuses and national mapping agencies, were often carefully documented, standardized, and produced through relatively controlled procedures. Today, GIScience increasingly works with massive, diverse, and less controlled data sources: GPS traces, social media data, volunteered geographic information, remote sensing products, mobile phone records, sensor networks, and multiple overlapping data products from different agencies or platforms.

This creates a problem of synthesis. Instead of having one authoritative source for a question like “What is the elevation of this point?”, we may now have multiple digital elevation models, digitized contours, spot-height catalogs, and other derived products, each with different resolution, provenance, and quality. The challenge is no longer only how to analyze one dataset, but how to integrate multiple datasets into a single estimate while also assessing the uncertainty of that estimate.

Importantly, more data or higher-resolution data do not automatically mean less uncertainty. Individual-level tracking data, for example, may seem highly precise, but they introduce new uncertainties related to GPS accuracy, sampling intervals, device differences, missing observations, privacy transformations, and interpolation between recorded locations. Social media data may provide detailed spatial traces, but those traces are socially and technologically biased. So the key lesson is that new data sources do not eliminate uncertainty; they often create new forms of uncertainty that traditional GIS methods were not designed to handle.

### __Replicability and Place-Based Variation__

A third challenge is replicability. In many sciences, a result is expected to be more trustworthy if it can be replicated. But in GIScience, replicability is complicated by spatial heterogeneity. Conditions vary across the Earth’s surface, and the processes operating in one place may not operate in exactly the same way somewhere else. This means that a result from one region may not reproduce perfectly in another region, even if the original analysis was carefully conducted.

This creates a difficult interpretive problem. If an analysis produces different results across places, does that mean the original result was wrong? Does it mean the data or methods were uncertain? Or does it mean the places themselves are genuinely different? In GIScience, a failure to replicate may not always signal scientific failure. It may reflect real spatial heterogeneity, place-specific processes, or uncertainty in the way geographic data and models travel across contexts.

---

References:

*Couclelis, H. (2003). The certainty of uncertainty: GIS and the limits of geographic knowledge. Transactions in GIS, 7(2), 165–175.*

*Goodchild, M. F. (2020). How well do we really know the world? Uncertainty in GIScience. Journal of Spatial Information Science, 20, 97–102.*

*Longley, P. A., M. F. Goodchild, D. J. Maguire, and D. W. Rhind. 2008. Geographical information systems and science 2nd ed. Chichester: Wiley. (only chapter 6: Uncertainty, pages 127-153)*