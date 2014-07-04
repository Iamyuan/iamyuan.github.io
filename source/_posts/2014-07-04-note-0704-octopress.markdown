---
layout: post
title: "Note_0704-Octpress"
date: 2014-07-04 17:22:14 +0800
comments: true
categories: 
---

Octopress
=====
[ Install ]
----
 
 * Install Git
 * Install ruby
 * Setup Octopress
 
    `git clone git://github.com/imathis/octopress.git octopress`
 
    `cd octopress`
 
 * Install dependencies
 
    `gem install bundler`   [bundle](http://bundler.io)
 
    `rbenv rehash`  
  
    `bundle install`
 
 * Install the defalt Octopress theme
 
    `rake install`
   
 * Set Deploying-Heroku (or [GitHub]) 
  
     Sign up an account
  
    `gem install heroku`
 
 * create a heroku app for deployment
    `heroku create`

  
  [GitHub]: http://octopress.org/docs/deploying/github/
 
 [ Rake ]
-------
 * `rake -T` 
 
 * `rake generate`
 
   `git add .`

   `git commit -m '    '`

   `git push heroku master`

  * `rake new_post`
 
    Enter a title, and then create a new file
     
    Edit the title.markdown
    
 *   
      
    
        
