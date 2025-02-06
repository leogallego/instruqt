---
slug: controller-101-project
id: ee0nwmbyve9s
type: challenge
title: 3 - Automation Controller - Creating your first Project
teaser: Let's import our first playbooks into automation controller
notes:
- type: text
  contents: |-
    # Projects

    ![projects-list-all.png](../assets/projects-list-all.png)

    You can manage playbooks on your server, or by placing your playbooks into a source code management (SCM) system supported by automation controller, including Git, Subversion, and Red Hat Insights.
tabs:
- id: xshlgze5aks2
  title: AAP
  type: service
  hostname: control
  port: 443
- id: olt7azkpnnbe
  title: gitea
  type: service
  hostname: gitea
  port: 3000
difficulty: ""
timelimit: 0
enhanced_loading: null
---
 💡 Projects
===

A **Project** in Automation Execution *(formerly Automation controller)* are one or more Ansible playbooks (and related roles, etc.) inside a directory. Usually, they are in a Source Control Management system like a **Git** repository. We use **Projects** to "*import*" our playbooks into Ansible Automation Platform.

In this challenge, you will create your first **Project** and import from the provided Git repository `aap_workshop`. This repository is provided by a local Gitea server we have installed as part of the lab and you can find it's web based user interface in the Gitea tab.


☑️ Task 1 - Creation of the Project
===

1. Expand the **Automation Execution** section in the sidebar menu.
2. Click the **Projects** link in the menu.
3. Click the **Create project** button.

  ![create project](../assets/create_project.png)

Fill out the form with the following details:

1.   **Name**: `NetOps Playbooks`
2.   **Organization**: `Default`
3.   **Source Control Type**: `Git`.
4.   **Source Control URL**: `http://gitea:3000/student/aap_workshop.git`
5.   Leave all other fields as they are.
6.   and click on **Create project** at the bottom.

  > [!NOTE]
> The **Source Control URL** will be the URL to the repository `aap_workshop` in the Gitea server, this field will appear after `Git` has been selected as the **Source Control Type**.


☑️ Task 2 - Verify the new Project synced successfully
===

1. After creating you should be taken to the **Details** tab of the new Project.
2. Verify that the **Status** for our `NetOps Playbooks` project is green and reads **Success**.
3. Click the **Success** text and review the output of the sync

✅ Next Challenge
===
Press the **Next** button below to go to the next challenge once you’ve completed the challenge.

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
