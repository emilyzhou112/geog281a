# __Spatial Ontologies - Place__

In the previous lesson, we examined how GIScience conceptualizes __space__. We began with the familiar absolute view of space as a fixed geometric container defined by coordinates, and then moved toward relative and relational perspectives that better capture proximity, interaction, and process. Throughout this progression, we saw how many real-world phenomena cannot be fully understood through Euclidean distance alone. Relative and relational thinking brought us closer to how the world actually works. Nevertheless, even these richer conceptions still struggle to account for how places are felt, experienced, remembered, and given meaning by the people who inhabit them. There remains a fundamental dimension of geographic life that is difficult to quantify or formalize, and it is this dimension that we call __place__.

## __The Representation of Experience__

Loosely speaking, space—conceived absolutely—belongs to the realm of calculation, coordinate systems, and geodesy, while place belongs to the realm of everyday life and practice, emotion, and meaning. This distinction makes intuitive sense because, in ordinary life, we rarely think in coordinates or buffers. Instead, we think in terms like home, campus, downtown, or my neighborhood.

Formally defined, following O’Sullivan, place can be understood as the intersection of __space with experience and meaning__, or more completely, as both a context for and a product of physical, social, economic, and cultural processes. A coordinate can be anywhere, but “home” cannot. A polygon may delineate a neighborhood boundary, but that boundary rarely matches how residents themselves describe their community. Places carry meaning not only because of human understanding, culture, and memory, but also because they are sites where the processes that make places are continuously shaped and reshaped by the character of those places themselves (more on that in the next lesson). In other words, place is not just where things happen: it actively participates in shaping what happens.

