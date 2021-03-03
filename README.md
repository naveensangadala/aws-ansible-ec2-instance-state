Ansible playbook to Change the state (start,stop,restart,terminate etc..) of an AWS EC2 instance
------------------------------------------------------------------------------------------------
By using this ansible playbook we can change the status of a Ec2 instance in AWS, it will gather all the facts based on the availability zone and the tag value for the ec2 instance and then it will perform the requested action.

Playbook Execution:
-------------------

Actions can be performed by issuing the below commands from ansible controller 

To 'Stop' the Ec2 instance:

ansible-playbook aws-ec2-instance-status-change.yml --extra-vars "value=test-ec2 status_change=stopped"

To 'Start' the Ec2 instance:

ansible-playbook aws-ec2-instance-status-change.yml --extra-vars "value=test-ec2 status_change=running"

To 'Restart' the Ec2 instance:

ansible-playbook aws-ec2-instance-status-change.yml --extra-vars "value=test-ec2 status_change=restarted"

To 'Terminate' the Ec2 instance:

ansible-playbook aws-ec2-instance-status-change.yml --extra-vars "value=test-ec2 status_change=absent"

