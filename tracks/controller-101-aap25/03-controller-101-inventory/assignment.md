---
slug: controller-101-inventory
id: 3r6lsub3iiy6
type: challenge
title: 1.1 - Creating an Inventory
teaser: Managing hosts and groups the easy way
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
- id: p8ktesjmsej6
  title: Automation controller
  type: service
  hostname: control
  path: /
  port: 443
- id: 4aezyvjr82gp
  title: Terminal
  type: terminal
  hostname: control
difficulty: ""
timelimit: 600
enhanced_loading: null
---
🗃️ 1.1 - Inventories
===

An inventory is a collection of hosts against which jobs (ex. playbooks) may be launched, the same as an Ansible inventory file, it indicates which nodes will be managed by the control machine, in this case the automation controller.

**Inventories** may be divided into *groups* and these groups contain the actual *hosts*. The *hosts* may be sourced manually or dynamically and can be referenced by their **IP addresses** or their **hostnames**.

In automation controller you will be able to run multiple playbooks against these inventories without recreating them.


☑️ Task 1 - Creation of the Inventory
===

1. On the side navigation bar, click the Automation Execution menu option
2. Now click the **Infrastructure** section to expand it and click on **Inventories**
3. Click on the blue **Create inventory** button
4. Select **Create inventory** from the dropdown
5. Name it `Lab-Inventory` .
6. In the **Organization** dropdown, select `Default`
7. Leave all the other fields as they are.
8. Click **Create inventory**

☑️ Task 2 - Add Hosts to the Lab-Inventory
===

> [!NOTE]
> If you are not in the  **Lab-Inventory**, click on it again to edit it.

1. Inside the `Lab-Inventory` you will see a tab bar
2. On the tab bar, click on **Hosts**
3. Click on the blue **Create host** button in the center.
4. In the **Name** text box enter `node1` . Leave all the other fields as they are.
5. Click **Create host**
6. Use the breadcrumb **"< Back to Hosts"** on the tab bar, or click **Hosts** on the sidebar.
7. Repeat the above steps to create a new host, named `node2` in `Lab-Inventory`.


☑️ Task 3 - Create the [web] group in Lab-Inventory
===

1. On the sidebar, go to **Inventories** and click on  the `Lab-Inventory`
2. On the tab bar of `Lab-Inventory`, click on the  **Groups** tab
3. Click on the **Create group** button to create a new group.
4. Name the group `web` (NOTE: you don't need to input it with the brackets `[ ...]` like you would in an inventory file).
5. Click **Create group**


☑️ Task 4 - Add node1 and node2 to the [web] group in Lab-Inventory
===

1. Inside the `web`  group you just created
2. Click on the **Hosts** tab on the top menu
3. Click **Add existing host**. A pop up will appear.
4. Tick both `node1` and `node2` then click **Add hosts**.
5. Verify `node1` and `node2` are now added to the `web` group in the **Hosts** tab


✅ Next Challenge
===
Press the `Check` button below to go to the next challenge once you’ve completed the task.

🐛 Encountered an issue?
====

If you have encountered an issue or have noticed something not quite right, please [open an issue](https://github.com/ansible/instruqt/issues/new?labels=controller-101&title=Issue+with+Intro+to+Controller+slug+ID:+controller-101-inventory+AAP25&assignees=leogallego).

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