Perhaps an interesting example of this lived and negotiated character of place can be seen in projects like [Hoodmaps](https://hoodmaps.com/philadelphia-neighborhood-map). Rather than presenting neighborhoods as official administrative boundaries, Hoodmaps crowdsources how residents feel about different areas and label them accordingly. 

<iframe
  src="https://hoodmaps.com/philadelphia-neighborhood-map"
  width="1000"
  height="600"
  style="border:0;">
</iframe>

These labels are obviously subjective, humorous, and sometimes contradictory, yet they often feel more recognizable to everyday experience than census tracts or ZIP codes. The map captures not geometry, but perception. It demonstrates that what counts as a "neighborhood" is not simply a polygon in a database, but a socially shared understanding built through everyday life. Feel free to swtich to another city you are interested in and explore the labels. Make sure to check which neighborhood each area of interest falls in.

Importantly, place is not just emotional or personal; it is also social and political. Places regulate behavior and encode expectations about who belongs and what is appropriate. Certain activities may feel "in place" in one setting and "out of place" in another. In this sense, place is inherently normative. As O’Sullivan illustrates through the example of graffiti, the same physical act can be interpreted very differently depending on where it occurs. Graffiti is a practice whose meaning is bound up with place and timing: what is considered vandalism in one location may be celebrated as public art in another. Graffiti is only "graffiti" when it is out of place.

To make this more concrete, consider the two images of the same vacant lot in the Frankford neighborhood of Philadelphia. In one, the lot appears abandoned, scattered with debris, and covered in unsanctioned graffiti. It may be read as neglect, disorder, or even danger. In the other, the very same space is reimagined as a community playground, with landscaping, seating, and murals integrated into a planned design. Here, similar visual elements (painted walls, open ground, informal activity) are interpreted entirely differently because the context has changed. One is labeled blight; the other, revitalization. What changed is not simply the geometry of the site, but the social meaning attached to it.

<div style="display:flex; gap:0.6rem; align-items:stretch;">
  <a href="../../assets/frankfordb4.jpg" class="zoomable" style="width:49%;">
    <img src="../../assets/frankfordb4.jpg"
         style="width:100%; height:310px; object-fit:cover; object-position:center;">
  </a>

  <a href="../../assets/frankfordafter.jpg" class="zoomable" style="width:49%;">
    <img src="../../assets/frankfordafter.jpg"
         style="width:100%; height:310px; object-fit:cover; object-position:center;">
  </a>
</div>

More broadly, neighborhoods can be welcoming to some groups and exclusionary to others. Decisions about zoning, policing, or development shape who has access to particular places and who does not. In this way, place is bound up with power. It is not simply a backdrop for social life, but an active participant in structuring it.

Understanding place is therefore essential to understanding how ideology is created and maintained. Ideological beliefs have effects precisely because they shape how people behave in and experience the world. Shared, or contested, understandings of what actions are allowable or inappropriate in particular places mean that place, and how places are defined, become central to the maintenance of power. Places are not only where social life unfolds; they are mechanisms through which social norms are reinforced, negotiated, and challenged.

## __Place in Relational Space__

Building on our earlier discussion of relational space, we can also think of places relationally. This shift is surprisingly easy to conceptualize. A neighborhood, for example, is shaped not only by what happens inside it, but also by commuting patterns, migration histories, economic ties, and cultural exchanges that link it to elsewhere. In other words, what makes a place what it is cannot be understood in isolation. It is always connected outward.

Doreen Massey (1991) suggests that places are processes, not things. They are constantly unfolding, being made and remade through time. Because of this, places are often messy, contradictory, and internally diverse, reinforcing their non-unitary nature. They are not coherent, bounded containers with stable identities. Furthermore, places in this sense do not have clear or fixed boundaries. Whatever uniqueness a place has is not derived solely from a set of local attributes or some purely internal history, but rather from the geographically specific sets of relations it maintains with other places and with wider social, economic, and political systems. These external relations interact with local histories to produce what we recognize as a place.

From this perspective, what we often call a __sense of place__ is not simply a feeling that emerges from being “local”, but an understanding of how a place is situated within broader networks of connection. The character of a place can only be understood by linking it to places beyond itself. A neighborhood is shaped by where its residents work, where goods come from, where cultural influences circulate, and where histories intersect. Its identity is relational rather than self-contained. Massey reiterates this point in her later work, arguing that we cannot seriously posit space as something outside of place as lived, nor simply equate the everyday with the local. If we truly think space relationally, then space is the sum of all our connections, and in that sense deeply grounded in everyday life—even when those connections stretch across the globe. 

As a caveat, however, it is also useful to consider the related concept of __placelessness__. If sense of place refers to the distinctiveness and meaning that emerge from lived experience and relational histories, placelessness describes the opposite tendency: environments that feel interchangeable, generic, or detached from local identity. Think of airport terminals, chain stores, shopping malls, or standardized developments that could exist almost anywhere. These spaces often lack the accumulated memories, social ties, and historical depth that give places their character. Placelessness reminds us that place is not guaranteed. It must be produced and sustained through practice. 

## __Situating Place in GIScience__

But experience is a tricky idea to pin down. While undeniably important, the concept of place has a long history in geography and related disciplines, yet it has also been plagued by a fundamental vagueness of definition: what exactly does the term mean, and how do we identify it in practice? This ambiguity poses a particular challenge for GIScience. If our tools are designed to represent geometry and measurable relationships, how do we represent something as subjective, contextual, and experiential as place?

Rather than tackling head-on the challenge of formalizing the subtleties of place, GIScientists have often sidestepped the issue and focused instead on limited interpretations of place that are more amenable to formalization, and therefore computation. Goodchild (2011) effectively summarizes these into two dominant approaches: place as location and place as context.

### __Place as Locations__

One of the most common ways GIScience handles place is by quietly reducing it back to __location__. This approach treats place names as labels that must ultimately be converted into coordinates or polygons through geocoding and gazetteers. Technically, this is framed as a translation problem: how do we map human ways of referring to places onto machine-readable geometry? Digital gazetteers and search engines attempt to solve this by returning a point or administrative boundary for any given name. From a computational standpoint, this is efficient and necessary. But conceptually, it is reductive. 

The problem is that place names are rarely precise. Many names are repeated across space. For example, there are dozens of “Springfields”, and their intended meaning depends heavily on context. Even when a single referent exists, equating a place with its coordinates misses the point entirely. As the text bluntly notes, London is not the same thing as its latitude and longitude.  A coordinate can identify where something is, but it cannot capture what it means, how it feels, or how it is socially understood. In this sense, “place as location” solves a technical indexing problem while sidestepping the richer cultural and experiential dimensions of place. It makes places legible to computers, but thinner to humans.

A useful illustration of this limitation can be seen in interactive projects like _Same Name_ map. In addition to showing the variations of place names across the US, we see that when different people are asked to identify or react to the same place name, their associations often vary widely depending on their personal histories and social contexts. The same label can evoke entirely different meanings for different people.

<div class="embed-wrapper">

  <div class="embed-toolbar">
    <button onclick="refreshFrame('lifeFrame')">↻ Refresh</button>
  </div>

  <iframe
    id="lifeFrame"
    src="https://pudding.cool/2023/03/same-name/"
    width="1000"
    height="500"
    loading="lazy">
  </iframe>
</div>

### ___Place as Geographical Context___

A second, more sophisticated move in GIScience shifts attention from naming to __context__. Taking geographical context seriously immediately reveals the inadequacy of simplistic notions of coincidence in space as a way of understanding what it means for things to interact in place. Instead of asking “Where is this place?”, researchers ask “What surroundings affect what happens here?” This perspective is often framed through the Uncertain Geographic Context Problem (UGCoP), which highlights how difficult it is to define the relevant environment influencing people’s outcomes.

For example, studies of health or mobility frequently assign individuals to the census tract where they live and treat that tract as their “neighborhood.” However, this effectively assumes that the activity space of each resident is confined to the census tract itself—something that will only rarely be the case—and furthermore assumes that the tract is somehow sealed off from everywhere else in the wider region. In reality, people commute, travel, socialize, and experience many overlapping environments throughout the day.This reveals a deeper issue: context is not fixed or uniform. Different people experience different “places” even when they share the same address. A student, a retiree, and a delivery driver might inhabit entirely different activity spaces within the same city. Any single boundary is therefore only an approximation. 

Compared to “place as location,” this approach is conceptually richer because it recognizes that places are defined by relationships and exposure, not just coordinates. Yet it still struggles with ambiguity. There is no single correct neighborhood size or context definition, only defensible assumptions.

## __Towards Computable Space__

Up to this point, we have seen two dominant strategies(reducing place to location or approximating it as context), but both remain constrained by geometric thinking. If place is experiential, relational, and socially constructed, then the obvious question for GIScience becomes: can place ever be made computational?

The __first__ step toward making place computational is to move beyond purely geometric representations and deliberately incorporate narrative structure into maps. Rather than treating maps as neutral stacks of layers, this approach recognizes that place is experienced sequentially and interpretively. Traditional GIS layering synthesizes information analytically: each theme is added as another independent layer, and meaning is expected to emerge from visual overlap. But this logic often fragments place into components rather than presenting it as a lived whole. In contrast, narrative cartography and story mapping reorganize representation around sequence, annotation, and storytelling. 

There are many compelling examples of this approach in both static and dynamic forms. As an exampke, see the biking journey map shown here. Instead of simply plotting GPS tracks, it organizes the author’s travel history into a story of movement across cities and landscapes. Insets, distances, and annotations guide the reader through experiences accumulated over time. The map does not just show routes; it communicates a personal relationship with those places

  <a href="../../assets/biking_screen.png" class="zoomable" style="width:100%;">
    <img src="../../assets/biking_screen.png"
         style="width:100%; object-fit:cover; object-position:center;">
  </a>

_Credit: Atlas Guo (2024), Source: [cartoguophy](https://cartoguophy.com/maps/biking.html)_

Dynamic story maps extend this idea even further. Interactive projects, such as the [Dark Skies map](https://jake-steinberg.github.io/2022_DarkSkies_js/), allow users to scroll, click, and explore place through sequence and discovery. The map becomes more like a guided experience here.

<iframe
  src="https://jake-steinberg.github.io/2022_DarkSkies_js/"
  width="1000"
  height="600"
  style="border:0;">
</iframe>

_Credit: Jake Steinberg et. al (2022)_

The __second__ step takes a different direction. Instead of translating place into narrative overlays, it attempts to directly implement explicit conceptual models of place computationally. In other words, rather than adding stories to maps, this approach asks whether the underlying data structures themselves can encode theories of how places are organized and experienced. O’Sullivan specifically  points to examples such as Lynch’s image-of-the-city framework (paths, edges, districts, nodes, and landmarks) as a set of perceptual elements that could be operationalized in GIS layers. Here, place is modeled not simply as geometry but as a structured configuration of meaningful features, whose combination produces a recognizable urban environment. 

!!! summary "Should we think of place and space as completely opposed where place is local, concrete, and particular whereas space is global, abstract, and general? Perhaps the answer to this is not that place is not concrete, grounded, real, lived, etc. It is that space is too. The local and immediate feels more concrete, because it is often visible, right there in front of us. But more remote events are no less real, even if they seem that way. Place cannot be fully computed, only approximated. What GIS can do is not to perfectly capture place, but to provide thoughtful, partial representations that remain sensitive to experience and interpretation."