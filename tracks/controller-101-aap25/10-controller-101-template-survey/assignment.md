---
slug: controller-101-template-survey
id: cgprj2ulgs1u
type: challenge
title: '1.8 - BONUS: Creating a Job Template with a Survey'
teaser: Level-up, let's try a fourth Job Template for installing Apache, including
  a Survey this time
notes:
- type: text
  contents: |+
    # Job templates

    ![job-templates-home-with-example-job-template.png](../assets/job-templates-home-with-example-job-template.png)

    In controller, job templates are a visual representation of the `ansible-playbook` command and all flags you can utilize when executing from the command line.

tabs:
- id: 1canvzbj49kg
  title: Automation controller
  type: service
  hostname: control
  path: /
  port: 443
- id: bbrfdlsl0tya
  title: Node1 Web
  type: service
  hostname: node1
  path: /
  port: 80
  url: http://node1
- id: 01awdhqcg2vi
  title: Terminal
  type: terminal
  hostname: control
difficulty: ""
timelimit: 600
enhanced_loading: null
---
🎉 Success!
===

Congratulations on finishing the **Introduction to automation controller** laboratory.

> [!NOTE]
> BONUS TRACK!
> This is an ***optional bonus track***. If you want to try the **Survey** feature of Ansible Automation Platform continue with the tasks below. You will also find a perk for your[ Ansible Forum](https://forum.ansible.com) profile at the end, claim your badge!

> [!IMPORTANT]
> If you want to finish right now and skip this challenge, simply press the  button at the bottom one last time to complete the lab, and remember to review and leave a comment. We appreciate all feedback!

📑 Bonus track: Job Template with a Survey
===

In this challenge, we will explore the **Survey** feature, which allows us to input a variable at runtime when we execute our **Job Template** (playbook), making it possible to change a parameter or setting at each run. We will be changing the index.html we deployed previously for a new one, so you can see the results in real time.

☑️ Task 1 - Creation of the Job Template
===

1. Click the **Templates** link in the **Automation Execution** section of the sidebar
2. Click the **Create template** dropdown button and select **Create job template**
3. **Name** the Job Template as `Install Apache with Survey`
4. For the **Job Type** field, leave the default: **Run**
5. For the **Inventory** field, select `Lab-Inventory` from the dropdown
6. For the **Project** field, select `Apache playbooks` from the dropdown
7. For the **Playbook**  field, you will notice that the dropdown it's auto populated with all the playbooks available in the **Project** repository we selected. Choose the `apache_template.yml` playbook.
8. For the **Credentials** field,  select `lab-credentials` from the dropdown and click outside the box to save.
9. Tick the **Privilege escalation** checkbox at the bottom
10. Leave all the other fields the same and click the blue **Create job template** at the bottom.

☑️ Task 2 - Create the Survey for the Job Template
===

1. Once the **Job Template** is saved, you should be taken to the *Details* tab of it
2. Look for the **Survey** tab and click on it.
3. Click the **Create survey question** button
4. In the **Question** field, enter `What is your name, fellow student?`
5. In the **Description** field, enter `Enter your name or nickname to see it works!`
6. In the **Answer variable name**, enter `student_name`
7. Leave the **Answer type** as is, `text`
8. Make sure **Required** is **NOT** ticked.
9. Leave minimum and maximum lengh as they are.
10. In the **Default answer** type `Skippy`
11. Press the **Create survey question** button at the bottom
12.  Now the **Survey** tab should show a list with the one we created
13.  Notice there is a toggle that reads **Survey disabled**, next to the *Create survey question* button now.
14. Click the toggle  to **Enable** the survey


☑️ Task 3 - Launch the new Template
===

1. Click the **Launch template** button at the top of the "Install Apache with Survey" Job Template screen
2. Delete Skippy from the **What is your name, fellow student?** field and enter your name
3. Click the **Next** button
4. Review and press the **Finish** button to launch the Job Template
5. Verify the execution was successful by visiting the **Node1 Web** tab in the top left of the screen, you should see the Apache message with your name below!

🎉 Congratulations!
===

You have finished the lab successfully and even managed to do the extra track! Claim your [Ansible Forum](https://forum.ansible.com) badge by scanning the QR below.

> [!IMPORTANT]
> Remember to press the green **Check** button below to finish the laboratory, rate and review it, we appreciate the feedback!

![Oct-23-2024_at_18.16.01-image.png](../assets/Oct-23-2024_at_18.16.01-image.png)

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
