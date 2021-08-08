# Updating from GitHub
When working on projects with other people, often your will need to update your repo with what they have committed. Depending on your client, you will need to do the following to make sure you get these files.

## GitHub Desktop

When using GitHub Desktop, if there were updates to a repo you are working on, you can hit the **Fetch origin** button.

![](images/github-desktop-fetch.png)

Image from and more info: [GitHub Desktop- Syncing your branch](https://docs.github.com/en/desktop/contributing-and-collaborating-using-github-desktop/keeping-your-local-repository-in-sync-with-github/syncing-your-branch/)

Sometimes, it may happen that more than one person is working on the same file. While Git will try to figure this out on it own, sometimes you may have a *conflict*. When this happens you may need to [use command line Git to straighten this out](https://help.github.com/articles/resolving-a-merge-conflict-from-the-command-line/)

## TortoiseGit
For TortoiseGit, there are two ways to get the latest from the repo.

* **Pull** -  This gets all the latest files and merges them with your files. Select **TortoiseGit -> Pull...**

  ![](images/tortoisegit_menu_pull.jpg)
  
  This will make the Pull requester pop up:
  
  ![TortoiseGit - Pull](https://tortoisegit.org/docs/tortoisegit/images/GitPull.png)

* **Fetch** - This downloads the latest files, but does not override any files you have modified. Select **TortoiseGit -> Fetch...**

  ![](images/tortoisegit_menu_fetch.jpg)

  Once you do, you will see a view like this:

  ![TortoiseGit - Fetch](https://tortoisegit.org/docs/tortoisegit/images/Fetch.png)

Images from and more info: [Pull and Fetch change](https://tortoisegit.org/docs/tortoisegit/tgit-dug-pull.html)

If there have been changes to the same file by different developers, and Git cannot automatically merge them, you may end up having to [resolve a conflict](https://tortoisegit.org/docs/tortoisegit/tgit-dug-conflicts.html)

[](https://tortoisegit.org/docs/tortoisegit/tgit-dug-conflicts.html)

<!--
## TortoiseSVN
Once you have a repo checked out, you just have to do an Update. Just right-click and select **TortoiseSVN -> Update...**

![](images/tortoisesvn_menu_update.jpg)

![TortoiseSVN - Update](http://tortoisesvn.net/docs/release/TortoiseSVN_en/images/UpdateFinished.png)

Images from and more info: [Update Your Working Copy With Changes From Others](http://tortoisesvn.net/docs/release/TortoiseSVN_en/tsvn-dug-update.html)

If more than one person has changed a file and SVN cannot figure out how to merge them automatically, you will have to [resolve the conflict](http://tortoisesvn.net/docs/release/TortoiseSVN_en/tsvn-dug-conflicts.html).
-->