Meetings are held weekly, on Tuesdays at [9am PT / 12pm ET / 9:30pm SLT](https://www.worldtimeserver.com/meeting-planner-times.aspx?&L0=US-OR&Day=14&Mon=8&Y=2018&L1=US-MD&L2=LK&L3=&L4=&L5=&L6=&L7=).
Anyone is welcome to join. Unless posted differently in the [FederatedGalaxy
Gitter channel](https://gitter.im/galaxyproject/FederatedGalaxy?utm_source=share-link&utm_medium=link&utm_campaign=share-link), we'll use the following meeting URL:
https://zoom.us/j/3980033400.

## 2019-04-02
- Enable rolling updates for celery (preStop signal currently not working as expected: https://github.com/CloudVE/cloudlaunch-helm/blob/a021bc809da17c2c3707a618f84adfe5d8075ab7/cloudlaunch-server/templates/cl-celery-deployment.yaml#L37)
- Better way to handle vm_default_username for GCP and Azure. Store with image?
- Rancher and Keycloak integration (https://149.165.157.181:4430)
- CloudBridge OpenStack issue: networking and compute resources in different zones
- AWS Instance Types by Zone (https://github.com/CloudVE/aws-instance-types/commits/master)
- Helm chart and Postgress connectivity
- Reinstallation of CloudLaunch 
- Status of the Custos integration PR: https://github.com/galaxyproject/galaxy/pull/7195
- Milestones for the upcoming week

## 2019-03-26
- Rancher and Keycloak integration (https://149.165.157.181:4430)
- CloudBridge OpenStack issue: networking and compute resources in different zones
- AWS Instance Types by Zone (https://github.com/CloudVE/aws-instance-types/commits/master)
- Helm chart and Postgress connectivity
- Reinstallation of CloudLaunch 
- Status of the Custos integration PR: https://github.com/galaxyproject/galaxy/pull/7195
- Milestones for the upcoming week

## 2019-03-12
- Update on Enis's sailing adventure
- Updates on CloudLaunch changes and CloudBridge v2
- CloudMan upgrade to Rancher 2.2
- CloudMan scaling
- ConfigMaps handling for Galaxy Chart
- Follow up on Galaxy Docker image with tools
- NFS & CVMFS CSI integration w/ K8S

## 2019-03-05
- Demo cross-cloud job dispatcher 
- Updates on CloudLaunch changes and CloudBridge v2
- CloudMan upgrade to Rancher 2.2
- CloudMan scaling
- ConfigMaps handling for Galaxy Chart
- Follow up on Galaxy Docker image with tools
- NFS & CVMFS CSI integration w/ K8S
- Blocking issues and how to proceed


## 2019-02-25
- [@almahmoud, @nuwang] Finalize CloudBridge v2 release, preceeded with the necessary CloudLaunch++ updates
- [@ic4f] Upgrade CloudMan 2.0 charts to latest ([Rancher 2.2?](https://github.com/rancher/rancher/releases) (set [here](https://github.com/CloudVE/cloudman-boot/blob/b340ee7947af6deaaea66cce9cea93127cca5c9d/providers/other/vars/other_vars.yml)), [Keycloak 4.8?](https://github.com/keycloak/keycloak/releases)). Chart versions are mostly set [in this file](https://github.com/CloudVE/cloudman-helm/blob/master/cloudman/requirements.yaml). Enable Keycloak login support in Rancher.
- [@nuwang] CloudMan scaling
- [@ic4f] ConfigMaps for all Galaxy config files
- Galaxy Docker image with tools ([related PR?](https://github.com/galaxyproject/galaxy/pull/7316)) + exec jobs in K8S via the K8S job runner
  - Try https://github.com/galaxyproject/galaxy/pull/7316 from within the Minimal Container
  - Sync w/ John about the status and plans re. the [3-part job execution on K8S ](https://docs.google.com/presentation/d/1TaWmxet80B0REDGYFL3z4GBDmANtr1j_uFvZMIkrBF0/edit)
  - See what the current Galaxy Docker/Helm is doing
- Implement multi-part object store uploads in CloudBridge (push to Q2/2019)
- [@vjalili] NFS & CVMFS CSI integration w/ K8S ([tracking issue](https://github.com/galaxyproject/galaxy-kubernetes/issues/31)) (+ environment modules integration)

## 2019-02-19
- CloudBridge
  - Progress update: [remaining issues](https://github.com/CloudVE/cloudbridge/issues?q=is%3Aopen+is%3Aissue+milestone%3A%22release+2.0.0%22), impact on CloudLaunch
    - [Zone decision](https://docs.google.com/spreadsheets/d/1wuM-JKtskSwHTAXmtU4o1rFy8SqE_MHBMGDPTPu2bh8/edit#gid=1938807527)
  - Release plans
- Minimal Galaxy Docker image
  - [Avoiding Ansible?](https://github.com/ic4f/galaxy-kube-playbook/tree/no-ansible)
  - Initial Kubernetes manifests
- ITCR project update following the kickoff meeting

## 2019-02-12
- Coding standards:
  - Unless it's an interface method with an existing docstring, a method must have a docstring, including a description of each parameter
  - Continuously passing tests
- CloudBridge 
  - Optional dependencies (xref: https://github.com/galaxyproject/galaxy/issues/7320)
  - Use of generic project metadata for key pairs vs. ssh-keys metadata
  - Review the [remaining CloudBridge 2.0 issues](https://github.com/CloudVE/cloudbridge/issues?q=is%3Aopen+is%3Aissue+milestone%3A%22release+2.0.0%22)
- Status of the [minimal Galaxy Docker container](https://github.com/CloudVE/galaxy-kube-playbook)

## 2019-02-05
- Towards CloudBridge 2.0 release: [remaining issues](https://github.com/CloudVE/cloudbridge/issues?q=is%3Aopen+is%3Aissue+milestone%3A%22release+2.0.0%22)
- Next steps for the minimal Galaxy image

## 2019-01-29
- CloudBridge GCE provider update
- Need to update CloudLaunch server to include fix for https://github.com/CloudVE/cloudbridge/issues/167
- Galaxy & Keycloak integration PR https://github.com/galaxyproject/galaxy/pull/7195
- Progress on the [minimal Galaxy Docker container](https://github.com/CloudVE/galaxy-kube-playbook) & plans

## 2019-01-22
- CloudBridge 
  - Naming issues (on OpenStack at least), [#167](https://github.com/CloudVE/cloudbridge/issues/167)
  - Status of GCE support, including [key pair ID issue](https://github.com/CloudVE/cloudbridge/pull/114/commits/f981ed9c123bea6a25d312b6afb03210b7ed9c97#r249219848)
  - BucketObjectService, EventDispatcher; can we clean up some of the branches?
  - Colabfest update
- Galaxy Admin Training instance [launch script](https://github.com/almahmoud/cloudbridge-demo-loop) & support
- Progress on the [minimal Galaxy Docker container](https://github.com/CloudVE/galaxy-kube-playbook)
- Implications of the [Galaxy login PR](https://github.com/galaxyproject/galaxy/pull/7047) having been merged

## 2019-01-15
- GalaxyCloudRunner package added to Galaxy
- CloudBridge event dispatcher
- CloudBridge GCE progress
- Update on ansible-galaxy-os role: 18.04, slim version, need for nginx

## 2019-01-08: Plans for Q1/2019
![Q1/2019 projects](https://i.imgur.com/EdoOKvJ.png "Q1/2019 projects")

- GCE support in CloudBridge: https://github.com/CloudVE/cloudbridge/pull/114
- [Galaxy on Kubernetes planning document](https://docs.google.com/document/d/1ffL_LePZ35Cr_FEgirFMnguZmIcfhrF1wZMogOHCijo/edit#)

## 2018-12-18
- Prioritze CloudBridge tasks for CollaborationFest with Vassar
- CloudBridge GCE provider
- Making Galaxy jobs fetch/deposit their own input/output data

## 2018-12-11
- No meeting

## 2018-12-04 
- No meeting

## 2018-11-27
- CloudMan 2.0 charts update
- Making the Pulsar bursting more robust
- Finalizing CloudBridge docs update
- Galaxy Helm chart early impressions

## 2018-11-20
- Galaxy bursting update
- Update on the CloudMan 2.0 charts
  - [x] Keycloak stock and latest version
  - [x] Keycloak-Rancher integration
  - [x] Prometheus stock
  - [ ] Grafana stock

## 2018-11-13
- GalaxyCloudRunner update:
  - [Rules module override](https://github.com/galaxyproject/galaxy/pull/6993)
  - [Chaining dynamic destinations](https://github.com/galaxyproject/galaxy/pull/7006)
  - [Support for CVMFS in Pulsar Docker](https://github.com/galaxyproject/pulsar/pull/166)
- Chart updates for CloudMan

## 2018-11-06
- Items from last week: [todos](https://github.com/CloudVE/mgmt/issues/5), [GVL 4.4 issues](https://github.com/galaxyproject/cloudman/issues)
- Update on the Custos project kickoff
- Galaxy PR [#6583](https://github.com/galaxyproject/galaxy/pull/6583)
- Progress on Pulsar bursting: https://docs.google.com/document/d/12SPNzG4E_tJyA1jEG2VqAi90r65THPxZpsDRTb5-IoM/edit
- ClouBridge branch cleanup: https://docs.google.com/spreadsheets/d/1rfl9vzfU1nCXks962QDnrr_DRrja6N1W5RQAmZzJS74/edit?usp=sharing

## 2018-10-30 [todo list](https://github.com/CloudVE/mgmt/issues/5)
- Todos from last week: https://github.com/CloudVE/mgmt/issues/4
- Update on the call with the AnswerALS project
- Name for the dynamic job runner library
- Issues reported with GVL 4.4: https://github.com/galaxyproject/cloudman/issues
- Progress on Pulsar bursting: https://docs.google.com/document/d/12SPNzG4E_tJyA1jEG2VqAi90r65THPxZpsDRTb5-IoM/edit
- Galaxy PR [#6583](https://github.com/galaxyproject/galaxy/pull/6583) status.

## 2018-10-23: [todo list](https://github.com/CloudVE/mgmt/issues/4)
- Assignemnts from last week: https://github.com/CloudVE/mgmt/issues/3
- Cloud bursting demo and next steps
- Galaxy cloud send tool [PR #6583](https://github.com/galaxyproject/galaxy/pull/6583)

## 2018-10-16
- Galaxy cloud download tool [PR #6583](https://github.com/galaxyproject/galaxy/pull/6583)
- Status of GVL 4.4 issues from last week
- CloudLaunch issues in Sentry (https://sentry.galaxyproject.org/sentry/cloudlaunch/)
- Updates and plans with Pulsar bursting

## 2018-10-09
- Reported issues with GVL 4.4: https://github.com/galaxyproject/cloudman/issues
- Galaxy bursting progress & plans: 
  - [CloudLaunch API keys](https://github.com/galaxyproject/cloudlaunch/pull/156)
  - [Pulsar Docker container](https://github.com/galaxyproject/pulsar/pull/166)
  - [Pulsar Helm chart](https://github.com/galaxyproject/pulsar-helm)
  - Operational validation
- Galaxy cloud download tool progress

## 2018-09-26
- Report from _[Nuwan the biologist](http://www.icter.org/conference/workshops/)_
- GVL 4.4/Galaxy 18.05 release
- Galaxy [team meeting presentations](https://docs.google.com/presentation/d/10uNH8tbWwZ1nPr3WtAHBrfF7rT8vWb93pCacfWbS6L4/edit#slide=id.p)
- Kicking off work on [Galaxy bursting](https://github.com/galaxyproject/galaxy/issues/6426)
- Interest in another meeting focused on _using galaxy_?

## 2018-09-11: [todo list](https://github.com/CloudVE/mgmt/issues/2)
- CloudAuthz [PR #5903](https://github.com/galaxyproject/galaxy/pull/5903) review/merge (@Vahid & @Enis)
- Download tool [PR #6583](https://github.com/galaxyproject/galaxy/pull/6583) review/merge (@Vahid & @Enis)
- CloudBridge publication
- Updating CloudLaunch for CloudBridge v1
- Add Galaxy-Docker-Stable on Azure in CloudLaunch
- GVL 4.4/Galaxy 18.05 release

## 2018-09-04
- CloudBridge v1 release;
- Genomespace update.

## 2018-08-28
- CloudBridge 1.0 release
- Update Genomespace to avoid dependency conflicit with CloudBridge 1.0. 

## 2018-08-21
- CloudBridge 1.0 release
  - Changing of `name` property to `label` status
  - [Issue #140](https://github.com/CloudVE/cloudbridge/issues/140)
  - [Release process](http://cloudbridge.cloudve.org/en/latest/topics/release_process.html) and plans
- GVL with Galaxy 18.05 testing
- CloudBridge 1.0 in Galaxy

## 2018-08-14
- CloudBridge 1.0 release
  - Documentation updates
  - Changing of `name` property to `label`
  - [PR #136](https://github.com/CloudVE/cloudbridge/pull/136)
  - [Issue #135](https://github.com/CloudVE/cloudbridge/issues/135)
- Galaxy download data tool [PR #6853](https://github.com/galaxyproject/galaxy/pull/6583)
- GVL with Galaxy 18.05 testing

## 2018-08-08
- CloudBridge 1.0 release
  - Installation of dependencies
  - Documentation
  - Changing of `name` property to `label`
  - PR [#136](https://github.com/CloudVE/cloudbridge/pull/136)
- Progress update on async Galaxy data download to cloud object stores
- GVL release with Galaxy 18.05
- Other
