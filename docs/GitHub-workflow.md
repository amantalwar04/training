# The master branch
The TechDocs repo holds the `<docid>` branch with an infinite lifetime. The source files on this branch are always in a _production-ready_ state.

 > **Naming Convention:** `<docid>` - Usually named after the Document ID

# The development branch
Once the writer forks the TechDocs repository to his personal GitHub, he is expected to create a development branch from the main `<docid>` branch. 

 > **Naming Convention:** `<docid>-develop` - Where `<docid>` is the Document ID. For example, `UG1236-develop`

# Supporting branches
Next to the main and development branches, our workflow uses a variety of supporting branches. Each of these branches have a specific purpose and are bound to strict rules which branches may be their originating branch and which branches must be their merge targets. 

The different types of supporting branches we recommend are:
		
* Release branches  - for finalizing a major/minor release
   > **Naming Convention:** `<docid>-release-*` - Where `<docid>` is the Document ID and `*` is the release number. For example, `UG1236-release-2018.1`
		
* Hotfix branches -  for applying patches to the latest release
   > **Naming Convention:** `<docid>-hotfix-*` - Where `<docid>` is the Document ID and `*` is the release number. For example, `UG1236-hotfix-2018.1`
		
* Support branches - for applying patches to old release versions
   > **Naming Convention:** `<docid>-support-*` - Where `<docid>` is the Document ID and `*` is the release number. For example, `UG1236-support-2017.4`

## Release branches

Release branches are created when the `develop` branch is at a stable point and release specific changes need to be made, such as bumping version numbers, etc. At that point, `develop` should be branched and the changes made before ultimately merging it into `master` and tagging the release. There should only be one active release branch at a time. Until the current release is wrapped up, merged into `master` and deleted, development of the next release should take place on `develop`. When `develop` reaches another state of stability for release, another release branch is be created.

**May branch off from**: `develop`
* create a branch (e.g. `<docid>-release-2018.1`), based on `<docid>-develop`
Fixes made on a release branch may be merged back into `develop` continuously if needed, though ultimately they will be merged in when the release is finalized.
* fix and merge `<docid>-release-2018.1` back into `<docid>-develop` 
* merge `<docid>-release-2018.1` back into `master`	
* create a tag `v2018.1`
	
At this point the release branch is safe to delete, since the changes are reflected in `develop` and `master`.

## Hotfix branches

Patches that need to be made to the most recent production release are applied to a hotfix branch off `master`. 

* create a branch (e.g. `<docid>-hotfix-2018.1.1`), based on `master`
* fix the bug and merge `<docid>-hotfix-2018.1.1` back into `<docid>-develop` and `master`

Merge into `develop` only if there is no current release branch, otherwise, merge into release branch instead. Finally, delete.

## Support branches

If `master` has moved on a point release (2017.1, 2017.2, 2017.3, etc) and a hotfix must be applied to a older version ( e.g 2017.1):

* create a `<docid>-support-2017.1` branch (if none exists) based on the newest 2017.1 tag in `master`
* create a branch (e.g. `<docid>-hotfix-2017.1.1`), based on `<docid>-support-2017.1`
* fix the bug and merge `<docid>-hotfix-2017.1.1` back into `<docid>-support-2017.1`
	
📌 **NOTE:** The support branch effectively becomes a master branch for a past version.