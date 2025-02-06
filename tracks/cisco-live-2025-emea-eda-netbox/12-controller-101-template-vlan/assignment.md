---
slug: controller-101-template-vlan
id: i1z1fwzzsxxg
type: challenge
title: 7 - Automation Controller - Creating a Job Template for VLAN
teaser: This is how you run a playbook with automation controller!
notes:
- type: text
  contents: |
    # Job templates

    ![job-templates-home-with-example-job-template.png](../assets/job-templates-home-with-example-job-template.png)

    In controller, job templates are a visual representation of the `ansible-playbook` command and all flags you can utilize when executing from the command line.
tabs:
- id: 1pondvm6vx66
  title: AAP
  type: service
  hostname: control
  port: 443
- id: neuh6ajbtoaw
  title: Gitea
  type: service
  hostname: gitea
  path: /
  port: 3000
difficulty: ""
timelimit: 0
enhanced_loading: null
---
📑 Configuring a VLAN
===

Now we are going to add a VLAN to our devices

☑️ Task 1 - Creation of the Job Template
===

1. Click the **Templates** link under the **Automation Execution** section of the sidebar.
2. Click the **Create template** dropdown button and select **Create job template**. Fill out the form with the following details.
3. **Name** the Job Template as `Configure VLAN`
4. For the **Job Type** field, leave the default: `Run`
5. For the **Inventory** field, click and and select `NetOps Inventory` from the dropdown
6. For the **Project** field, click and select `NetOps Playbooks` from the dropdown
7. For the **Playbook** field, click and you will notice that it's auto populated with all the playbooks available in the *Project* repository we selected.
8. Choose the `solutions/playbooks/vlan.yml`. We are using a provided playbook for this exercise.
9. For the **Credentials** field,  click and only tick `cat8000v-credential` from the dropdown. You can click outside the dropdown to close. No need to click browse right now, but if you do, simply click confirm.
9. Leave all the other fields the same and click **Create job template**.

> [!IMPORTANT]
> Note that the **Credentials** field is not mandatory when creating a **Job Template**, but if you don't select the right credentials for the hosts you are executing against, the tasks will fail as AAP won't be able to connect to those devices..

☑️ Task 2 - Launch the new Template
===

1. Click the **Templates** link in the **Automation Execution** section of the sidebar.
2. You can launch it from this list, by clicking the **Rocket** icon, or by clicking on the `Configure VLAN` template and then clicking the **Launch** button at the bottom.
3. Verify the execution was successful and our devices show as "changed" and in yellow in the output of the **Job Template**

✅ Next Challenge
===
Press the **Next** button below to go to the next challenge once you’ve completed the task.

🐛 Encountered an issue?
====

If you have encountered an issue or have noticed something not quite right, please [open an issue](https://github.com/ansible/instruqt/issues/new?labels=netops-aap25&title=Issue+with+netops-aap25&assignees=leogallego)

<style type="text/css" rel="stylesheet">
  .lightbox {
    display: none;
    position: fixed;
    justify-content: center;
    align-items: center;
    z-index: 999;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    padding: 1rem;
    background: rgba(0, 0, 0, 0.8);
    margin-left: auto;
    margin-right: auto;
    margin-top: auto;
    margin-bottom: auto;
  }
  .lightbox:target {
    display: flex;
  }
  .lightbox img {
    /* max-height: 100% */
    max-width: 60%;
    max-height: 60%;
  }
  img {
    display: block;
    margin-left: auto;
    margin-right: auto;
  }
  h1 {
    font-size: 18px;
  }
    h2 {
    font-size: 16px;
    font-weight: 600
  }
    h3 {
    font-size: 14px;
    font-weight: 600
  }
  p span {
    font-size: 14px;
  }
  ul li span {
    font-size: 14px
  }
</style>
