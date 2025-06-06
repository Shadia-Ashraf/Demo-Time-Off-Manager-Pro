# Time-Off Manager Pro - Test Cases

## Objective  
Create a time-off management system for employees, managers, and HR.

## Context  
This project will streamline time-off request submissions and management, improving communication and efficiency.

## Scope  
Included:
- User interface for requests
- Notification system for managers and HR
- Manager dashboard for requests
- Centralized tracking for HR
- Calendar integration for visualizing time-off

## Success Criteria
- User-friendly interface developed
- Notification system functioning
- Managers can manage requests efficiently
- User has a centralized tracking system
- Calendar feature operational

---

## Table of Contents
1. [Requirement 01.01 - View Home Page After Successful Login](#requirement-0101---view-home-page-after-successful-login)
    - Test Case 1: Validate Login with Unregistered User
    - Test Case 2: Validate Homepage Layout and Icons
    - Test Case 3: Validate Employee Login
    - Test Case 4: Validate Welcome Username Display
2. [Requirement 02 - New Request "Fields validations"](#requirement-02---new-request-fields-validations)
    - TC_001_NewRequestNavigation
    - TC_002_RequestType
    - TC_003_RequestTypeMandatory
    - TC_004_TimeOffType
    - TC_005_TimeOffTypeMandatory
    - TC_006_TimeOffTypeDropdownOptions
    - TC_007_TimeOffTypeInvalidEntry
    - TC_008_TimeOffTypeUIValidation

---

## Requirement 01.01 - View Home Page After Successful Login

### Test Case 1 - Validate Login with Unregistered User

| **Field**       | **Details**                                               |
|-----------------|-----------------------------------------------------------|
| **Test Case ID**| TC_01                                                     |
| **Title**       | Validate Login with Unregistered User                      |
| **Priority**    | High                                                      |
| **Precondition**| User does not have an account                              |
| **Test Data**   | Username: `test.employee@domain.com`<br>Password: `ValidPassword123` |
| **Steps**       | 1. Navigate to the login page.<br>2. Enter invalid credentials.<br>3. Click **Login**. |
| **Expected Result** | Error message displayed: **"User not found. Please sign up first."** |
| **Status**      | To be tested                                              |
| **Notes**       | -                                                        |

### Test Case 2 - Validate Homepage Layout and Icons

| **Field**       | **Details**                                               |
|-----------------|-----------------------------------------------------------|
| **Test Case ID**| TC_02                                                     |
| **Title**       | Validate Homepage Layout and Icons                        |
| **Priority**    | High                                                      |
| **Precondition**| User is logged in                                         |
| **Test Data**   | Valid registered user                                     |
| **Steps**       | 1. Login with valid credentials.<br>2. Observe homepage layout. |
| **Expected Result** | Elements appear:<br>- Icon: “Time-Off Manager Pro”<br>- Links: “New Request”, “My Time-Off Balance”, “Learn More”<br>- Sections: “My Time-Off”, “Current Time-Off”<br>- Table: “My Current Time-Off”<br>- Text: “Welcome [username]” at top right<br>- All links and sections clickable |
| **Status**      | To be tested                                              |
| **Notes**       | -                                                        |

### Test Case 3 - Validate Employee Login

| **Field**       | **Details**                                               |
|-----------------|-----------------------------------------------------------|
| **Test Case ID**| TC_03                                                     |
| **Title**       | Validate Employee Login                                   |
| **Priority**    | High                                                      |
| **Precondition**| Employee account exists in the system                     |
| **Test Data**   | Username: `test.employee@domain.com`<br>Password: `ValidPassword123` |
| **Steps**       | 1. Navigate to login page.<br>2. Enter valid credentials.<br>3. Click **Login**. |
| **Expected Result** | Employee redirected to homepage                        |
| **Status**      | To be tested                                              |
| **Notes**       | -                                                        |

### Test Case 4 - Validate Welcome Username Display

| **Field**       | **Details**                                               |
|-----------------|-----------------------------------------------------------|
| **Test Case ID**| TC_04                                                     |
| **Title**       | Validate Welcome Username Display                         |
| **Priority**    | Medium                                                    |
| **Precondition**| User logged in                                            |
| **Test Data**   | Username: `test.employee@domain.com`<br>Password: `ValidPassword123` |
| **Steps**       | 1. Login with valid credentials.<br>2. Observe top right corner on homepage. |
| **Expected Result** | Text: “Welcome test.employee” visible<br>Displayed name matches logged-in user |
| **Status**      | To be tested                                              |
| **Notes**       | -                                                        |

---

## Requirement 02 - New Request "Fields validations"

### TC_001_NewRequestNavigation

| **Field**       | **Details**                                               |
|-----------------|-----------------------------------------------------------|
| **Test Case ID**| TC_001                                                   |
| **Title**       | Verify navigation to "Create New Time-Off Request" page  |
| **Priority**    | High                                                      |
| **Precondition**| User logged in with valid credentials                     |
| **Test Steps**  | 1. Login with valid username and password.<br>2. Click **New Request** link on homepage. |
| **Expected Result** | User redirected to page titled “Create New Time-Off Request” |
| **Postcondition**| User lands on correct page and sees form fields          |
| **Status**      | To be tested                                              |

### TC_002_RequestType

| **Field**       | **Details**                                               |
|-----------------|-----------------------------------------------------------|
| **Test Case ID**| TC_002                                                   |
| **Title**       | Verify "Request Type" dropdown default and options       |
| **Priority**    | Medium                                                    |
| **Precondition**| User logged in and on "Create New Time-Off Request" page |
| **Test Steps**  | 1. Login.<br>2. Click **New Request**.<br>3. Check "Request Type" dropdown.<br>4. Click dropdown. |
| **Expected Result** | "Full Day" selected by default<br>"Full Day" is only option |
| **Postcondition**| Field remains set to "Full Day"                           |
| **Status**      | To be tested                                              |

### TC_003_RequestTypeMandatory

| **Field**       | **Details**                                               |
|-----------------|-----------------------------------------------------------|
| **Test Case ID**| TC_003                                                   |
| **Title**       | Verify "Request Type" field is mandatory                  |
| **Priority**    | Medium                                                    |
| **Precondition**| User logged in and on the request page                    |
| **Test Steps**  | 1. Login.<br>2. Click **New Request**.<br>3. Try to clear "Request Type". |
| **Expected Result** | Field pre-filled with "Full Day"<br>User cannot clear it<br>No error messages |
| **Postcondition**| Field always contains "Full Day"                          |
| **Status**      | To be tested                                              |

### TC_004_TimeOffType

| **Field**       | **Details**                                               |
|-----------------|-----------------------------------------------------------|
| **Test Case ID**| TC_004                                                   |
| **Title**       | Verify "Time-Off Type" dropdown default and options       |
| **Priority**    | Medium                                                    |
| **Precondition**| User logged in and on the request page                    |
| **Test Steps**  | 1. Login.<br>2. Click **New Request**.<br>3. Check "Request Type".<br>4. Open "Time-Off Type" dropdown.<br>5. Select option. |
| **Expected Result** | Dropdown empty by default<br>User can select options:<br>“Annual”, “Casual”, “Sick”, “Maternity” |
| **Postcondition**| Field shows selected value                                 |
| **Status**      | To be tested                                              |

### TC_005_TimeOffTypeMandatory

| **Field**       | **Details**                                               |
|-----------------|-----------------------------------------------------------|
| **Test Case ID**| TC_005                                                   |
| **Title**       | Verify "Time-Off Type" field is mandatory                 |
| **Priority**    | High                                                      |
| **Precondition**| User logged in and on the request page                    |
| **Test Steps**  | 1. Login.<br>2. Click **New Request**.<br>3. Leave "Time-Off Type" empty.<br>4. Submit form. |
| **Expected Result** | Error message appears under "Time-Off Type"<br>Form submission rejected until filled |
| **Postcondition**| Field stays empty or shows error until valid choice       |
| **Status**      | To be tested                                              |

### TC_006_TimeOffTypeDropdownOptions

| **Field**       | **Details**                                               |
|-----------------|-----------------------------------------------------------|
| **Test Case ID**| TC_006                                                   |
| **Title**       | Verify "Time-Off Type" dropdown contains expected options |
| **Priority**    | Medium                                                    |
| **Precondition**| User logged in and on the request page                    |
| **Test Steps**  | 1. Login.<br>2. Click **New Request**.<br>3. Open "Time-Off Type" dropdown. |
| **Expected Result** | Dropdown options:<br> - Annual<br> - Casual<br> - Sick<br> - Maternity |
| **Postcondition**| Options selectable                                         |
| **Status**      | To be tested                                              |

### TC_007_TimeOffTypeInvalidEntry

| **Field**       | **Details**                                               |
|-----------------|-----------------------------------------------------------|
| **Test Case ID**| TC_007                                                   |
| **Title**       | Verify invalid entry not accepted in "Time-Off Type"      |
| **Priority**    | High                                                      |
| **Precondition**| User logged in and on the request page                    |
| **Test Steps**  | 1. Login.<br>2. Click **New Request**.<br>3. Attempt to enter invalid text in "Time-Off Type". |
| **Expected Result** | Input rejected<br>Error message displayed                |
| **Postcondition**| User must select valid option                             |
| **Status**      | To be tested                                              |

### TC_008_TimeOffTypeUIValidation

| **Field**       | **Details**                                               |
|-----------------|-----------------------------------------------------------|
| **Test Case ID**| TC_008                                                   |
| **Title**       | Verify UI validation for "Time-Off Type" field            |
| **Priority**    | Medium                                                    |
| **Precondition**| User on "Create New Time-Off Request" page                |
| **Test Steps**  | 1. Click "Time-Off Type" dropdown.<br>2. Select option.<br>3. Check UI responsiveness. |
| **Expected Result** | Dropdown displays selected option<br>UI elements remain aligned |
| **Postcondition**| UI looks consistent                                      |
| **Status**      | To be tested                                              |

---



