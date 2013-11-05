Octopress Apache Alias Generator
======================================

A Jekyll/Octopress plugin for generating redirect rewrites in htaccess for post and pages.
The aliases are set in the YAML Front Matter.

Originally idea came from the following plugin: [jekyll_alias_generator](https://github.com/tsmango/jekyll_alias_generator)
It generates folders and files for redirects, if you use apache then you can easly do this in htaccess (and this keeps your public folder a bit cleaner).

**The plugin will only work if your deploy static pages and have an apache server (like dreamhost)**

### Usage
Place the full path of the alias (place to redirect from) inside the
destination post's YAML Front Matter. One or more aliases may be given.

Example Post Configuration:

    ---
      layout: post
      title: "How I Keep Limited Pressing Running"
      alias: /post/6301645915/how-i-keep-limited-pressing-running/index.html
    ---

Example Post Configuration:

    ---
      layout: post
      title: "How I Keep Limited Pressing Running"
      alias: [/first-alias/index.html, /second-alias/index.html]
    ---
    
### htaccess
An htaccess will automatically be generated with the correct redirections.
In case you would like to add your own htaccess rules (e.g page caching, a good template can be found [here](https://github.com/h5bp/html5-boilerplate/blob/master/.htaccess))
add a **_htaccess** file to your source directory with your rules/setup. The plugin will then append the redirect rules at the bottom of the file.
    
Make sure you **dont** have a **.htaccess** file in your source folder (when using Octopress) or sites folder (when using Jekyll), rename it to **_htaccess**.

### Bugs
If there are any bugs or problems, leave a report on github. More information at http://www.fritz-hut.com
