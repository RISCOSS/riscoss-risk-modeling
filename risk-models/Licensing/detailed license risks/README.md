The detailed license risk can be used for 2-layer configurations: 
- _Project_: in the sense of a software artifact including other software artifacts (OSS or not)
- _OSS Component_: OSS software components included in Projects

You can use these models following these steps:
1. Upload the three models in RISCOSS.
2. Create a risk configuration. E. g. you can create a risk configuration called _License Risks_.
3. Assign _detailed_license_indicators.xml_ to layer _OSS Component_. The other two should be assigned to layer _Project_.

Thats all. Now you can create several entities of type _OSS Component_; create at least one of type _Project_, containing one or more of the _OSS Component_ you have defined. Then, you will be able to create a Multi-layer analysis sessions choosing an entity of type _Project_ you have created to the risk configuration you also created previously _License Risks_.

If you want to include the impact over license related goals for the OSS adopter organization goals you also need to use the following models in the risk configuration:
- **goal-models/OSS Licenses/OSS license.istarml**: containing the OSS Adopter's goals
- **imact-models/license_impact.xml**: containing the relations between the risks defined in the _detailed_license_project.xml_ and _detailed_declining_risks.xml_ and the goals defined in the _OSS license.istarml_
