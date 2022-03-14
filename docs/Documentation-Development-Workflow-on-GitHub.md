This page is intended to provide you details on how to develop a document on GitHub from inception to publication. The process covers all the steps involved and provides you with links to external resources where necessary or helpful.

ℹ️ **Audience**  
 > This page is intended for use by the technical communicators in Technical Documentation and Localization (TDL) department. If you have suggestions for improvements, clarifications, or other feedback about the contents on this page, please raise an issue. For details, see  [Creating an issue](https://help.github.com/articles/creating-an-issue/).

## Let's Get Started!
A document on GitHub goes through multiple phases before its published. For example, content may be created by an author, approved by subject matter experts, and then polished by the editor before being sent off for translation. 

The following graphic illustrates various states of document development on GitHub.
![github workflow](https://user-images.githubusercontent.com/6716089/45685686-c8d18500-bb67-11e8-9ddc-c479fc882af7.png)

### Stage 1 - Git Clone
Cloning a repository to your local computer creates a copy of that same repo locally on your computer. This allows you to edit the files on your computer. TDL recommends the **Atom** editor to edit the markdown files.
Start from the github.com interface:

1. Navigate to the repo that you want to clone (copy) to your computer -- this should be YOUR-USER-NAME/TechDocs.
2. Click **Clone or Download**.
3. Click **Open in Desktop** to clone the repository and open it in GitHub Desktop.

   ![github-clone](https://user-images.githubusercontent.com/6716089/40775332-6b5e0034-64e5-11e8-91b1-6b515036ad98.png)

4. Click **Choose...** and, using Windows Explorer, navigate to a local path where you want to clone the repository.
5. Click **Clone**.

Once you successfully clone the repository to your local drive, you need to set the default branch. The default branch is considered the base branch in your repository, against which all pull requests and code commits are automatically made. You need to ensure that **your document branch** is set as default. 

ℹ️  For details on various branches recommended by TDL, see https://github.com/Xilinx/TechDocs/wiki/GitHub-workflow. 

>**📌 NOTE**
> Your default branch is named after your assigned document <kbd>DocID</kbd>. If you do not see a branch with your document <kbd>DocID</kbd>or if you do not have a <kbd>DocID</kbd>, contact your manager.

6. On GitHub, navigate to the main page of the repository.
7. Under your repository name, click  **Settings**.
8. In the left menu, click **Branches**.
9. In the default branch sidebar, choose the new default branch. The new default branch should be the one titled similar to the <kbd>DocID</kbd> of your document.

### Stage 2 - Editing Markdown Files
TDL recommends using Atom editor to edit/update the markdown files. For details on installing Atom, see https://github.com/Xilinx/TechDocs/wiki#step-5-install-and-configure-atom-editor.

1. Select **File** > **Add New Project** Folder.  The **Open Folder** dialog box appears.
2. Navigate to the cloned git repo on your local drive. 
3. Click **Select Folder** to add the git repo folder to view the files listed in the **Project** tab in the Atom editor. 

   ![image](https://user-images.githubusercontent.com/6716089/41344697-5ee36288-6f1f-11e8-82da-ba1baf2d2a47.png)

4. Click File > Settings to open the Settings tab.
5. Select + Install and search for the following packages to install:
    * Atom Markdown Auto Preview
    * Markdown Preview Plus
    * Tool Bar Markdown Writer
    
    The above packages provide the Markdown preview functionality in the Atom editor.

### Stage 3 - Push Updated Files
After you have finished making your changes, it is time to commit them. TDL recommends using GitHub Desktop application to perform git related actions. For details on installing and configuring GitHub Desktop, see https://github.com/Xilinx/TechDocs/wiki#step-4-install-and-configure-github-desktop.

1. Click the changes tab in the left sidebar to see a list of the files that have been changed or added since the last commit.
2. Use the checkboxes to indicate which files should be part of the commit. 

   ![image](https://user-images.githubusercontent.com/6716089/41346218-7fa7a124-6f23-11e8-9e5d-c05271e6092c.png)

>**📌 NOTE**
>It is a good idea to group files together based on the type of changes or the file content. For example, if you fixed the same formatting issue in several documents, you should group them into one commit.

3. Type your commit message in the Summary field.
    You will notice that GitHub Desktop has already populated the commit button with the current branch. 
4. Click the **Commit to <DocID>** button to commit your changes.


