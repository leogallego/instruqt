---
slug: eda-netbox
id: ynxzna8stwfk
type: challenge
title: 21 - Event-Driven Ansible - NetBox as Source of Truth
teaser: Managing hosts and groups the easy way!
notes:
- type: text
  contents: |-
    # Inventories

    ![Oct-16-2024_at_02.39.15-image.png](../assets/Oct-16-2024_at_02.39.15-image.png)

    An inventory defines the hosts and groups of hosts upon which commands, modules, and tasks in a playbook operate.
- type: text
  contents: |-
    # Inventories, create new inventory

    ![Oct-16-2024_at_02.39.47-image.png](../assets/Oct-16-2024_at_02.39.47-image.png)

    In this challenge, we will be creating a new inventory, adding hosts and creating a host group inside the inventory.
tabs:
- id: yent0vflween
  title: AAP
  type: service
  hostname: control
  port: 443
- id: vj3js9x3vlzx
  title: gitea
  type: service
  hostname: gitea
  path: /
  port: 3000
- id: pil8wkhkarnj
  title: netbox web
  type: service
  hostname: netbox
  path: /
  port: 8000
- id: oiovxsxrvefx
  title: netbox term
  type: terminal
  hostname: netbox
  cmd: bash
- id: 6qlova9nx9dk
  title: VS Code
  type: service
  hostname: devtools
  path: /editor/
  port: 80
difficulty: ""
timelimit: 0
enhanced_loading: null
---
🗃️ NetBox
===

NetBox and the Ansible Automation Platform are two of the most powerful tools available for modern network automation. NetBox serves as a Network Source of Truth (NSoT) which is a representation of the intended configuration and state of the devices, connections, and services of the network. It captures the intended state, which is different than the operational state. It uses a structured, cohesive, comprehensive data model for network intent, that forces completeness and correctness in design, planning, configuration management and operations.

We already configured NetBox as a Source of Truth in our previous exercise, and now we will integrate it with Event-Driven Ansible. By sending event data from NetBox to Ansible Automation Platform we can unlock the potential for dynamic, event-driven network automation. Instead of waiting for scheduled tasks or manual intervention, Event-Driven Ansible (EDA) reacts to real-time triggers, such as a new device being added to NetBox or a change being approved and a branch being merged.


☑️ Task 1 - Creating the EDA Project:
===
1. Go to **Automation Decisions > Projects**
2. Click on **Create project**
3. Fill the form with the following:
```
Name: aap-netbox-rulebooks
Organization: Default
Source control type: Git
Source control URL: https://gitea:3000/student/aap-netbox-rulebooks.git
```
4. Click the blue **Create project** button at the bottom.

☑️ Task 2 - EDA credentials
===
1. Go to **Automation Decisions > Credentials**
2. Click on **Create credential**
3. Fill the form with the following:
Name: AAP EDA Cred
Organization: Default
Credential Type: Red Hat Ansible Automation Platform
Type Details:
Red Hat Ansible Automation Platform: https://aap/api/controller
Username: EDA
Password: EDA
4. Click the blue **Save credential** button at the bottom



☑️ Task 3 - Creating the Rulebook Activation
===

1. Go to **Automation Decisions > Rulebook Activations**
2. Click on **Create rulebook activation**
3. Fill the form with the following:
```
Name: aap-netbox-rulebooks
Organization: Default
Project: aap-netbox-rulebooks
Rulebook: netbox-webhook.yml
Credentials: AAP EDA Cred
Decision environment: Default Decision Environment
Restart policy: On failure
Log level: Error
```
4. Leave the rest as-is and click the blue **Create rulebook activation** button at the bottom.


☑️ Task 3 -
===

☑️ Task 4 -
===



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
