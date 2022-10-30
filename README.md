## Pages App

Pages app is a simple app that has 2 pages homepage and about page.

### Templates

- New approach is used to create templates which is craete a single project-level templates directory and place all the templates within it, also making small tweak in ` settings.py ` fiel where we will tell django to alos look in this directory for templates.
- In the project directory ` $ mkdir templates `
- In templates directory ` $ touch home.html `
- In ` settings. py ` we need to tell django the location of our new templates directory, this is a one-line hange to the settings ` DIRS `under `TEMPLATES`:    
  ` 'DIRS':[str(BASE_DIR.joinpath('templates'))], `

### Class-based Views

Class-based views provide an alternative way to implement views as Python objects instead of functions. They do not replace function-based views, but have certain differences and advantages when compared to function-based views:

- Organization of code related to specific HTTP methods (GET, POST, etc.) can be addressed by separate methods instead of conditional branching.
- Object oriented techniques such as mixins (multiple inheritance) can be used to factor code into reusable components.

- In `views.py` :
`class HomePageView(TemplateView):`
    `template_name = 'home.html'`
- In `urls.py` :
`urlpatterns = [path('', HomePageView.as_view(), name='home'),]`

