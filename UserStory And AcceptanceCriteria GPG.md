# User Stories and Acceptance Criteria GPG (Good Practice Guidance)

In Scrum we operate with “user stories” and “acceptance criteria” to ensure clear descriptions of how end-users will use a product and how a team should fulfill each criteria. 

## **User stories**
User stories are simple, one-line benefits statements of a valuable function.
A few best practices to write an effective user story:
- know and understand your user/customer/personas
- it should be written by someone who represents business users (usually the product owner)
- it should initially include brief descriptions of the "who, what, and why," but not the "how"
- it should produce a vertical slice of working code (include change to each architectural layer sufficient to deliver an increment of value)
- it should be small enough that it can be coded and tested/reviewed independently

## Template - the role-feature-reason
The role - who will benefit from this story
The feature - briefly describe what the user wants
The reason - state why the user wants this feature

## Format
User stories explain the roles of users in a system, their desired activities, and what they intend to accomplish by successfully completing a user story. 
    As a (type of user/customer), 
    I want to (perform some action) so that 
    I (can achieve some goal/result/value).

## Example
    As a publisher
    I want to login to meridian, so that
    I can view the dashboard.

## **Acceptance Criteria**
Always include acceptance criteria in every user story as that identifies what constitutes "done.”
Writing a good acceptance criteria is one of the keys to successful software delivery. Unfortunately, we often overlook or under value the importance as an aspect of the iterative planning process. By defining clear acceptance criteria upfront, we avoid surprises during development and release, leading to high levels of customer satisfaction.

Define Acceptance Criteria before development starts; write and review the criteria before implementation begins to capture the Product Owner/Customer intent rather than Development reality.

The acceptance criteria must:
- be written in simple language with no technical details
- define boundaries limits (upper and lower limits)
- say how a system should work as well as gracefully fail in negative scenarios
- reach consensus on what conditions should be met (the entire user story testable, ...) 
- ensure intended functionality clearly defined
- serve as a basis for tests 
- allow for accurate planning and estimation 

## Template - the Given-When-Then
Given a precondition/context
When some action is carried out
Then expect a particular set of observable consequences

## Format 
The Given-When-Then style is an effective way to specify criteria:
Given some precondition When I do some action Then I expect some result

## Example
    Given a publisher
    When logged into meridian with valid credential
    Then he/she is able to view the dashboard with necessary details.

    Given a non-publisher
    When trying to login to meridian
    Then a user friendly error message is displayed.

    Given a publisher
    When trying to login to meridian with wrong password
    Then a user friendly error message is displayed.