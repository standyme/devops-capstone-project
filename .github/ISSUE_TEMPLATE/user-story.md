**As a** registered user  
**I need** the ability to reset my password  
**So that** I can regain access to my account if I forget it  

### Details and Assumptions
* The user must be registered with a valid email address  
* The reset link should expire after 24 hours  
* The reset process should include email verification  
* Security measures should be in place to prevent abuse  

### Acceptance Criteria     
```gherkin
Given I am on the login page  
When I click on "Forgot Password" and enter my registered email  
Then I should receive a password reset link via email  

Given I received the reset link  
When I click the link within 24 hours  
Then I should be taken to a secure page to enter a new password  

Given I entered a new valid password  
When I confirm the new password  
Then my password should be updated and I should see a confirmation message  
