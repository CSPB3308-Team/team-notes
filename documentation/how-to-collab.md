# How to Contribute

This document will outline steps on how to contribute to the code -- creating issues, assigning them, creating branches, opening Pull Requests (signals the code is ready to be tested, reviewed and merged into `main`)

## Creating Issues
You can create issues from the [Project Board](https://github.com/orgs/CSPB3308-Team/projects/1) or on Individual Repositories. On the Project Board, scroll the bottom of any column, and create...

**IMPORTANT: Make sure it's assigned to the correct repo! If you hit the `#` key when you start typing, you can select a repo to attribute it to (front-end, back-end, documentation, etc) and then fill out the details.**

I typically like to keep titles short and add the details in the Description, to make the automatic branch names easy (will get into below)

Once you have your issue created, you'll be left with something like this:
![alt text](img/Screenshot_2025-02-19_at_5.20.08_PM_optimized.png)

Now you fill out the important stuff!

### Issue Details
There's some nice-to-have stuff here, like labels but the important stuff to do here:
- `Assign` a team member or yourself
- Under `Projects`, set a Status. Ready indicates that this is Ready for Pickup.
- When you're ready to work on this issue, `Create a Branch` to automatically link the ticket to the code branch you'll be working on:

![alt text](<Screenshot 2025-02-19 at 5.29.30 PM.png>)
Here all you have to do is confirm the repo is correct, and the source is correct (usually main, unless you're blocked by an in-progress ticket that will soon be merged in) and create the branch!

## Code the Feature!
Go to the repo on your local machine and run `git fetch -a`, to grab any changes. You should see your new branch appear in the process running. When that finishes you can run `git checkout <branch-name>` so in this example I would run `git checkout 3-test-issue` to pivot to that new branch. This is why I keep issue titles short, otherwise you'll generate something like `3-adding-a-navbar-to-the-front-page-of-the-frontend` You're ready to build out that feature!

## Pull Requests
Once you're done building and have pushed your code up.