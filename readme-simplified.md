# Project Name
<!-- Brief Description of the Website -->
*An e-commerce website built with WP and Woocommerce*. 

<!-- Quick Access Environment URLs -->
**Production**: [website.com](#)  
**Staging**: [websitestag.wpengine.com](#)  
**Development**: [websitedev.wpengine.com](#)

<!-- Quick Access Important Docs -->
**Docs:**
- [Account Notes](#)
- [Developer Docs](#)
<<<<<<< HEAD
=======

**Tech:** Wordpress, GeneratePress  

**Plugins:** [Woocommerce](#), [WP Rocket](#), [WPML](#)
>>>>>>> 9a165c8 (Creates the simplified file. Removes tech, plugins, and repo clone section)
    
## Getting Started
1. Review the [Developer Docs](#) before starting your first project. 
2. Reference [Terminal Basics](#) and [Setup Your local Environment](#) sections.
3. Clone this repository using Bitbuckets clone button at the top right of this repo. Choose HTTPS. 

<<<<<<< HEAD
=======

### Clone this repo  
The line you copy from the Bitbucket clone button will create a folder with the {$pojectname} in your current directory. To clone a repo into the current directory without creating another folder, add a dot at the end to designate the files should be cloned into the current folder 

``` 
git clone https://{$devname}@bitbucket.org/{$company}/{$projectname}.git . 
```

>>>>>>> 9a165c8 (Creates the simplified file. Removes tech, plugins, and repo clone section)
### Basic Workflow
1. Every Task in JIRA should have its own branch. 
2. You should push your task branch up to the repo and keep it updated. 
3. Merge your task branch into Dev (will auto deploy) and assign to PM for testing.
4. If PMs tests pass, prepare your code for review: Pull Request your Task branch to Staging/Master and assign to Lead Dev.

*For a more indepth look at our Workflow, review the [Company Docs](#)*.

## Git Quick Reference 
Review the [Git Docs](#) for more information on alternate methods to the terminal.

**Update branch**
```
git checkout master
git pull
```

**Create your Task Branch**
```
git checkout master
git checkout -b TASK-123_Update_Plugins
```

**Prepare single edited file to commit**
```
git add /path/to/file.php 
```

**Prepare all currently edited files to commit**
```
git add .
```

**Make a commit**  
*Remember to review our [git commit guidelines](#) in the developer docs*.     
```
git commit -m "TASK-000: Updates Plugin to 1.1.2"
```

**Push your Task branch up to the repo**  
*Your branch TASK-XXX should always be available in the repo*
```
git push
```

**Merge your work into Dev and push**  
*Pushing dev to the repo will activate auto deployment*
```
git checkout dev
git pull dev
git merge --no-ff TASK-XXX
git push
```

## When a Task depends on code from another
Scenario:  
- Your first branch TASK-001 is up for review.
- You want to start your second branch TASK-002 but it depends on the code in the TASK-001 branch.

**Steps:**    
1. Start your TASK-002 branch from TASK-001 branch.  
```
git checkout TASK-001
git checkout -b TASK-002  
```  

Now you can start working on your task with the dependent code and continue with workflow as normal.

2. If TASK-001 changes while in review, you merge it into TASK-002 and dev.    
So lets say there was a bug you had to fix in TASK-001. You do your fix and make your commit:  
```    
git checkout TASK-001
git add .
git commit -m "TASK-001: Fixes some bug"  
git push
```  

Because you made a change to TASK-001, we have to update dev and TASK-002:  
```
git checkout TASK-002
git merge --no-ff TASK-001    

git checkout dev
git merge --no-ff TASK-001   
``` 

This publishes the new changes to dev for testing and brings TASK-002 up to date with the new changes and prevents conflicts later. Now if you have a change in TASK-002 you can merge into dev for testing without issues.If TASK-001 is up for review && TASK-002 is up for review, you can do the same for a TASK-003.  You just have to keep in mind that the more you do this, the more we will have to keep branches up to date by merging up and it can get confusing if we're not careful. So try and keep this at a minimum to prevent confusion. Sometimes it might be better to give Testers and the Lead Developer time to review before moving on and getting too far ahead. 




