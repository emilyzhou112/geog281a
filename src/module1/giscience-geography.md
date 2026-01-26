# __GIScience and Geography__

In the previous lesson, we examined the tool–science debate, which revealed that GIS is never “just a tool”: its data models, algorithms, defaults, and workflows actively shape what kinds of questions can be asked and what kinds of answers can be produced.

This lesson picks up where that debate leaves off. Rather than asking whether GIS is a science, it asks a different but closely related set of questions: __How has GIScience related to geography over time?__

## __Form or Process__

Before delving into more recent debates, we begin with a classic tension that has shaped discussions of GIScience and geography for decades: form versus process.

In 2004, Goodchild argued that GIS and GIScience had become very good at representing form—objects, shapes, and spatial patterns—but that geography’s core intellectual concern lies in process: how things change, interact, and unfold across space and time. As GIS matured, it unintentionally tilted the discipline toward form, because its data models, representational frameworks, and map-based metaphors privilege static snapshots over dynamic explanations.

Over time, this imbalance raises a concern: GIScience risks drifting away from geography’s explanatory and exploratory ambitions if it remains focused on form rather than enabling inference about process. This tension sets the stage for later questions about representation, disciplinary boundaries, and the future direction of GIScience.

## __An Evolving Relationship__

Building on this concern, Goodchild (2019) situates the form–process tension within a broader historical account of the evolving relationship between Geography and GISystems. He identifies three overlapping phases:

- __Phase 1 (1960s-1980s)__: during which there was a strong and largely unproblematic relationship between Geography and GISystems. Geographers dominated education and research, and traditional practices in cartography and remote sensing were deeply embedded in early system design. GISystems moved steadily toward comprehensive handling of geographic information.
- __Phase 2 (1990s-2000s)__: during which two major challenges emerged. First, many geographers began to question the intellectual merits of GISystems, a critique amplified by their widespread adoption in other disciplines. Second, GISystems were increasingly criticized for their social implications, including surveillance, privacy, and military origins. At the same time, research agendas broadened: data models became more complex, social critique entered GIS research, and GIS education expanded beyond geography departments.
- __Phase 3 (2000s-present)__: during which data science, big data, consumer GIS, and computer science increasingly shape geospatial practice. Geography risks losing influence unless it continues to assert why spatial thinking matters.

Goodchild warns that this new emphasis on data as the foundation of science, often ignoring how data are assembled, their provenance, and their relationship to the real world, is especially problematic. Effective and scientifically rigorous analysis becomes difficult without ground truth: knowledge of the geographic world gained through field observation, careful description, and attention to data quality.

> Without geographic thinking, GIS risks becoming data-driven computation divorced from social context, spatial reasoning, and geographic understanding. In this sense, the earlier concern about form and process reappears here at a disciplinary scale.

___A Related Detour:___

Against this backdrop, the rise of data science raises a parallel question: what kind of field is Geographic Data Science?

Scheider et al. (2020) argue that GDS is not yet a scientific discipline, but rather a community of practice. A scientific discipline, they contend, must have its own concepts and its own questions. GDS currently does not. It borrows concepts from Geography, methods from GIScience, Statistics, and Machine Learning, and infrastructure from Computer Science <sup><a class="sidenote-ref" href="#sn-1">1</a></sup>.

<div class="sidenote" id="sn-1">
<strong>1.</strong> Interestingly, this argument defends GIScience rather than replacing it. GIScience is framed as a meta-science, akin to Statistics or Information Science. Its role is not to answer geographic questions directly, but to study how geographic information is represented, measured, and reasoned with. This distinction becomes crucial in the discussions that follow.</div>

## __The Geographicness in GIS__

Picking up on these concerns, Guan, Wilson, and Knowles (2019) explicitly ask what it means to emphasize the geographic in GIS.

They argue that the geographic aspects of GIS remain insufficiently developed, and call for continued theoretical and methodological work to support a more geographic GIS. Central to their argument is a persistent ambiguity between:

- spatial analysis (Cartesian space, coordinates),
- geospatial analysis (Earth-referenced space), and
- geographic analysis (space entangled with social, physical, and historical processes)

GIS software, they argue, is very good at the first two, but much weaker at the third. As GIS spreads into the digital humanities, social sciences, and data science, there is a growing danger that “geographic” collapses into “spatial.”

They do not claim that GIS can fully capture all geographic knowledge—some epistemological irreducibility remains—but they insist that GIS theory and method could be far more deeply geographic than they currently are.

## __Towards Doing GIScience and Geography__

Taken together, these readings raise a final question: how should we study, teach, and practice GIScience in relation to geography moving forward?

Most recently, O’Sullivan argues that GIScience and geography share a common conceptual ground made up of many fundamental ideas—space, scale, place, regions, networks, time, process, and patterns. However, GIS platforms often flatten these ideas into inflexible representations of points, lines, and polygons. As a result, GIS constrains how geographic thinking can be expressed, explored, and extended.

While some argue that GIS primarily needs better qualitative tools, O’Sullivan suggests that this would not make much difference. The deeper issue is that representational geometry itself is rigid. We do not need a whole new platform to “do GIS.” Rather, it is essential to rethink the geographic representation model inside GIS and allow alternative spatial logics<sup><a class="sidenote-ref" href="#sn-2">2</a></sup> to be implemented. As what he said:

> I am convinced that the task of reimagining and reconstructing GIS as a flexible tool for creating diverse human geographies … will depend on GISers taking geographical thought much more seriously than they have hitherto.

<div class="sidenote" id="sn-2">
<strong>2.</strong> non-Euclidean space, relational space, etc.</div>

Speaking more broadly about representation, a major stumbling block for many critics of GIScience is its failure to take seriously the problematic nature of __representation__. Representation should be understood as process and practice, not as static objects. For example,

>The important question is not what a map is, nor what a map does, but how the map emerges through contingent, relational, context-embedded practices.

This reframing shifts attention away from maps as finished products and toward the practices, assumptions, and decisions through which representations are produced.

O’Sullivan argues that we need to interrogate more closely what we mean by terms like related, near, and distant. Finding ways to recognize the fuzziness, ambiguity, porosity, and uncertainty of boundaries has the potential to open up new and different ways of seeing geographies. Doing so could set the stage for representing processes, events, and patterns explicitly, rather than treating familiar GIS entities as fixed and pre-given.

Then,one way of “doing GIS” today is to develop a vision that is both technical and critical. This requires taking the geographical in GIScience more seriously, and for geography to take GIScience more seriously as well. This leads to O’Sullivan’s primary conclusion:

> Geography and GIScience curricula at all levels should actively explore the common ground they share.

There is no reason why an introductory GIS course cannot also be a class that critically examines fundamental geographic ideas—doing so beyond a narrow focus on the technical issues that arise from working with existing representations.

---

Reference:

*Goodchild, M. F. (2004). GIScience, geography, form, and process. Annals of the Association of American Geographers, 94(4), 709–714*

*Goodchild, M. F. (2019). Geography and geographic information science: An evolving relationship. The Canadian Geographer / Le Géographe canadien, 63(1), 5–11.*

*Scheider, S., Nyamsuren, E., Kruiger, H., & Xu, H. (2020). Why geographic data science is not a science. Geography Compass, 14(11)*

*Guan, W. W., Wilson, M. W., & Knowles, A. K. (2019). Evaluating the geographic in GIS. Geographical Review, 109(3), 297–307.*

*O’Sullivan, D. (2020). Doing GIScience, doing geography. In Geographic information analysis (2nd ed., pp. 247–254).*