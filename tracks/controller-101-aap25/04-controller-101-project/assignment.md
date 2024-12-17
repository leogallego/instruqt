---
slug: controller-101-project
id: jlenekrvxljq
type: challenge
title: 1.2 - Creating your first Project
teaser: Let's import our first playbooks into automation controller
notes:
- type: text
  contents: |-
    # Projects

    ![projects-list-all.png](../assets/projects-list-all.png)

    You can manage playbooks on your server, or by placing your playbooks into a source code management (SCM) system supported by automation controller, including Git, Subversion, and Red Hat Insights.
tabs:
- id: yfsnc9ewjzq9
  title: Automation controller
  type: service
  hostname: control
  path: /
  port: 443
- id: lzencg90bpju
  title: Terminal
  type: terminal
  hostname: control
difficulty: ""
timelimit: 600
enhanced_loading: null
---
 💡 1.2 - Projects
===

A **Project** in Ansible automation controller is one or more Ansible playbooks (and related roles, etc.) inside a directory. Usually, they are in a Source Control Management system like a **git** repository.

We use **Projects** to "*import*" our playbooks into automation controller. These playbooks might be in a source control management (SCM) like Git (in Github or Gitlab for ex.) or locally. Automation controller doesn't allow us to create or edit playbooks through the web-UI, we can only "*import*" them into **Projects** which we later run through the Job Templates feature, which we will review further ahead.

In this challenge, you will create your first **Project** which will import a GitHub repository with a few Apache playbooks. This playbook installs the Apache webserver, starts the service and copies an index.html file.


☑️ Task 1 - Creation of the Project
===

1. Expand the **Automation Execution** section in the sidebar menu
2. Click the **Projects** link in the menu
3. Click the **Create project** button
4. **Name** the Project as `Apache playbooks`
5. For the **Organization** field, select `Default` in the dropdown
6. For the **Source Control Type** dropdown, select **Git**, this will enable new fields below.
7. For the **Source Control URL** field copy & paste the following URL:
   ```
	 https://github.com/leogallego/instruqt-wyfp.git
	 ```
6. Leave all the other fields the same and click **Create project**

☑️ Task 2 - Verify the new Project synced successfully
===

1. After creating you should be taken to the **Details** tab of the new Project.
2. Verify that the **Status** for our `Apache playbooks` project is green and reads **Success**
3. Click the **Success** text and review the output of the sync

✅ Next Challenge
===
Press the `Check` button below to go to the next challenge once you’ve completed the task.

🐛 Encountered an issue?
====

If you have encountered an issue or have noticed something not quite right, please [open an issue](https://github.com/ansible/instruqt/issues/new?labels=controller-101&title=Issue+with+Intro+to+Controller+slug+ID:+controller-101-project+AAP25&assignees=leogallego).

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
