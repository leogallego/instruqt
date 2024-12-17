---
slug: controller-101-workflow
id: 2skayooaiuee
type: challenge
title: 1.7 - Creating a Workflow Job Template
teaser: 'Connecting all the dots: Link multiple playbooks by conditions'
notes:
- type: text
  contents: |-
    # Workflows

    ![wf-templates-home-with-example-wf-template.png](../assets/wf-templates-home-with-example-wf-template.png)

    A workflow job template links together different resources in a graphical way, this can include multiple playbooks (job templates), project syncs and even other workflows.
tabs:
- id: l1x1sy1y8n6n
  title: Automation controller
  type: service
  hostname: control
  path: /
  port: 443
- id: cpxezyta22dy
  title: Terminal
  type: terminal
  hostname: control
difficulty: ""
timelimit: 600
enhanced_loading: null
---
🔗 1.7 - Workflows
===

A **Workflow Job Template** is a series of connected automation tasks (or Playbooks) that are executed in a specific order to achieve a desired outcome.
Compared to an individual Playbook (or Job Template), a **Job Template** handles straightforward tasks in a single playbook, while a **Workflow job template** is designed to manage more complex automation scenarios involving multiple playbooks (or Job Templates) and decision-making processes.

- Job templates
- Workflow job templates
- Project syncs
- Inventory source syncs

Only **Workflow Job Templates** have the Workflow Visualizer icon (wf-viz-icon) as a shortcut for accessing the workflow editor.

> [!WARNING]
> Remember, do not confuse a **Job Template** with a **Jinja template**, or with **Workflow Job Template**.  They are 3 separate things.

☑️ Task 1 - Creating a Workflow Template
===

1. Click the **Automation Execution** dropdown in the sidebar
2. Click the **Templates** link
3. Click the **Create template** dropdown button and select **Create workflow job template**
4. In the **Name** field, input `Your first workflow`.
5. In the **Description** field, input: `Create a Workflow from previous Job Templates`
6. In the **Organization** dropdown, select `Default`
7. In the **Inventory** field, select `Lab-Inventory` from the dropdown
8. Leave everything else the same and click **Create workflow job template**.

☑️ Task 2 - Workflow Visualizer
===

1. This will take you to the Workflow Visualizer screen,
2. Click **Add step**, as the new Workflow is empty.
3. You will be presented with the **Add step** sidebar
4. For the **Node Type** field, select `Job Template` (default)
5. For the **Job Template** field, select `Install Apache`  from the dropdown.
6. Leave **Convergence** in `Any`
7. For the **Node alias** field, enter `apache101`, this is a simple label to use instead of the playbook name.
8. Click the **Next** button. In the next screen, review everything is correct and click **Finish**

☑️ Task 3 - Workflow Visualizer - Adding a condional step
===

1. Click the 3 dots next to the `apache101`  box we created in the previous step
2. Click the **Add step and link**
3. The same sidebar from before will show up to the right, this time with **one extra field**
4. For the **Node Type** field, select `Job Template` (default)
5.  For the **Job Template** field, select `Extended services`
6.  For the **Status** field, select `Run on sucess` from the dropdown
7.  Leave **Convergence** in `Any`
8. For the **Node alias** field, enter `extended201`, this is a simple label to use instead of the playbook name.
9.  Click the **Next** button. Review everything and click **Finish**.

Congratulations!  You have created a **Workflow Job Template** consisting of two linked **Job Templates**.

> [!NOTE]
> You can zoom in and out with the mouse wheel.

☑️ Task 3 - Workflow Visualizer - Adding a parallel step
===

> [!IMPORTANT]
> Pay atention to the source step!

Now let's add another step for a 3rd Job Template, but this time, it will run in parallel to the last one.

1. Click the 3 dots next to the `apache101`  box we created in the first step.
2. Click the **Add step and link**. Note this step will run in parallel to the last one, `extended201`.
3. The same sidebar from before will show up to the right, this time with **one extra field**
4. For the **Node Type** field, select `Job Template` (default)
5.  For the **Job Template** field, select `Set motd`
6.  For the **Status** field, select `Run on sucess` from the dropdown
7.  Leave **Convergence** in `Any`
8. For the **Node alias** field, enter `motd201`, this is a simple label to use instead of the playbook name.
9.  Click the **Next** button. Review everything and click **Finish**.

☑️ Task 4 - Workflow Visualizer - Save!
===

Now for the final step, we are going to save our Workflow:

1. Click the blue **Save** button at the top. If you miss this one, you will lose your changes!

☑️ Task 5 - Launch the new Workflow
===

There are 2 ways to launch our newly created Workflow. First the easiest while working on the Workflow:

1. Within the same **Workflow Visualizer** screen
2. Click the 3 dots right below the name, at the top, and select **Launch workflow** from the dropdown
3. Verify all the jobs executed successfully. You will  notice a **Sucess** text next to the Workflow name, as well as a ✅ tick in each job box.

Another option is to go back to the **Templates** list and
1. You can launch the Workflow from this list by clicking the 🚀 **Rocket** icon , or
2. You can click on the `Your first workflow`  name and click the **Launch template** button.
3. You will be presented with a smaller Workflow Visualizer that shows the progress of the execution as **Running**
4. Verify all the jobs executed successfully. You will  notice a **Sucess** text next to the Workflow name, as well as a ✅ tick in each job box.

✅ Next Challenge
===
Press the `Check` button below to go to the next challenge once you’ve completed the task.

🐛 Encountered an issue?
====

If you have encountered an issue or have noticed something not quite right, please [open an issue](https://github.com/ansible/instruqt/issues/new?labels=controller-101&title=Issue+with+Intro+to+Controller+slug+ID:+controller-101-workflow+AAP25&assignees=leogallego).

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
