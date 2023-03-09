# System Test Specification <!-- omit in toc -->

- [System Requirements](#system-requirements)
  - [For participants](#for-participants)
  - [For administrators](#for-administrators)
- [Requirement Traceability Matrix](#requirement-traceability-matrix)
- [Test Case Specifications](#test-case-specifications)
  - [T0 (Template)](#t0-template)
  - [T1.1](#t11)

## System Requirements

### For participants

> R1: Secure and private authentication  
R2: Reset password  
R3: Interactive "my story" timeline  
R4: Observe their own information  
R5: Compare with aggregated information  
R6: Exporting Views  
R7: Annotation and commenting  

### For administrators

> R8: Secure and private authentication  
R9: Reset password  
R10: Participant request management  
R11: Suspend/removal of participant accounts  
R12: Reset password of participant  
R13: Account control of other administrators  
R14: Upload data  
R15: View participants' session info  

## Requirement Traceability Matrix

| Req. ID | Test Case ID | Test Scenario | Test Status | Manual/Automated | Last Exexution Date | Last Execution Result |
| ------- | ------------ | ------------- | ----------- | ---------------- | ------------------- | ---------------- |
| R1 | [T1.1](#t11) | Login with valid credentials (as participant) | Complete | Automated | 2/27/2023 | Pass |
| R8 | [T8.1](#T8.1) | Login with valid credentials (as administrator) | Complete | Automated | 2/27/2023 | Pass |
| R1 | [T1.2](#T1.2) | Login with invalid credentials (as participant) | Complete | Automated | 2/27/2023 | Pass |
| R8 | [T8.2](#T8.2) | Login with invalid credentials (as administrator) | Complete | Both | 2/27/2023 | Pass |
| R1 | [T1.3](#T1.3) | Logout (as participant) | Complete | Automated | 2/27/2023 | Pass |
| R8 | [T8.3](#T8.3) | Logout (as administrator) | Complete | Automated | 2/27/2023 | Pass |
| R1, R8 | [T1.4](#T1.4) | Persistent session | Complete | Manual | 2/27/2023 | Pass |
| R1, R8 | [T1.5](#T1.5) | Two-factor authentication | Incomplete | N/A | N/A | N/A |
| R1 | [T1.21](#T1.21) | Potential participant requests an account with valid participant ID format | Complete | Both | N/A | N/A |
| R1 | [T1.22](#T1.22) | Potential participant requests an account with invalid participant ID format | Complete | Both | N/A | N/A |
| R1, R8 | [T1.25](#T1.25) | Participant cannot access administrator page | Complete | Both | N/A | N/A |
| R1, R8 | [T1.26](#T1.26) | Administrator cannot access participant page | Complete | Both | N/A | N/A |
| R1, R2, R8, R9 | [T2.1](#T2.1) | After reset password, the password is updated in the database | Complete | Manual | 2/12/2023 | Pass |
| R2 | [T2.2](#T2.2) | Receive email for resetting password (as participant) | Complete | Automated | 2/11/2023 | Pass |
| R9 | [T9.1](#T9.1) | Receive email for resetting password (as administrator) | Complete | Automated | 2/11/2023 | Pass |
| R1, R2 | [T2.3](#T2.3) | Login with new password (as participant) | Complete | Automated | 2/11/2023 | Pass |
| R8, R9 | [T9.2](#T9.2) | Login with new password (as administrator) | Complete | Automated | 2/11/2023 | Pass |
| R2, R9 | [T2.5](#T2.5) | Reset password with invalid email | Complete | Automated | 2/11/2023 | Pass |
| R10 | [T10.1](#T10.1) | Administrator view pending requests | Complete | Automated | - | - |
| R10 | [T10.2](#T10.2) | Administrator reject pending request | Complete | Automated | - | - |
| R1, R10 | [T10.3](#T10.3) | Administrator accept pending request | Incomplete | - | - | - |
| R12 | [T12.1](#T12.1) | Administrator invite new administrator with valid email format | Complete | Both | 2/27/2023 | Pass |
| R12 | [T12.2](#T12.2) | Administrator invite new administrator with invalid email format | Complete | Both | 2/27/2023 | Fail |
| R12 | [T12.3](#T12.3) | Administrator invite existing user (participant or administrator) as Administrator | Complete | Both | 2/27/2023 | Fail |
| R8, R12 | [T12.4](#T12.4) | New administrator login with provided credentials | Complete | Both | 2/27/2023 | Pass |
| R8, R12 | [T12.5](#T12.5) | New administrator login click link in invitation email | Complete | Both | 2/27/2023 | Pass |
| R8, R12 | [T12.6](#T12.6) | New administrator invite other administrator | Incomplete | - | - | - |

## Test Case Specifications

---
### T0 (Template)

Status (Waiting for feature/Pass/Fail): __Pass__  

Last Updated by: __John Doe__  

Cypress e2e test (if automated): `./cypress/e2e/a-test.ts`

| Step # | Step Details | Additional Information |
| ------ | ------------ | ---------------------- |
| 1 | - | - |

---
### T1.1

Status (Waiting for feature/Pass/Fail): __Pass__  

Last Updated by: __Mohamed Bensaleh__  

Cypress e2e test (if automated): `./cypress/e2e/a-test.ts`

| Step # | Step Details | Expected Results | Actual Result | Additional Information |
| ------ | ------------ | ---------------- | ------------- | ---------------------- |
| 1 | Participant navigates to login page | Participant presented with email and password fields | As expected | - |
| 2 | Participant enters their email address and password | Correct email and password will show up in the input fields | As expected | - |
| 3 | Participant submits login form | Successful authentication and authorization. Redirects to index/root page for participants | As expected | - |

---
