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
