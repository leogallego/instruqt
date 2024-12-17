---
slug: controller-101-intro
id: ycsfmtvpjhqs
type: challenge
title: 0. - Intro to the automation controller lab
teaser: Introduction and tips to the laboratory
notes:
- type: text
  contents: |-
    # Welcome to Ansible Automation Platform

    Welcome to Ansible Automation Platform interactive labs! In this laboratory we will explore the Automation Execution (also known as Automation controller) web-based user interface (web-UI) of Ansible Automation Platform.

    Through hands-on exercises we will demonstrate how easy it is to use Ansible Automation Platform by running some of the playbooks from the "*Writing your first playbook*" lab from the web-UI.

    The "Writing your first playbook" lab is not a prerequisite, neither it is to have Ansible playbook development experience, although having done that lab or having command-line experience with Ansible will help for context.

    We will start exploring the web-UI, create an **Inventory** to manage our servers, import our playbooks into **Projects**, add **Job Templates** to run our playbooks and finally, create a **Workflow** linking a few of those playbooks through success or failure conditions, to create more complex environments.
- type: text
  contents: |-
    # Automation Platform Overview

    ![Oct-16-2024_at_02.01.47-image.png](../assets/Oct-16-2024_at_02.01.47-image.png)

    The **Overview**  shows a summary of your hosts, projects and inventories. Each of them are a link to the corresponding objects for easy access. Right below the resource counts, you will find a Job Activity graph with the executions and below that a card-like summary of the existing Jobs, Projects and Inventories.

    We will go through all of this sections in the upcoming challenges, while doing hands-on exercises.
tabs:
- id: sd8jb6eycupg
  title: Automation controller
  type: service
  hostname: control
  path: /
  port: 443
- id: shkrwdndryrq
  title: Terminal
  type: terminal
  hostname: control
difficulty: ""
timelimit: 600
enhanced_loading: null
---
💡 Laboratory tips before we begin!
===

Before we begin, some basic tips to improve your lab experience:

1.  The instructions sidebar to the right can be resized (drag and drop the border) or completely collapsed (click on the "Hide instructions" button at the top) in case you need extra space for the main panel. You can try this now!
2. In the right sidebar, you will find the different sections. In each chapter, there will be an introduction to the challenge and the related tasks below. The sections can be collapsed and expanded by clicking on them.
![image.png](../assets/image.png)
3. When you finish with a challenge (or chapter), you need to click the green **Check** button to move to the next one. This will review the steps. If no review is required the button might be simply labeled **Next**.
4.  You have the option to **Skip** a challenge or chapter, keep in mind this will auto-solve the exercises.
5.  The lab has a 55 minutes limit that can be extended at the end. If you need more time, make sure to accept the popup.
6.  To start with the exercises click the green button labeled **Next**  below.

🐛 Encountered an issue?
====

If you have encountered an issue or have noticed something not quite right, please [open an issue](https://github.com/ansible/instruqt/issues/new?labels=controller-101&title=Issue+with+controller-101-intro+AAP25&assignees=leogallego).

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
