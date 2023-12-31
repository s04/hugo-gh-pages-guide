# Hugo and Github Pages Guide for quick static websites

# Requirements

- Hugo installed
- New github repo (name does not have to match URL)
- Theme picked (or just follow instructions to use Theme picked below

# Quickstart

https://gohugo.io/getting-started/quick-start/
https://themes.gohugo.io/themes/hugo-paper/

1. Clone Github repo to local machine

2. Setup Hugo

```bash
hugo new site personal-portfolio
cd personal-portfolio
git submodule add https://github.com/nanxiaobei/hugo-paper ./themes/paper
echo "theme = 'paper'" >> config.toml
```

3. Create sample posts

```bash
hugo new blog/first_blog_post.md

echo "This my first blog post." >> ./content/blog/first_blog_post.md
```

4. Change "draft: true" to "draft: false" in the blog post metadata


5. Run Hugo locally to develop

```bash
hugo server -D -t paper
```
6. If you wish, take a look at the theme's webpage for the config option or look at the default_config.toml

7. Hosting Hugo on Github pages follow the official guide here: https://gohugo.io/hosting-and-deployment/hosting-on-github/

- Since this guide doesn't assume you put hugo site at your root, the default action from github pages won't work and neither will the hugo guide actions. You need to adjust the source path where hugo is build. To do this view the "env: \n\t hugo_root:" parameter in the "adjusted_hugo_deploy.yaml"

## DO NOT FORGET TO ADD cname OF YOUR WEBSITE TO A FILED CALLED CNAME FILE AND PUT IT IN YOUR HUGO ROOT FOLDER (not the root of the github repo, they may not be the same)
