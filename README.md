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
	
#source:https://www.lightningdesignsystem.com/faq/

	

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

	#source:https://help.salesforce.com/articleView?id=workflow_time_action_considerations.htm&type=5

	

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
	
	
*View State Salesforce:

	#source:https://www.jitendrazaa.com/blog/salesforce/introduction-to-view-state-in-visualforce/
	
	
*Salesforce Data Security Model:
	
	#source:https://developer.salesforce.com/blogs/developer-relations/2017/04/salesforce-data-security-model-explained-visually.html
	
	
	
*What is a “Lookup Relationship”?

	-This type of relationship links two objects together,
	-Up to 25 allowed for object
	-Parent is not a required field.
	-No impact on a security and access.
	-No impact on deletion.
	-Can be multiple layers deep.
	-Lookup field is not required.
	
*What is “Master-Detail Relationship”?

	-Master Detail relationship is the Parent child relationship. In which Master represents Parent and detail represents Child.
	If Parent is deleted then Child also gets deleted.
	Rollup summary fields can only be created on Master records which will calculate the SUM, AVG, MIN of the Child records.
	-Up to 2 allowed to object.
	-Parent field on child is required.
	-Access to parent determines access to children.
	-Deleting parent automatically deletes child.
	-A child of one master detail relationship cannot be the parent of another.
	-Lookup field on page layout is required.
	
*How can I create Many – to – Many relationship?

	-We can create many – to – Many relationship by using junction object. Junction object is a custom object with two master 		detail relationships.
	
*Workflow:

	-Workflow is automated process that fired an action based on Evaluation criteria and rule criteria.
	-We can access a workflow across the object.
	-We cannot perform DML operation on workflow
	-We cannot query from database

*Trigger:

	-Trigger is a piece of code that executes before or after a record is inserted or updated.
	-We can access the trigger across the object and related to that objects
	-We can use 20 DML operations in one trigger.
	-We can use 20 SOQL’s from data base in one trigger.
	
	
*How many ways we can share a record?

	-Role Hierarchy:
	If we add a user to a role, the user is above in the role hierarchy will have read access.
	Setup -> manage users -> roles -> setup roles -> click on ‘add role’ -> provide name and save.
	
	-OWD:
	Defines the base line setting for the organization.
	Defines the level of access to the user can see the other user’s record
	OWD can be Private, Public Read Only, Public Read and Write.
	Setup -> Security Controls -> sharing settings -> Click on ‘Edit’
	
	-Manual Sharing:
	Manual Sharing is sharing a single record to single user or group of users.
	We can see this button detail page of the record and this is visible only when OWD setting is private.
	
	-Criteria Based Sharing rules:
	If we want to share records based on condition like share records to group of users
	Whose criteria are country is India.
	Setup -> security controls -> sharing settings -> select the object and provide name and
	Conditions and save
	
	-Apex sharing:
	Share object is available for every object(For Account object share object is AccountShare ). 
	If we want to share the records using apex we have to create a record to the share object.
