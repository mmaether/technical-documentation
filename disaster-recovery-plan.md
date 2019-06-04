# Disaster Recovery Plan

## Purpose

The purpose of this policy is to establish a baseline disaster recovery plan for minimizing risks associated with potential disasters. This policy establishes a process for recovery should a disaster occur that may cause significant outages.

## Scope
This policy is applicable to all Company employees and governed by management who are responsible for the development, testing, implementation, and continuous review. 

## Policy
Company shall identify potential disasters and create plans of action that cover the behavior of Company during and potentially following disaster. This policy will identify the roles of who shall initiate the implementation of the plans. Company shall review the current state of each plan quarterly. It shall conduct semi-annual practice scenarios to test adherence and effectiveness of implementation.

| Disaster | Plan of Action | Implementer |
|--------- | -------------- | ----------- |
| Power Failure | Install UPC power supplies for mission critical devices. | Programming Department | 
| Internet Failure | Fall back to wireless hotspots within the office. | Programming Department | 
| Environmental Disaster / Hazardous Weather | Require personnel to remote into the office from a safe location. | Human Resources Department | 
| Social Engineering Attack | Enact the Social Engineering Plan. | Programming Department, Legal |
| Office Cyber Attack | Enact Office Cyber Security Plan. | Programming Department |
| Company Software Cyber Attack | Enact the Cyber Response Plan. | Programming Department |
| Data Center Outage | Inform client support of the outage issue. Acknowledge the issue on social media if the outage persists. | Client Support Department, Marketing Department | 
| Workplace Violence / Theft | Follow the Handbook. | Human Resources Department |
| Inavailability of Key Personnel | Follow individual department's contingency plan. | Individual Departments |
| Third-Party System Compromise | Alert clients if data was exposed. | Client Support Department |

## Social Engineering Plan

- Gather a list of all actions taken prior to the attack being discovered.
- Alert effected department heads about actions that have occurred.
- Research how the attacker may have gained information to make the attack possible.
    - Post-disaster review policies for potential updates to close these down.
- Potentially pursue legal action.

## Office Cyber Security Plan

- Disconnect infected device from the office internet.
- Update firewall rules.
- Securely transfer anti-virus and operating system updates onto device.
- Run thorough anti-virus scan.
- Post-disaster review policies, or adherence to policies, to make necessary updates to prevent attack from re-occurring.

## Cyber Response Plan

- Gather a list of all actions that were taken prior to the attack being discovered.
- Alert effected department heads about actions that have occurred.
- Put the site into maintenance mode to prevent clients from exposure to infected site.
- Update firewall rules to block the IP address(es) of attacker(s).
- Replace infected files with a clean version of the files by replacing the server with an untainted cloud image, or updating the files if there is no clean image.
    - Take a new image that is used for new cloud instances if there is no untainted image.
- Take the site out of maintenance mode.
- Post-disaster review how the attack became possible. Apply security updates if they were lacking, or update custom code to remove vulnerability.
