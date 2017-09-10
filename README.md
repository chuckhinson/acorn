# acorn

Acorn is a web application used to help manage the operation of servers in a development and test environment hosted in AWS. If you're looking for a DevOps tool that uses containers to automatically scale an application, acorn is not what you're looking for.

Note that acorn is not meant to offer an opinion on how servers should be managed for dev and test environments. Rather, acorn is meant to scratch a particular itch on a particular project, and serves primarily as a way for the author to learn about nodejs and the AWS API.

Acorn is intended to address the following needs:

* Managing hours of operation for servers. Unlike a production environment, servers in a dev and test environment do not generally need to be powered on 24x7. Some machines only need to be powered on during 'business hours' (while developers and QC are working), and some machines only need to be turned on while certain tasks are being performed).
* Allowing devs and QCs to manage servers without needing access to he AWS console. For security reasons, we want to limit the number of users who have access to the AWS console. We also want to limit the number of people who need to understand how to use the AWS console tools and understand processes and procedures for managing individual AWS resources (instances, voulmes, subnets, etc.)
* Automating various AWS-related operational tasks. Note that acorn is not intended to manage all operational tasks.
* Allowing users to create VM 'snapshots' and revert to them as needed. Due to the nature of the project, we often have the need to experiment and learn how to deploy and operate new applications and technologies. This often requires working through a non-trivial processes it is often useful to be able to snapshot the current state of server before moving on to the next step.
* Providing the ability to generate inventory reports for auditing purposes
* Providing the ability to forecast costs by combining the inventory, server configuration and operating schedule
