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

**Tech:** 
- Wordpress 
- GeneratePress

**Plugins:** 
- Woocommerce
- WP Rocket
- WPML
    
## Getting Started
1. Review the [Developer Docs](#) before starting your first project. 
2. Reference [Terminal Basics](#) and [Setup Your local Environment](#) sections.
3. Clone this repository using Bitbuckets clone button at the top right of this repo. Choose HTTPS. 


### Clone this repo  
The following will create a folder with the {$pojectname} in the current directory.

``` 
git clone https://{$devname}@bitbucket.org/{$company}/{$projectname}.git 
```

To clone a repo into the current folder without creating another folder, add a dot at the end to designate the files should be cloned into the current folder 

``` 
git clone https://{$devname}@bitbucket.org/{$company}/{$projectname}.git . 
```

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

**Push your changes up to the repo**  
```
git push
```



