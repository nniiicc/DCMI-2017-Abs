**Abstraction Layers for Data on the Web**

**Overview**

Open data  - structured and unstructured public sector information freely available on the web - are an increasingly important object of study for information scientists (e.g. Attard et al. 2016). In this project report we discuss challenges in developing knowledge representation and organization systems for open data, focusing specifically on the implementation of vocabularies for open civic data. We argue that a choice between richness of expressivity and ease of use results in vocabularies with abstraction layers that are either leaky or sticky. Leaky abstraction occurs when a vocabulary exposes (leaks) details from a higher level abstraction. Leaky abstraction has the potential to communicate information about a resource that lacks relevancy and can confuse domain practitioners. Sticky abstraction occurs when a vocabulary obscures important details about a resource found in a lower-level abstraction. Sticky abstraction makes it difficult to transfer knowledge about the resource between domains. In the following sections we will offer a motivating case of sticky abstraction from urban planning. We apply the W3C&#39;s Data Usage Vocabulary (DUV) to the open data used in this study. We then conclude by summarizing lessons learned from this case, and the potential for further development of what we refer to as a &#39;rhetorically powerful&#39; theory for abstraction layers.

**Up and Down the Ladder of Abstraction**

One of persistent challenges in developing knowledge organization systems is finding a balance between rich expressive terminology and computational tractability (Levesque &amp; Brachman, 1987). In practice, this challenge is often faced when designing descriptive metadata standards, controlled vocabularies, or user tagging and commenting features. Balancing expressivity vs tractability can be achieved through an appeal to layers of abstraction: Higher level abstractions, such as subclass distinctions, allow designers to create richly expressive hierarchies in open data portals (Thorsby et al., 2016); Lower-level abstractions, such as a controlled vocabulary, can help make conceptual details tractable for the sake of indexing open data published on the web (Bizer et al. 2009).

One of the motivations of the work presented here is to develop a theory about how abstraction layers operate within knowledge organization implementations for data on the web. We believe that by describing these abstractions in greater detail designers of knowledge organization systems can gain what Halverson calls a &#39;rhetorical power&#39; for information systems theory- that is, the ability to identify and name phenomena that emerge in complex information systems (2002). We are especially interested in identifying, and giving name to how abstraction layers are used when implementing knowledge organization systems for open data published on the web.

**Urban Transport in Bologna**

The case under consideration comes from a research study attempting to understand population mobility within the densely populated city of Bologna (Italy). The goal of this study was to develop an urban transport model that can accurately simulate the impact of adding or removing different modes of transport, such as a bike sharing program (Caiati et al, 2016). In the context of urban planning, the development of an accurate transport model depends on access to valid and accurate real-world data, such as traffic counts, demographic data from census tracts, and road-network information (e.g. length of a thoroughfare, speed limits, vehicle power source, etc.).

Open data from the City of Bologna as well as the National Institute for Statistics (Italy) was used for much of this work (Caiati et al, 2016). But, as the authors note, &quot;Even though open data platforms are experiencing a rapid expansion over the last years, a very limited number of urban mobility dataset that describes real world travel demand and road traffic data over an urban area is publicly available today.&quot; (Caiati et al., 2016) Understanding how these researchers combined different publicly available demographic variables, tested their model with existing data, and came to preliminary conclusions about the effectiveness of bike sharing is of great interest to urban planners working on similar problems.

The Data Usage Vocabulary (DUV), developed by the W3C&#39;s Data on the Web working group, provides a set of terms for citing, offering feedback to data publishers, and rating open civic data. DUV is meant to interoperate with the Data Catalog Vocabulary (DCAT) standard used by many open data publishers, including the City of Bologna.  As an example of how DUV might be applied to this case, below is a set of comments by the authors about their use of the City of Bologna&#39;s data:

