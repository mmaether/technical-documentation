# Operations and Security

## Data Center
All production services are hosted on Amazon Web Services (AWS). Company implements numerous AWS services including, but not limited to, EC2, RDS, S3, and Glacier.

Company has separate and distinct production, staging, and development environments. Customer data is not to be replicated outside of the production environment and is not to be replicated onto employee workstations. Because of this, Company relies on AWS for physical security compliance. Information on the security of AWS EC2 data centers is available directly from Amazon.

All user content is stored within US regions of AWS. The production environment is hosted on an AWS EC2 platform, and user content is stored in EC2, S3, and Glacier. We currently do not offer the option of hosting service on a private server.

## Access Control

All customer data is considered highly sensitive and protected and access is least privilege. Only authorized and trained members of the Company team have direct access to production systems and user data. Those who do have direct access to data are only permitted to view it in aggregate or for troubleshooting purposes. User data is only viewed by Company employees for troubleshooting purposes when consent has expressly been provided ahead of time by the account owner or team administrator.

The information access provided to Company personnel should be aligned with each individual's job functions and duties. For example, the Programming team, tasked with developing updates, improvements, and expansions to the functionality of the Learning Management System, requires access to the databases used by the LMS.

Unless specifically authorized by Company management, sensitive Company data is not to be removed or transferred from Company premises, whether in hardcopy form, over the Internet, or on Company-owned or personal devices or media.

## Backup Policy

Data entered into service is backed up regularly. All backups are encrypted and stored at multiple offsite locations to ensure that they are available in the unlikely event that a restore is necessary. All backups are retained on the following schedule and at the following locations:

- AWS EC2 snapshots are taken at 3am each day and stored for 90 days.
- AWS S3 follow Amazon's internal redundancy mechanism with versioning.
- RDS snapshots are taken daily and are saved for 30 days.
- Only authorized members of the Company team has access to the backup locations, so that they are able to monitor the performance of the backup processes, and in the very unlikely event that a restore becomes necessary.

## Data Portability

All training records can be exported as CSV files within the service site. Learners have the ability to export transcripts and their individual course records, while admins have the ability to export the entirety of the training records via the reporting pages.

## Incidents and Response

A Company problem customers encounter will be assigned a Severity Level and handled according to the resolutions in the table below.

| Level | Description | Resolution | Examples |
| ----- | ----------- | ---------- | -------- |
| Severity 1 | service is not available or is unusable. | Work beings within 1 hour from report, temporary solution within 4 hours, and final resolution within 7 hours. | The site is not responding. |
|Severity 2 | Service or performance is substantially degraded in a way that prevents normal use. | Work begins within 2 hours from report, temporary resolution within 48 hours, final resolution within 14 days. | Courses can't be assigned by administrators. |
| Severity 3 | A service not essential to main functionality is unavailable or degraded. | Work begins within 72 hours from report, temporary resolution within 7 days, final resolution within 30 days. |The search in Reporting does not display results for Additional Training records. |
| Severity 4 | Minor or cosmetic issues, and all feature requests. | Resolution at Company team's discretion | Icons are appearing in the wrong color. A feature request for adding more details in reporting. |

## Availability
We work to keep service available 100% of the time, and we've experienced 99.97% uptime in 2017. service's availability is published in real-time at the Company Status page, where you can also find our incident history.

## Planned Maintenance

When it is necessary to perform planned maintenance on our services, Company will perform the work during planned scheduled maintenance windows. We will make reasonable efforts to announce maintenance procedures that could potentially impact users on the Company Status page at least 24 hours prior to the event.

## Unplanned Maintenance

Due to unforeseen events, we may have to infrequently perform unplanned maintenance. This maintenance might cause some or all of the services to be inaccessible by our users for a period of time. It is our goal to do this as infrequently as possible. Any unplanned or emergency maintenance will be announced on the Company Status page. As with planned maintenance, we do our best to minimize disruption caused by service outages.

## Legal and Privacy
Our Terms & Conditions and Privacy Policy outline what you agree to when using service, and the procedures we take to ensure that your information is handled responsibly and in accordance with applicable data protection and privacy laws.
