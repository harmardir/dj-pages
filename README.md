# dj-pages

- Pages app is a simple app that has 2 pages homepage and about page.
- New approach is used to create templates which is craete a single project-level templates directory and place all the templates within it, also making small tweak in ` settings.py ` fiel where we will tell django to alos look in this directory for templates.
- In the project directory ` $ mkdir templates `
- In templates directory ` $ touch home.html `
- In ` settings. py ` we need to tell django the location of our new templates directory, this is a one-line hange to the settings ` DIRS `under `TEMPLATES`:    
  ` 'DIRS':[str(BASE_DIR.joinpath('templates'))], `
  
