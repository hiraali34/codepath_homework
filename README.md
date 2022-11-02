# Honeypot Assignment

**Time spent:** 2:00 hours spent in total

**Objective:** Create a honeynet using MHN-Admin. Present your findings as if you were requested to give a brief report of the current state of Internet security. Assume that your audience is a current employer who is questioning why the company should allocate anymore resources to the IT security team.

### MHN-Admin Deployment (Required)

**Summary:** How did you deploy it? Did you use GCP, AWS, Azure, Vagrant, VirtualBox, etc.?
I used GCP to deploy my VM

![](installing honeypot.gif)

.
### Dionaea Honeypot Deployment (Required)

**Summary:** Briefly in your own words, what does dionaea do?
It is the Honeypot that is used for attacks, and tracks the attacks

![](honeypot.gif)


### Database Backup (Required) 

**Summary:** What is the RDBMS that MHN-Admin uses? What information does the exported JSON file record?
Mongoexpert db is used for MHN-admin, it is being used to store the attack record.
![](json.gif)


*Be sure to upload session.json directly to this GitHub repo/branch in order to get full credit.*



## Notes

Describe any challenges encountered while doing the assignment.
