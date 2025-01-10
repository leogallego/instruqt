---
slug: controller-101-dashboard
id: so1tdhdv9mrp
type: challenge
title: 1.0 - Exploring the web-UI and Dashboard
teaser: Let's explore the dashboard, inventory and projects!
notes:
- type: text
  contents: |-
    # Welcome to Ansible Automation Platform

    Welcome to Ansible Automation Platform interactive labs! In this laboratory we will explore the Automation Execution (also known as Automation controller) web-based user interface (web-UI).

    Through hands-on exercises we will demonstrate how easy it is to use Ansible Automation Platform by running some of the playbooks from the "*Writing your first playbook*" lab from the web-UI.

    The "Writing your first playbook" lab is not a prerequisite, neither it is to have Ansible playbook development experience, although having done that lab or having command-line experience with Ansible will help for context.

    We will start exploring the web-UI, create an **Inventory** to manage our servers, import our playbooks into **Projects**, add **Job Templates** to run our playbooks and finally, create a **Workflow** linking a few of those playbooks through success or failure conditions, to create more complex environments.
- type: text
  contents: |-
    # Automation Platform Overview

    ![Oct-16-2024_at_02.01.47-image.png](../assets/Oct-16-2024_at_02.01.47-image.png)

    The **Overview**  shows a summary of your hosts, projects and inventories. Each of them are a link to the corresponding objects for easy access. Right below the resource counts, you will find a Job Activity graph with the executions and below that a card-like summary of the existing Jobs, Projects and Inventories.
- type: text
  contents: |-
    # Automation controller Jobs view

    ![ug-dashboard-jobs-view.png](../assets/ug-dashboard-jobs-view.png)

    Access the Jobs view by clicking Jobs from the left navigation bar. This view shows all the jobs that have ran, including projects, templates, management jobs, SCM updates, playbook runs, etc.
- type: text
  contents: |-
    # Schedules view

    ![Oct-16-2024_at_02.12.32-image.png](../assets/Oct-16-2024_at_02.12.32-image.png)

    Access the Schedules view by clicking the "Automation Execution" menu on the left sidebar, then the "Schedules" section. This view shows all the scheduled jobs that are currently configured and programmed to launch on a regular basis. They can be used to launch jobs against machines, synchronize with inventory sources, and import project content from a version control system.
tabs:
- id: 9quyzhjzysl6
  title: Automation controller
  type: service
  hostname: control
  path: /
  port: 443
- id: xlnsmqad1lgr
  title: Terminal
  type: terminal
  hostname: control
difficulty: ""
timelimit: 600
enhanced_loading: null
---

👋 1.0 - Introduction to automation controller
===

Welcome to the **Introduction to automation controller** lab.

Red Hat Ansible Automation Platform includes a web-UI and API that allows you to define, operate, scale, and delegate automation across the enterprise.

The new unified UI in Ansible Automation Platform 2.5 has several sections, but for this lab we will focus on the **Automation Execution (Automation controller)** view and features, highlighted below:

![Oct-16-2024_at_02.36.20-image.png](../assets/Oct-16-2024_at_02.36.20-image.png)

In the following challenges we will build upon the work from the *Writing your first playbook* laboratory and show you how to run your Ansible playbooks through the web-UI like you would in a corporate environement for operating the automation.

**The screen on the left shows the login screen. You can log in with the following credentials and then continue on to the tasks:**

> [!IMPORTANT]
> * Username: `admin`
> * Password: `ansible123!`

☑️ Task 1 - Explore the Overview
===

Explore the **Overview**.  The initial screen will show little information due to the lack of playbooks, hosts, and executions, but take a look now and you will be able to compare once you finished the lab and notice the difference.

You will find the following card-like sections:

* **Resource counts**: This section will show a summary of **hosts**, **projects** and **inventories**
* **Job activity**: This section will show a graph with the past month Job runs
* **Jobs**: A list of recently runned jobs
* **Projects**: A list of recently updated projects
* **Inventories**: A list of recently updated inventories

If you click any of the titles (or "View all" links) it will take you to the corresponding section. We recommend you take a peek at them.

And last but not least, a new card-like section in Ansible Automation Platform 2.5 that includes quick start guides or interactive howtos:
![Oct-16-2024_at_02.29.14-image.png](../assets/Oct-16-2024_at_02.29.14-image.png)

This new section will be very useful for learning right after you installed Ansible Automation Platform, as you will get instructions for using AAP in the same interface.

☑️ Task 2 - Explore the inventories section
===

Click on the **Inventories** text in the **Overview** or the link in the sidebar menu (under **Infrastructure**) and explore the **Demo inventory** that comes pre-loaded. For now, just explore the different tabs to familiarize with the fields. You will create your own soon!

An **Inventory** is a collection of hosts against which playbooks may be launched or run against. Basically, the "managed nodes" or devices we are automating. The inventory here is the same as an inventory file you might know from working with Ansible on the command line.

**Inventories** in AAP have several advantages over file based ones, you get all the functionality from the latter ones, with added features and better reusability.

☑️ Task 3 - Explore the projects section
===

In the sidebar menu, under the **Automation Execution** click on the **Projects** submenu and explore the **Demo project** that comes pre-loaded. You will see all the fields available to use when creating one. Don't forget to look at the tabs!

**Projects** are logical groups of Ansible playbooks in automation controller. These playbooks usually reside in a source code version control system like Git (and platforms as Github or Gitlab). With **Projects** we can reference a repository or directory with one or several playbooks, that we will later use.


✅ Next Challenge
===

Press the `Next` button below to go to the next challenge once you’ve completed the tasks.

🐛 Encountered an issue?
====

If you have encountered an issue or have noticed something not quite right, please [open an issue](https://github.com/ansible/instruqt/issues/new?labels=controller-101&title=Issue+with+controller-101-dashboard+AAP25&assignees=leogallego).

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