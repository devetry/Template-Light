# Couscous Light template

## Usage

To use the template, set it up in your `couscous.yml` configuration file:

```yaml
template:
    url: https://github.com/LaunchCodeEducation/Template-Light
```

## Configuration

Here are all the variables you can set in your `couscous.yml`:

```yaml
# Base URL of the published website
baseUrl: http://education.launchcode.org/module

siteTitle: My project

# Google Custom Search Engine ID
cseId: 222222222222222222222:aaaaaaaaaaa

# Google Analytics ID
gaId: UA-55555555-5

# The left menu bar
menu:
    items:
        home:
            text: Home page
            # You can use relative urls
            relativeUrl: doc/faq.html
        foo:
            text: Another link
            # Or absolute urls
            absoluteUrl: https://example.com
```

Note that the menu items can also contain HTML:

```yaml
home:
    text: "<i class=\"fa fa-github\"></i> Home page"
    relativeUrl: doc/faq.html
```

## Menu

To set the current menu item (i.e. highlighted menu item), set the `currentMenu`
key in the Markdown files:

```markdown
---
currentMenu: home
---

# Welcome
```

## Local development

For local development, clone the template and use the following template config:

```yaml
template:
    directory: ../Template-Light
```

To run and test your site or template locally, it's recommended that you use the Phar installation method from the [Couscous documentation](http://couscous.io/docs/getting-started.html).

### Note on deploying static changes

When making updates to static files (CSS, JS, etc.) you may need to delete the file(s) from the project that is using the template and rebuild, in order to force the new file to be deployed.