:circulo-2016-05-17

        a dcat:Dataset ;

        dct:title &quot; Cars circulating Bologna Metro Area divided by power-2016&quot; ;

        dct:identifier &quot; http://dati.comune.bologna.it/node/1063 &quot;^^xsd:anyURI   ;

        dct:issued &quot;2016-05-17&quot;^^xsd:date ;

        pav:version &quot;1.0&quot; ;

        dct:publisher : Automobile Club of Italy;

        duv:hasDistributor :Open-Data-ComuneDiBologna;

        disco:fundedBy :ComuneDiBologna ;

        dct:created &quot;2016-05-17&quot;^^xsd:date ;

        dcat:distribution : &quot;http://dati.comune.bologna.it/download/file/fid/3733&quot; &quot;^^xsd:anyURI   ;

        duv:hasFeedback :comment1`

        .

:circulo-2016-05-17

        a dcat:Distribution ;

        dcat:downloadURL &lt;&quot; http://dati.comune.bologna.it/download/file/fid/3733&quot;;

        dct:title &quot;CSV distribution of cars circulating Bologna Metro Area divided by power&quot; ;

        dct:description &quot;CSV distribution of the bus stops dataset of MyCity&quot; ;

        dcat:mediaType &quot;text/csv;charset=UTF-8&quot; ;

        dct:license &lt;http://creativecommons.org/licenses/by-sa/3.0/&gt;   ;

        duv:hasFeedback :comment2.

:comment1

        a duv:UserFeedback ;

        oa:hasBody &quot;Resolution of dataset is by hour, and is missing hours 2000-2400&quot;^^xsd:string;

        oa:hasTarget : circulo-2016-05-17;

        oa:motivatedBy oa:editing;

        dct:creator :researchExpert

:comment2

        a duv:UserFeedback ;

        oa:hasTarget : circulo-2016-05-17;

        oa:hasBody &quot;Power is divided by three ACI type – petrol, electric, and hybrid&quot; xsd:string ;

        oa:motivatedBy oa:editing;

        dct:creator :researchExpert

**Sticky Abstractions**

In the above example the research expert has noted two limitations faced in using the dataset for developing an urban transit model. First, the dataset has a temporal resolution that is calculated by hour, but is missing a set of hours each day for the year of 2016. Second, the dataset makes a distinction by vehicle type that is limited to three types of automobiles – electric, petrol, and hybrid. In the DUV model, this kind of information is meant to be conveyed only to data publishers so that they can interpret and better understand users of the data. As such, DUV expressions are nested within DCAT records, but are not exposed in search functions implemented by a data portal. We argue that this information is of great value to urban planners working in the same area of research – urban mobility. In order for the expressed information to be of value to potential data reusers, it needs to &quot;stick&quot; with the dataset – that is, it needs to become a part of the harvestable metadata that allows for an individual to discover and judge the dataset with the relevant context of use. The challenge for DUV then is to find a way to attach, and communicate this kind of information to domain experts.

In future work, we will continue to model instances of feedback about this dataset from Caiati et al&#39;s work, so as to better understand ways that DUV could be of value to potential data reusers in the field of urban planning. In our presentation of this ongoing work, we will make recommendations about how DUV information can be included in DCAT records as annotations that are discoverable when searching for data with an API that connects open data portals in Europe, and the USA.



**Works Cited**

Attard, J., Orlandi, F., &amp; Auer, S. (2016). Value Creation on Open Government Data. In _2016 49th Hawaii International Conference on System Sciences (HICSS)_ (pp. 2605–2614). https://doi.org/10.1109/HICSS.2016.326

Bizer, C., Heath, T., &amp; Berners-Lee, T. (2009). Linked data-the story so far. _Semantic Services, Interoperability and Web Applications: Emerging Concepts_, 205–227.

Caiati, V., Bedogni, L., Bononi, L., Ferrero, F., Fiore, M., &amp; Vesco, A. (2016). Estimating urban mobility with open data: A case study in Bologna. In _Smart Cities Conference (ISC2), 2016 IEEE International_ (pp. 1-8).

Halverson, C. A. (2002). Activity theory and distributed cognition: Or what does CSCW need to DO with theories?. _Computer Supported Cooperative Work (CSCW)_, _11_(1), 243-267.

Levesque, H. J., &amp; Brachman, R. J. (1987). Expressiveness and tractability in knowledge representation and reasoning. Computational intelligence, 3(1), 78-93.

Thorsby, J., Stowers, G. N., Wolslegel, K., &amp; Tumbuan, E. (2016). Understanding the content and features of open data portals in American cities. _Government Information Quarterly_. Retrieved from http://www.sciencedirect.com/science/article/pii/S0740624X16301071
