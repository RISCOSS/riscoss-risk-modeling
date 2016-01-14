The detailed license risk can be used for 2-layer configurations: 
- Project: in the sense of a software artifact including other software artifacts (OSS or not)
- OSS Component: OSS software components included in Projects

You can use these models following these steps:
1) Upload the three models in RISCOSS.
2) Create a risk configuration. E. g. you can create a risk configuration called 'License Risks'.
3) Assign detailed_license_indicators.xml to layer OSS Component. The other two should be assigned to layer Project.

Thats all. Now you can create several entities of type 'OSS Component'; create at least one of type 'Project', containing one or more of the 'OSS Component' you have defined. Then, you will be able to create a Multi-layer analysis sessions choosing an entity of type 'Project' you have created to the risk configuration you also created previously 'License Risks'.

If you want to include the impact over license related goals for the OSS adopter organization goals you also need to use the following models in the risk configuration:
- goal-models/OSS Licenses/OSS license.istarml: containing the OSS Adopter's goals
- imact-models/license_impact.xml: containing the relations between the risks defined in the detailed_license_project.xml and detailed_declining_risks.xml and the goals defined in the OSS license.istarml
