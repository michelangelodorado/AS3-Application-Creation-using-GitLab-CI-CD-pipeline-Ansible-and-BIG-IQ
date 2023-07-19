# AS3-Application-Creation-using-GitLab-CI-CD-pipeline-Ansible-and-BIG-IQ

We are going to use GitLab to store the BIG-IP configuration (AS3 declaration) and deploy it through BIG-IQ to BIG-IP using Ansible.

![image](https://github.com/michelangelodorado/AS3-Application-Creation-using-GitLab-CI-CD-pipeline-Ansible-and-BIG-IQ/assets/102953584/814ea63f-d593-48b8-8127-6adc732dbd4a)

GitLab will keep track of the changes and control user access to the application service configuration of the F5 BIG-IP. We are using BIG-IQ to provide visibility with enhanced analytics (HTTP/TCP) to the DevOps/Application owner.

This lab will be using the following F5 Ansible Galaxy roles:
- atc_deploy ansible Role: Allows AS3 declaration to be sent to automation tool chain service.
- bigiq_move_app_dashboard ansible Role: Move Application Service(s) in BIG-IQ Application Dashboard.

1. Connect via SSH or Web Shell to the system Ubuntu Lamp Server.
2. Execute the following commands:
```sh
./gitlab/start-gitlab.sh
```
3. Wait ~10 min to open GitLab web UI from the lab environment. Click on the ACCESS button of the Ubuntu Lamp Server system and click on GitLab. The login/password is root/purple123. Or open http://localhost:7002 from Google Chrome browser in the Jumphost.
>> **Note**
>> You can check GitLab status with docker exec gitlab_gitlab_1 gitlab-ctl status and GitLab logs with docker logs gitlab_gitlab_1.
