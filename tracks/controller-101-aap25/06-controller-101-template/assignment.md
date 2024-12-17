---
slug: controller-101-template
id: zipmj3fb1g3c
type: challenge
title: 1.4 - Creating a Job Template
teaser: This is how you run a playbook with automation controller!
notes:
- type: text
  contents: |+
    # Job templates

    ![job-templates-home-with-example-job-template.png](../assets/job-templates-home-with-example-job-template.png)

    In controller, job templates are a visual representation of the `ansible-playbook` command and all flags you can utilize when executing from the command line.

tabs:
- id: 27clkosuqosy
  title: Automation controller
  type: service
  hostname: control
  path: /
  port: 443
- id: 74w7vegze6ly
  title: Node1 Web
  type: service
  hostname: node1
  path: /
  port: 80
  url: http://node1
- id: c7vasovymu4w
  title: Node2 Web
  type: service
  hostname: node2
  path: /
  port: 80
difficulty: ""
timelimit: 600
enhanced_loading: null
---
📑 1.4 - Job Templates
===

In automation controller a **Job Template** is a definition and set of parameters for running an Ansible playbook. Job Templates are useful to execute the same job many times while also encouraging the reuse of Ansible content and collaboration between teams.

To create a **Job Template** you need to have a **Project** (a repository or directory) from which to source our *Playbooks*. We created our Project in the previous challenge. Also note that although a **Project** might contain multiple *Playbooks*, a **Job Template** can only run one of those playbooks. For running multiple Playbooks we will explore the **Workflow** feature further ahead in the  laboratory.

> [!WARNING]
> **Do not confuse a Job Template with a Jinja template**. Jinja templates are used to create dynamic template files, with variables and facts that will be replaced during runtime. This is very useful for configuration files for example. If you don't know Jinja, don't worry about it right now, just know that they are different things.

☑️ Task 1 - Creation of the Job Template
===

1. Click the **Templates** link under the **Automation Execution** section of the sidebar
2. Click the **Create template** dropdown button and select **Create job template**
3. **Name** the Job Template as `Install Apache`
4. For the **Job Type** field, leave the default: `Run`
5. For the **Inventory** field, click and and select `Lab-Inventory` from the dropdown
6. For the **Project** field, click and select `Apache playbooks` from the dropdown
7. For the **Playbook** field, click and you will notice that it's auto populated with all the playbooks available in the **Project** repository we selected. Choose the `apache.yml`.
8. For the **Credentials** field,  click and only tick `lab-credentials` from the dropdown. You can click outside the dropdown to close. No need to click browse right now, but if you do, simply click confirm.
9. Scroll to the bottom and make sure to tick the **Privilege escalation** checkbox.
10. Leave all the other fields the same and click **Create job template**

> [!IMPORTANT]
> Note that the **Credentials** field is not mandatory, but if you don't select the right credentials, the execution will fail.

☑️ Task 2 - Launch the new Template
===

1. Click the **Templates** link in the **Automation Execution** section of the sidebar
2. You can launch it from this list, by clicking the **Rocket** icon, or
3. You can click on the `Install Apache` template and then click the **Launch** button at the bottom.
4. Verify the execution was successful

☑️ Task 3 - Verify Apache is working in node1 and node2
===

1. In the tab bar at the top left of your screen you will find **Node1 Web** and **Node2 Web** tabs.
2. Click on **Node1 Web**, check the message
3. Click on **Node2 Web**, check the message


✅ Next Challenge
===
Press the `Check` button below to go to the next challenge once you’ve completed the task.

🐛 Encountered an issue?
====

If you have encountered an issue or have noticed something not quite right, please [open an issue](https://github.com/ansible/instruqt/issues/new?labels=intro-to-controller&title=Issue+with+Intro+to+Controller+slug+ID:+controller-101-template&assignees=leogallego).

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
