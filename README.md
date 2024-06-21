# How to use [SimFL Lab](https://simfl-lab.github.io/) github blog
Written by Jeongwon Park

## Based on [Minimal Mistakes Jekyll theme](https://mmistakes.github.io/minimal-mistakes/)

[![LICENSE](https://img.shields.io/badge/license-MIT-lightgrey.svg)](https://raw.githubusercontent.com/mmistakes/minimal-mistakes/master/LICENSE)
[![Jekyll](https://img.shields.io/badge/jekyll-%3E%3D%203.7-blue.svg)](https://jekyllrb.com/)
[![Ruby gem](https://img.shields.io/gem/v/minimal-mistakes-jekyll.svg)](https://rubygems.org/gems/minimal-mistakes-jekyll)
[![Tip Me via PayPal](https://img.shields.io/badge/PayPal-tip%20me-green.svg?logo=paypal)](https://www.paypal.me/mmistakes)
[![Donate to this project using Buy Me A Coffee](https://img.shields.io/badge/buy%20me%20a%20coffee-donate-yellow.svg)](https://www.buymeacoffee.com/mmistakes)

## Update note
### 2022-03-05 update
Open blog (ver 1.0)

## Manual
### - set up
Sign up github -> Install git, Ruby, Jekyll
### - For building a new blog 
clone github blog theme(minimal mistakes) -> make repository(SimFL-Lab.github.io) -> rename the folder (SimFL-Lab.github.io)(maybe not necessary) -> push into repository
### - For updating this blog
clone this repository(SimFL-Lab.github.io) -> update content -> open cmd -> push into repository (see below process)  
**Update would take 5~10 minutes**

~~~md
git init
git remote remove origin
~~~
git remote remove origin (To prevent just in case when you already have remote origin)
~~~ 
git remote add origin https://github.com/SimFL-Lab/SimFL-Lab.github.io.git
git add .
git commit -m "write what is updated"
~~~
Commit is for writing a memo
~~~
git push -u origin main
~~~
git push origin (branch name)

when push rejected with this message 'fetch first'  
use this code below and push again
~~~
git pull --rebase origin main
~~~
git pull --rebase (remote repository nickname) master  

## Customizing
### - For layout setting
* _config.yml (Default layout setting)
* /_data/navigation.yml (menu on top)
* /_sass/minimal-mistakes/skins/_contrast.scss (blog theme color)
* /_sass/minimal-mistakes/_variables.scss (width)
* /_sass/minimal-mistakes/_reset.scss (font)
* /_sass/minimal-mistakes/_sidebar.scss ***and*** /_layouts/default.html (back to top button, [reference](https://masunii.github.io/blog_custom/top_button/))
* /_includes/head/custom.html (favicon, [reference](https://danggai.github.io/github.io/Github.io-%ED%8C%8C%EB%B9%84%EC%BD%98-%EC%88%98%EC%A0%95%ED%95%98%EA%B8%B0/))
* /_sass/minimal-mistakes/_masthead.scss (menu bar font, [reference](https://devinlife.com/howto%20github%20pages/github-pages-settings/))
* /_layouts/home (recent posts 'list' -> 'grid' ({% assign entries_layout = page.entries_layout | default: 'grid' %}) )

### - For updating page
> * Home  
index.html ***(Use HTML language)***
> * People  
/_pages/people.md ***(Use Markdown language)***
> * Research  
/_pages/research.md ***(Use Markdown language)***
### - For creating a new post
1. make an md(markdown) file (file name format: yyyy-mm-dd-[post title].md)
2. write title (optional: excerpt)
### - For checking with your local server before push
~~~
gem install bundler
bundle exec jekyll serve
~~~
~~~
jekyll serve
~~~
[Local server (http://127.0.0.1:4000)](http://127.0.0.1:4000)  

**How to handle this error** - `require': cannot load such file -- webrick (LoadError)
~~~
bundle add webrick
jekyll serve
~~~

## Reference
### Korean
[GitHub Pages 블로그 따라하기](https://devinlife.com/howto/)  
[[A to Z] Github Blog Jekyll minimal mistakes](https://eona1301.github.io/a_to_z/GithubBlog/#00-github-blog-a-to-z)  
[Github Page 블로그 만들기](https://jinhoooooou.github.io/tags/#github-page)  
[github.io minimal mistake](https://danggai.github.io/tags/#github-io)  
[GitHub Blog 시작하기](https://honbabzone.com/jekyll/start-gitHubBlog/)  
[[Github 블로그] utterances 으로 댓글 기능 만들기](https://ansohxxn.github.io/blog/utterances/)
### English
[W3 schools - HTML](https://www.w3schools.com/html/default.asp)
[nbviewer (pdf url)](https://nbviewer.org/)
