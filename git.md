# Product Vision Document

### Notes by Gannon Darcy

1. Git is a tool we use as developers to keep a record/working history of our work and share our code with other developers.

2. Flow
   - no more forking!
   - clone the repo from the master branch
   - create a FEATURE branch (example: front-end-login)
   - do an inital commit and then open a "Draft PR" immediately (the down arrow on the green "Create Pull Request" button on Github. is where you can find this).
   - your TL as a reviewer of the PR.
3. Your team owns the projects. These are open sourced and you have them forever.

   - star your Labs repos and add to your GitHub Profile top 6

4. Merge Conflicts
   -when you're working on a branch, master gets updated and you do a pull and merge from master to your branch and there is a conflict (a file you're working on was updated in master and now git doesn't know who is right).
   -If you're not sure what to do, pull in your TL or SL for help.
   -install GitLens on VSCode to help you know who was working on each line of code, this can help you DM the person whose code you're in conflict with and sort things out
   -accept incoming changes to have the final code be what was on master
   -accept current changes to have the final code be what is on your branch.

5. extra resoures

   - Nick used to work for github for several years. He made this for lambda students to take git-fu to the next level for labs: https://www.youtube.com/watch?v=Z71DfROQsMs&amp=&feature=youtu.be
   - for git branching https://learngitbranching.js.org/
   - got to the #git channel because there is a lot of gold in there too.

   Foundational Resources:
   Writing good commit messages: https://chris.beams.io/posts/git-commit/
   Learn Git Branching: https://learngitbranching.js.org/

6. Free Courses:

   - Upcase — Mastering Git: https://thoughtbot.com/upcase/mastering-git
   - Udacity — Version Control with Git: https://www.udacity.com/course/version-control-with-git--ud123

7. Paid Courses:
   - Pluralsight — How Git Works: https://app.pluralsight.com/library/courses/how-git-works/table-of-contents
   - Pluralsight — Mastering Git: https://app.pluralsight.com/library/courses/mastering-git/table-of-contents

Things to keep pinned in your browser:
Git Flight rules: https://github.com/k88hudson/git-flight-rules (edited)

6. Do everything in the command line. GUI's are not where you should be spending your time.

7. PRs are a short story /self contained unit of work... the commits are like a paragraph of that story. Your rarely if ever should have 1 commit for a PR. But you most likely don't need a ton of commits per PR (if you do.... the PR is most likely too big).

8. Your TL's will be setting up staging server. You will be expected to use the staging server flow/set up.
