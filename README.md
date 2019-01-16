# SF-Objective-samples

*What are the different ways to make a field as mandatory in salesforce?

	Different ways to make field mandatory :

		1.	Make the field “Required” at the time of field creation by checking the “Required” check box.

		2.	Make the field Required through Page Layout by checking the “Required ” checkbook in Field Properties.

		3.	Validation Rules can also be used to make the field mandatory. In Error Condition Formula, one can use ISBLANK(“FieldName”);

		4.	Triggers can be used to make field mandatory. Ex. If a user try to insert the record without the field which is required,

    		we can throw the page massage specifying to fill up required fields.(Using Trigger.addError()).

		5.	One can make field mandatory through Visualforce.

    		(If the field is getting referenced) by setting the required attribute in <apex:inoutField> to True.





*can we edit active process from process builder  ?

	process is created, defined the criteria, and added our immediate process actions, 

	it needs to be activated in order to evaluate new Trip Request records. 

	After you activate a process, you can no longer edit that process. 

	However, you can click Clone to save the process as a new inactive process.





*Record Id should be unique, it can never be changed even if record is deleted and then undeleted. it can be set to primary and not         null.



*SLDS supported browsers:

	-Google Chrome(Latest)

	-Mozilla Firefox(Latest)

	-Safari(Latest)

	-Microsoft Edge(Latest)

	-Internet Explorer(V11)

	

*Adding slds to visualforce page:

	two ways:

		1-add <apex:slds/> in page tag and wrap code in container <div class="slds-scope">......</div>

		2-create CSS file with custom scoped outer wrapper.

	

*Dynamic dashboards cannot be scheduled, it has to be scheduled manually.



*Sharing rules:

	-gives particular user greater access by making automatic exceptions to OWD sharing setting.

	-upto 300 rules with 50 criteria based sharing rules.

	-OWD is baseline level of access for each object

	-can have both vertical and horizontal access

	

*Custom Controller:

	-Apex class that implements all logic for a page without leveraging std controller

	-used when you want your vfpage to run entirely in system mode,

	 which does not enforce the perssions and field level security of a current user.

	

*Controller Extension:

	-Apex class that extends functionality of a existing std/custom controller.

	-can be used when:

					-leveraging builtin functionality of std controller but overriding  basic actions(save,edit,delete).

					-adding new actions

					-build vfpage that respects user permissions

					

*Salesforce API: flexibility to manipulate data however you want

		-REST

		-SOAP

		-BULK

		-Streaming



*Pass:

	-proven model for running appications without the hassle of maintaining on-premises H/W and S/W infrastructure at ur organization.

	-applications have latest features without pain of constant updates.

	-pass solutions-SF for simplicity,reliability,scalability.

	-provides huge benefits for companies adopting microservices architecture.

	-provides all the infrastructure needed to develope and run applications over internet.

	-allows microservices to be deployed and managed faster.

	

*Types of Lightning pages:

	-App page(Mobile and lightning experience)-only global actions will be achieved

	-Home page(Relevant to specific types of users/profiles)

	-Record page(Customized version of an object's record page)



*Sequence:

	-fire event

	-capture phase

	-bubble phase

	

*Roll-Up Summary Field:

	-A roll-up summary field calculates values from related records, such as those in a related list. You can create a roll-up summary 		field to display a value in a master record based on the values of fields in a detail record.

	

*Time-Triggered approval process:

	https://help.salesforce.com/articleView?id=workflow_time_action_considerations.htm&type=5

	

*Approval Process:

	-total no of approval process(1000)

	-process/object(300)

	-steps/process(30)

	-approvers(25)

	-initial submission actions(40)

	-final approval actions(40)

	-final rejection actions(40)

	





*Dashboards:

	-20 components per dashboard

	-3 filters per dashboard

	-3 dynamic dashboards/org(Developer)

	-5 dynamic dashboards/org(Enterprise)
