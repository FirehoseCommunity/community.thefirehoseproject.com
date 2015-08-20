---
layout:     post
title:      "How To Fork A Repo And Contribute"
subtitle:   "A how to guide for forking a github repo and contribute to an open source project."
date:       2015-08-19 19:00:00
author:     "Colin Rubbert"
header-img: "img/chem.png"
---

{% include youtubePlayer.html id="G1I3HF4YWEw" %}

### Getting Your Fork On!

You're first step in the process will be going to the address of the repository that you will want to fork. For this example it will be the one and only rockstar, ninja, guru, [insert more cliche buzzwords], awesome [community Firehose Project Jekyll site](https://github.com/FirehoseCommunity/community.thefirehoseproject.com)!

`https://github.com/FirehoseCommunity/community.thefirehoseproject.com`

Pretty simple so far, now we're going to click on that wonderful little "fork" button. If it gives you an option to which organization you want to fork then you will just want to make sure you select your personal page.

![Image of Fork button](https://github-images.s3.amazonaws.com/help/bootcamp/Bootcamp-Fork.png)

Next we will want to move to our now forked repository, get the URL for the cloning process, and do a quick copy to our clipboard.

![Image of Clone button](https://help.github.com/assets/images/help/repository/clone-repo-clone-url-button.png)

Moving on we will want to open up our terminal, move to the directory that we want to host our files locally and run a git clone command.

Example (yours may look different):

`git clone git@github.com:FirehoseCommunity/community.thefirehoseproject.com.git`

Now we will want to move into our newly created directory. From here what you want to do it make sure everything is setup properly and that the Jekyll server serves up the data.

You can do this by running (mileage may vary due to differing environments).

`jekyll serve`

Kill the server by running `ctrl + c` so that we can create a new branch to make our changes in. This is a best practice way of doing things and this is how we recommend it to be done for submitting changes to the community site.

To create the branch we will want to run the command:

`git checkout -b [your_branch_name]`

What this will do is create your branch and check it out in one command. To verify you are working in your newly created branch run `git branch` and make sure the asterisk is next to the new branch.

From here we open up our text editor and make the changes that you want to make. Save your changes and do your standard git workflow with the exception for when you push your changes you will want to push to origin and then the specific branch you are working in.

`git add .`

`git commit -am "My rocking new changes"`

`git push origin [your_branch_name]`

After we commit our changes we can go back to our GitHub page and checked to make sure that we have a compare for pull request notice at the top of our repository.

![Compare and Pull Request](https://github-images.s3.amazonaws.com/help/pull_requests/recently_pushed_branch.png)

Click on "Compare & Pull Request", you will be redirected to the pull request page. Add your pull request information including description of your changes and then click "Create Pull Request".

![Create Pull Request](https://github-images.s3.amazonaws.com/help/pull_requests/pullrequest-send.png)

This will submit your pull request which will result in a notification to the the community maintainers and from there the changes will be reviewed. You will get feedback indicating if anything needs to be modified or if things look good we will merge the changes into the master branch.

There you have it, you've got all of the information that you will need to know for contributing to an open source project. Looking forward to your contributions and keep on coding!
