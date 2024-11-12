# test-case-design
writing test cases


 Test Cases for Age Restriction
 Test case design techniques such as Boundary value Analysis, Equivalence partioning, and Error guessing.
Boundary value Analysis technique:
1. Test case:   
   Description: Verify that a user below the minimum age requirement (e.g., 16 years) cannot access the account creation page.  
  Precondition: The system has a minimum age requirement of 16.  
  Test Steps:
Input: Enter a date of birth that corresponds to an age below 16 years.
   2. Attempt to access the account creation page.
  Expected Result: Access to the account creation page is denied, and an error message displays, stating that the user does not meet the minimum age requirement.

2. Test Case   
   Description: Verify that a user who meets the minimum age requirement (e.g., 16years) can access the account creation page.  
  Precondition: The system has a minimum age requirement of 16.  
  Test Steps:
   Input: Enter a date of birth that corresponds to an age of exactly 16 years.
   2. Attempt to access the account creation page.
 Expected Result: Access to the account creation page is granted, allowing the user to proceed with account creation.

3. Test Case :   
   Description: Verify that a user above the minimum age requirement can access the account creation page.  
  Precondition: The system has a minimum age requirement of 16.  
  Test Steps:
   Input: Enter a date of birth that corresponds to an age above 16years
      
  2. Attempt to access the account creation page.
  Expected Result: Access to the account creation page is granted, allowing the user to proceed with account creation.

ERROR GUESSING TECHNIQUE:

4.Test Case  
   Description: Verify that an error message displays when a user enters an invalid date of birth format.  
   Precondition: The account creation page accepts a valid date format.  
 Test Steps:
   Input: Enter an invalid date format (e.g., "32/13/2005").
   2. Attempt to access the account creation page.
   Expected Result: An error message displays, prompting the user to enter a valid date.

5.Test Case 
Description: Verify that a user is blocked from account access if their date of birth was altered to bypass age restrictions.  
  Precondition: System records the user's date of birth on initial input.  
  Test Steps:
  Input: Enter a date of birth that meets the minimum age requirement initially.
   2. Attempt to alter the date of birth to a date below the minimum age.
   Expected Result: The system prevents the account access, displaying a message indicating age restrictions.

6.Test Case 
  Description: Verify that the system logs an event when a user attempts to bypass age restrictions.  
  Precondition: System logging is enabled for age-related access attempts.  
 Test Steps
  Input: Enter a date of birth below the minimum age requirement.
   2. Attempt to access the account creation page.
   Expected Result: The system logs an event recording the access attempt by an underage user.

7.Test Case 
  Description: Verify that age restriction validation persists across different devices and sessions.  
 Precondition: Account age restriction implemented across sessions.  
 Test Step:
   1. On Device A, enter a date of birth below the minimum age requirement.
   2. Attempt to access the account creation page.
   3. On Device B, repeat the above steps.
  Expected Result: Access to the account creation page is denied on both devices, with an error message stating the user does not meet the age requirement.
