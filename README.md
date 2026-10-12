# SOAR-EDR Automation Lab

## Objective

The objective of this project was to build a Security Orchestration, Automation, and Response (SOAR) workflow that integrates endpoint detection data from LimaCharlie EDR with Tines.

The workflow receives security detections, sends notifications, presents an analyst with a decision to isolate the affected endpoint, and then performs the appropriate response action.

---

## Skills Demonstrated

- SOAR workflow development
- EDR integration
- Security automation
- Incident response
- Webhook configuration
- REST API integration
- HTTP requests
- JSON event processing
- Conditional logic
- API authentication
- Slack integration
- Email notification
- Endpoint isolation
- Troubleshooting API and workflow errors

---

## Technologies Used

- Tines SOAR
- LimaCharlie EDR
- Slack
- Gmail / Email
- Windows 11 endpoint
- REST APIs
- Webhooks
- JSON
- HTTP requests

---

## Lab Workflow

The workflow follows this general process:

1. LimaCharlie detects suspicious activity on an endpoint.
2. Detection data is sent to Tines.
3. Tines sends notifications through Slack and email.
4. A User Prompt asks the analyst whether the affected endpoint should be isolated.
5. The analyst selects Yes or No.
6. Tines evaluates the response using conditional logic.
7. If Yes is selected, Tines sends an authenticated request to LimaCharlie to isolate the endpoint.
8. If No is selected, Tines sends a Slack message confirming that isolation was not performed.

<img width="731" height="701" alt="Fig 1 Workflow Diagram" src="https://github.com/user-attachments/assets/ca54d1af-48df-441c-a53e-fe016553b440" />

*Figure 1: Workflow Diagram*
<br>
The lab environment consists of a Windows endpoint monitored by LimaCharlie EDR, Tines SOAR for workflow automation, and Slack and email for analyst notifications.

<br>
<img width="1908" height="865" alt="Fig 2 Tines Detection" src="https://github.com/user-attachments/assets/c33bc099-5e13-461e-b673-7a849ec60d36" />

*Figure 2: LimaCharlie Endpoint Telemetry*
<br>
LimaCharlie displays process, network, and system activity collected from the Windows target endpoint.

<br>
<img width="1388" height="660" alt="Fig 3 Slack Detection Alert" src="https://github.com/user-attachments/assets/ac94d490-507b-4ca2-92be-c9551e439980" />

*Figure 3: Slack Detection Alert*
<br>
Tines sends an automated Slack notification containing key detection and endpoint details received from LimaCharlie.

<br>
<img width="1511" height="418" alt="Fig 4 Email Detection Alert" src="https://github.com/user-attachments/assets/82d751b2-879f-4824-b92b-2c211353a4bb" />

*Figure 4: Email Detection Alert*
<br>
Tines sends an automated email containing the same key detection details from LimaCharlie for analyst review and incident notification.

<br>
<img width="553" height="484" alt="Fig 5 User Prompt" src="https://github.com/user-attachments/assets/c2317d2e-2d8c-4ebe-b7a1-3f9a58f0ed23" />

*Figure 5: Analyst Isolation Prompt*
<br>
The Tines User Prompt presents the detection details to the analyst and provides a Yes or No decision to determine whether the affected endpoint should be isolated.

<br>
<img width="1324" height="578" alt="Fig 6 No Isolation Response" src="https://github.com/user-attachments/assets/c7b24562-1bd9-494f-aa99-7a9c6afee5d6" />

*Figure 6: No Isolation Response*
<br>
After the analyst selects No in the Tines User Prompt, the workflow sends a Slack notification and email confirming that the endpoint was not isolated.

<br>
<img width="480" height="247" alt="Fig 7 Endpoint Isolation Email" src="https://github.com/user-attachments/assets/d80bda13-508d-4e41-881d-8375ba585daa" />

*Figure 7: Endpoint Isolation Confirmation*
<br>
After the analyst selects Yes, Tines sends the isolation request to LimaCharlie and notifies the analyst that the endpoint was successfully isolated.

<br>
<img width="618" height="634" alt="Fig 8 Network Isolation Verification" src="https://github.com/user-attachments/assets/22e13f59-5777-40f3-bed4-66d7b2489778" />

*Figure 8: Network Isolation Verification*
<br>
Command Prompt confirms successful network connectivity before isolation and repeated general failures after the endpoint is isolated

<br>
<img width="1548" height="454" alt="Fig 9 Endpoint Isolation Status" src="https://github.com/user-attachments/assets/585c0caf-1ded-4772-ba13-a55f8b8dddad" />

<br>
LimaCharlie confirms the Windows endpoint is isolated following the analyst-approved containment action.

