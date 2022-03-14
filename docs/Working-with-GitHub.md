<h1>Create a branch</h1>

1. On GitHub, navigate to the main page of the GitHub repository.
2. Click the branch selector menu.
3. Type the branch name. For details on branches, see the [GitHub Workflow](GitHub-workflow.md)
4. Press <b>Enter</b>. 

<h1>Start a Review</h1>

1. Under your repository name, click <b>Pull requests</b>.
2. In the list of pull requests, click the pull request that you'd like to ask a specific person or a team to review.
3. To request a review from a suggested person, in the right sidebar under <b>Reviewers</b>, click <b>Request</b>.
4. Press <b>Enter</b>.

📌 <b>NOTE:</b> If you request a review, other people with read access to the repository can still review your pull request. If the requested reviewer does not submit a review, and the pull request meets the repository's mergeability requirements, you can still merge the pull request.

<h2>Add Review Comments</h2>

1. Under your repository name, click <b>Pull requests</b>.
2. In the list of pull requests, click the pull request you'd like to review.
3. On the pull request, click  <b>Files changed</b>.
4. Hover over the line of code where you'd like to add a comment, and click the blue comment icon.
5. In the comment window, type your comment. When you're done, click <b>Start a review</b>. If you have already started a review, you can click <b>Add review comment</b>.

<h2>Submit Review</h2>

1. Under your repository name, click <b>Pull requests</b>.
2. In the list of pull requests, click the pull request you'd like to review.
3. On the pull request, click  <b>Files changed</b>.
4. Above the changed code, click <b>Review changes</b>.
5. Type a comment summarizing your feedback on the proposed changes.
6. Select the type of review you'd like to leave:
   1. Select <b>Comment</b> to leave general feedback without explicitly approving the changes or requesting additional changes.
   2. Select <b>Approve</b> to submit your feedback and approve merging the changes proposed in the pull request.
   3. Select <b>Request changes</b> to submit feedback that must be addressed before the pull request can be merged.
7. Click <b>Submit review</b>.

# Rename a branch

📌 <b>NOTE:</b> Please contact your GitHub Admin in case you need to rename a branch.

```
git branch -m old_branch new_branch         # Rename branch locally    
git push origin :old_branch                 # Delete the old branch    
git push --set-upstream origin new_branch   # Push the new branch, set local branch to track the new remote
```
# Extract individual folders from within a repo

```
git init
git remote add -f origin <url>
git config core.sparsecheckout true
echo <dir1>/ >> .git/info/sparse-checkout
echo <dir2>/ >> .git/info/sparse-checkout
echo <dir3>/ >> .git/info/sparse-checkout
git pull origin master
```

<h1>Additional resources</h1>
   
- For basic writing and formatting syntax, see https://help.github.com/articles/basic-writing-and-formatting-syntax/
