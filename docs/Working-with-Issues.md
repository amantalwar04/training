Our docs are a continuous work in progress. Good issues help us focus our efforts on the highest priorities. The more detail you can provide, the more helpful the issue. Tell us what information you sought. Tell us the search terms you used. If you can't get started, tell us how you want to start exploring unfamiliar technology.

Issues start the conversation about what's needed. TDL will respond to these issues with ideas for what we can add, and ask for your opinions. When we create a draft, we'll ask you to review the pull request.

## Overview

GitHub’s issue tracking is special because of its focus on collaboration, references, and excellent text formatting. A typical issue on GitHub looks a bit like this:

![image](https://user-images.githubusercontent.com/6716089/43625764-515d8e08-970c-11e8-83e2-be0ef59b95fc.png)

* A **title** and **description** describe what the issue is all about. It is recommended that you provide a meaningful title and clear description to ensure quick resolution of your issue.

* Color-coded **labels** help you categorize and filter your issues (just like labels in email). You can create your own labels to ease the identification and categorization of the issues. For more information, see the GitHub help article at [Labeling issues and pull requests](https://help.github.com/articles/labeling-issues-and-pull-requests/).

* A **milestone** acts like a container for issues. This is useful for associating issues with specific features or project phases (e.g. v2018.3). For more information, see [About milestones](https://help.github.com/articles/about-milestones/).

* One **assignee** is responsible for working on the issue at any given time. It is recommended that the writer watches his repository to get updates. This helps in situation when no assignee is added to the issue. For more information, see [Watching and unwatching repositories](https://help.github.com/articles/watching-and-unwatching-repositories/).

* **Comments** allow anyone with access to the repository to provide feedback.

* By using **@mentions** and references inside of Issues, you can notify other GitHub users & teams, and cross-connect issues to each other.

## Workflow

As for the workflow, it is expected that the writer updates the markdown files and initiates a conversation with the issue reporter to close the issue. 
* **If the issue is a high priority one:**
  * Create a hotfix branch from the existing doc branch
  * Create/update the topic(s)
  * Create a interim pull request to discuss the updates 
  * Get approvals and merge the updates
  * Download a zip of the hotfix branch and upload the files to the public repo (manually)
  * Create a pull request to merge the hotfix branch into the doc master branch
  * Create a new release (by selecting the updated doc branch).

    >:pushpin: **NOTE:** The hotfix branch is deleted from the repository as this is an incremental change to the current version.

For more information on the Hotfix branch, see [Hotfix branches](https://github.com/Xilinx/TechDocs/wiki/GitHub-workflow#hotfix-branches)


* **If the issue is an update that can be released in a future release:**
  * Create a development branch, if it does not exist.
  * Create/update the topic(s) in the development branch

For more information on the development branch, see [Development branch](https://github.com/Xilinx/TechDocs/wiki/GitHub-workflow#the-development-branch)

* **If the issue is an update to an older release:**
  * Create a support branch from the release tag of the previous version
  * Create/update the topic(s) in the support branch
  * Copy the updates to the public repo. Ensure that you select the right branch before copying the contents to the public repo.

    >:pushpin: **NOTE:** Support branches are never deleted from the repository.

For more information on the Support branch, see [Support branches](https://github.com/Xilinx/TechDocs/wiki/GitHub-workflow#support-branches)

# Worth reading
* [About issues](https://help.github.com/articles/about-issues/)
* [Mastering Issues](https://guides.github.com/features/issues/)