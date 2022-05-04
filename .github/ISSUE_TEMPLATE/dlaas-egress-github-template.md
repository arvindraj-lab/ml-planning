---
name: WML Custom Egress template
about: Template for IBM Support to request custom WML egress policies for customers
title: WML customer egress request for [WML INSTANCE ID]
labels: WML-devOps
assignees: krishnamurthy-a, otucker, pvanrun

---

# Watson Machine Learning - Deep Learning Custom Egress Request

Upon request WML customers can ask to have their training and scoring processes blocked from outbound access (egress) to the internet for security purposes. They can do so by submitting a request to IBM Support. This is documented in the WML public cloud documentation.

---

## For IBM Support to fill in:

Please supply the following:

- Customer name:
- WML Instance ID:

### Select the WML location

- [ ] Dallas
- [ ] London
- [ ] Frankfurt 
- [ ] Tokyo

### White list selection

Select any (zero or more) of the following white lists:

  - [ ] IBM COS
  - [ ] Python repo's and related locations
  - [ ] AWS S3
  - [ ] Github
  - [ ] IBM PostgresSQL

### Custom IP locations

In addition the customer can provide their own list of a maximum of 25 customer
specific IPs, provided in cidr `999.999.999.999/99` format. Only IP's or IP
ranges are accepted, WML cannot deal with domain names.

e.g.
```
       129.42.38.10/32     # ibm.com
       10.1.129.00/24      # range of private IBM COS locations, using first 3 octets only
```
Provide the required IP addresses here, 25 max. :

```
       999:999:999:999/99     # domain name (if available)
       999:999:999:999/99     # domain name (if available)
       999:999:999:999/99     # domain name (if available)
       999:999:999:999/99     # domain name (if available)
       999:999:999:999/99     # domain name (if available)
       ...
```

### Desired Target Deployment Date
- < MM-DD-YYYY >

---

### Deployment logs
(Added as a seperate comment -- not in description)
- < copy of Deployment Logs for each cluster >

### Backout logs (if applicable)
(Added as a seperate comment -- not in description)
- < Backout Logs for each cluster (if applicable) >

### Approvals
(Added as a seperate comment -- not in description)
- Dev representative **->** <Add comment stating "I have reviewed and I approve for Dev.">
- QA representative **->** <Add comment stating "I have reviewed and I approve for QA.">
- DevOps representative **->** <Add comment stating "I have reviewed and I approve for DevOps.">
