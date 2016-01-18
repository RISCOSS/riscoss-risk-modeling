= Github Activeness Risks

= Analysed Risks
* **Project Bug Risk**: Refers to the possibility that critical bugs are present and/or not promptly patched.
* **Project Obsolescence Risk**: Refers to a lack of popularity of the project, due to a reduced number of people following it and reporting bugs and opening issues
* **Project Analysability Risk**:Refers to the (lack of) quality of the software to be easily understood from the adopter"
* **Project Activity Risk: Refers to the activeness of the project developers (contributors), their responsiveness in the issue tracker and the stability of the project (including project age)

**Note**: Remember that the risk description can be found in the file: for each risk (<event>), there is the description (<property name='description'.../>)

= Data-Collectors needed
In order to use this risk model, you need to have configured the riscoss-rdc-github data-collector for all the components are hosted in github. Detailed information about this data-collector in https://github.com/RISCOSS/riscoss-data-collector/wiki/GitHub-API-RDC

= Risk Analysis
The github_activeness risk model can be used in 1 and 2-layer configurations. For the 2-layer configuration you need: 
- _Project_: in the sense of a software artefact including other software artefacts (OSS or not)
- _OSS Component_: OSS software components included in Projects

==1-layer configuration
You can use these models following these steps:
1. Upload the model in the file _github_activeness_risks.xml_ in RISCOSS.
2. Create a risk configuration. E. g. you can create a risk configuration called _Component Activeness Risks_.
3. Assign _github_activeness_risks.xml_ to layer _OSS Component_. 

==2-layer configuration
You can use these models following these steps:
1. Upload the models in files _github_activeness_risks.xml_ and _github_project_activeness_risks.xml_ in RISCOSS.
2. Create a risk configuration. E. g. you can create a risk configuration called Project Activeness Risks_.
3. Assign _github_activeness_risks.xml_ to layer _OSS Component_ and _github_project_activeness_risks.xml_ to layer _Project_. 

== Analysing Activeness risks
You can create several entities of type _OSS Component_ or _Project_,  the _Project_ ones containing one or more of the _OSS Component_. Then, you will be able to create a Multi-layer analysis sessions:
- choosing an entity of type _OSS Component_ and the risk configuration _Component Activeness Risks_.
- choosing an entity of type _Project_ and the risk configuration _Project Activeness Risks_. In the results, you were be able to see risk results for all the entities involved in the analysis: the project and all the components that it includes.

== Impact on goals
If you want to include the impact over the related goals for the OSS adopter organization goals you also need to use one goal modelling the risk configuration. If you don't have an specific goal model, you can use:
- one of the OSS strategy goal models, the one fitting most with your adoption strategy, located in **goal-models/OSS Adoption Strategies**
- **OSS adoption strategy_impact**: containing the relations between the risks defined in the Activeness risk models and the goals defined in all the OSS adoption strategy models
