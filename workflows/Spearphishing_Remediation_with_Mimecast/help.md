# Description

IDR provides built-in machine learning based detections of spearphishing attempts through DNS queries to spoofed domains. On alert generation, this workflow automatically blocks a sender and creates a managed URL in Mimecast.

# Key Features

* Tag owned domains in IDR
* Alert on DNS queries to spoofed domains and create an investigation to track related alerts
* Prompt the user in Slack to either remediate or close the investigation
* Block a sender in Mimecast
* Create a managed URL to block access to it
* Notify team of all actions performed

# Requirements

* API access to Mimecast as described in the Links section below

# Documentation

## Setup

* Tag domains in IDR at #/settings/domains
* Download the workflow or clone the repository `git clone https://github.com/rapid7/insightconnet-workflows.git`
* Login to InsightConnect, and “Import” the .icon file into the workflow builder
* Configure the connections for the Mimecast plugin
* Activate your workflow
* Navigate to IDR's alert triggers page at #/automation/alerts
* Click Create Alert Trigger
* Select Spearphishing Remediation with Office365
* While Selecting Alerts, check "Spear Phishing URL Detected"

## Technical Details

* Spear Phishing URL Detected will generate an alert of type SpoofedDomainVisited
* The alert will always provide a domain, and will sometimes provide user and/or asset information

Plugins leveraged by workflow:

* Mimecast 2.5.0

## Troubleshooting

# Version History

* 1.0.1 - Updated documentation
* 1.0.0 - Initial workflow

# Links

## References

* [Mimecast API Auth](https://www.mimecast.com/tech-connect/documentation/api-overview/authentication-and-authorization/)