---
title: "Getting Started"
date: 2024-04-05
---

# Generating a static website

1. Install Hugo Static Website generator
    * [Official Website Documentation](https://gohugo.io/)
2. Hugo new site "Website name"
3. Use a theme as the backbone of the site
    * [Follow Hugo doc to add default theme](https://gohugo.io/getting-started/quick-start/)
    * Or create your theme from scratch 
        ```bash
        hugo new theme "theme name"
        ````

# Hosting the website

## Using Github Pages for public repositories
1. Go to your repository settings on Github
    * Go to the "Pages" section
    * Select "Github Actions" as the source for the build and deployment
2. [Copy the official Hugo documentation Github workflow in a new file](https://gohugo.io/hosting-and-deployment/hosting-on-github/)
    * Filepath: .github/workflows/hugo.yml
3. Update the hugo.toml baseURL to fit you github account path : https://"account name".github.io
    * For our website, it deployed the website to https://SimpleOpenSource.github.io/simpleopensource.com

### Use custom domain
1. Add a CNAME record to your provider
    * Name = "@" or domain name
    * Content = github base url such as "simpleopensource.github.io"
2. Add another CNAME record
    * Name = "www"
    * Content = github base url such as "simpleopensource.github.io"
3. Add a Page Rule
    * URL = www."domain name".com/*
    * Parameter = "Always use https"
4. Enable Full SSL/TLS encryption for the domain
5. Add a CNAME to your repository
    * Create a file named "CNAME"
    * Add the domain name such as "simpleopensource.com"
6. Access Github repository settings
    * In the "Pages" section, enter your custom domain name such as "simpleopensource.com"

Your website is now available at your custom domain with free hosting!
* Be careful not to generate too much traffic or Github will stop the hosting. [See documentation](https://docs.github.com/en/pages/getting-started-with-github-pages/about-github-pages#limits-on-use-of-github-pages)

