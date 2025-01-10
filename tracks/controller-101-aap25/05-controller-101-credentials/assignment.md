---
slug: controller-101-credentials
id: h1qqqibr1zbf
type: challenge
title: 1.3 - Get to know Credentials
teaser: Check the authentication options of automation controller
notes:
- type: text
  contents: |-
    # Credentials

    ![credentials-demo-edit-details.png](../assets/credentials-demo-edit-details.png)

    Credentials are utilized for authentication when launching Jobs against machines, synchronizing with inventory sources, and importing project content from a version control system.
tabs:
- id: yfzitf7v7krx
  title: Automation controller
  type: service
  hostname: control
  path: /
  port: 443
difficulty: ""
timelimit: 600
enhanced_loading: null
---
🔐 1.3 - Credentials
===

**Credentials** are utilized by Ansible Automation Platform for authentication when launching jobs against devices or managed nodes, synchronizing with inventory sources, and importing project content from a version control system.

Credentials are imported and stored encrypted within Ansible automation controller, and are not retrievable in plain text on the command line by any user.  You can grant users and teams the ability to use these credentials, without actually exposing the credential to the user itself.

There are multiple types of credential types, ranging from tokens, to user/passwords or public keys. In total, there are over 20 supported types and even the option to create *Custom* ones. We will explore the **Machine** credential type today, which we will use to connect to the servers in our inventory through SSH.

> [!IMPORTANT]
> In this excercise we are not making any changes. Credentials are pre-loaded.


☑️ Task 1 - Exploring the Credentials section
===

1. In the sidebar, expand the **Automation Execution** section
2. Now expand the **Infrastructure** menu and click the **Credentials** option
3. This will display a searchable list of pre-loaded credentials, classified by name and type.
4. Look for the `lab-credentials`, notice it says **Machine** type. Click on it.
5. Here you can see the details of the credential. Notice the **SSH Private Key** field says **Encrypted**.
6. Click the **Team Access** and **User Access** tab to see who has access to use this credential. These are the automation controller users.
7. Click the **Job Templates** tab to see what Jobs are currently using this credential. It should be empty right now.

☑️ Task 2 - Exploring the Machine Type credential
===

1. Go back to the **Details** tab of the **lab-credentials**
2. Click the **Edit credential** button
3. Look at the different fields available, but **don't edit or change anything**.
4. Notice how the **SSH Private Key** field only allows us to **Reset**. As we mentioned before, the key is encrypted and not retrievable.
5. To exit, click the **Cancel** button to avoid accidental modifications.


✅ Next Challenge
===
Press the `Check` button below to go to the next challenge once you’ve completed the task.

🐛 Encountered an issue?
====

If you have encountered an issue or have noticed something not quite right, please [open an issue](https://github.com/ansible/instruqt/issues/new?labels=controller-101&title=Issue+with+Intro+to+Controller+slug+ID:+controller-101-template+AAP25&assignees=leogallego).

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