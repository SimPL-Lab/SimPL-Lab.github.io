# How to use [SimPL Lab](https://simpl-lab.github.io/) github blog
Written by Jeongwon Park,
Modified by Hoyong Choi

## Based on [Minimal Mistakes Jekyll theme](https://mmistakes.github.io/minimal-mistakes/)

[![LICENSE](https://img.shields.io/badge/license-MIT-lightgrey.svg)](https://raw.githubusercontent.com/mmistakes/minimal-mistakes/master/LICENSE)
[![Jekyll](https://img.shields.io/badge/jekyll-%3E%3D%203.7-blue.svg)](https://jekyllrb.com/)
[![Ruby gem](https://img.shields.io/gem/v/minimal-mistakes-jekyll.svg)](https://rubygems.org/gems/minimal-mistakes-jekyll)
[![Tip Me via PayPal](https://img.shields.io/badge/PayPal-tip%20me-green.svg?logo=paypal)](https://www.paypal.me/mmistakes)
[![Donate to this project using Buy Me A Coffee](https://img.shields.io/badge/buy%20me%20a%20coffee-donate-yellow.svg)](https://www.buymeacoffee.com/mmistakes)

## Update note
### 2024-06-21 update
Open blog (ver 1.0)
### 2024-11-19 update
교수님 사진 링크 수정 (로컬 서버에서 운영서버로 변경) (http://127.0.0.1:4000) -> (https://simpl-lab.github.io/) <br>
Home의 교수님 사진은 _config.yml->avartar에서 변경
### 2024-12-30 update1
Recent Post 수정 (index.html에 Front Matter 추가)
~~~
---
layout: home
author_profile: true
classes: wide
---
~~~
없을 시 _config.yml에서 index.html을 불러오지 못함 -> 404에러 뜸
### 2024-12-30 update2
_config.yml에서 baseurl 수정 (문자열을 의미하는 "" 추가,null로 인지될 수 있는 상황 방지)
<h3>2024-12-30 인수인계용 코드 설명서</h2>

<h4>1. 포스트 추가 (중요)</h3>
<p>_posts에서 <code>.md</code> 파일 업로드 (파일명 뒤에 <code>.md</code> 붙여야 함)<br>
_config.yml의 Recent Post는 <code>0000-00-00-파일이름.md</code> 형식을 인식</p>

<h4>2. 이미지 추가 (중요)</h3>
<p>_assets 내의 images에 추가</p>

<h4>3. 연구실 인원 추가 및 변경 (중요)</h3>
<p>_pages 내의 <code>people.md</code> 파일 수정</p>

<h4>4. 사이트 내 글 변경 (Home, Publication, Post 등)</h3>
<p>_pages 내의 md 파일 수정 (3번과 동일)</p>

<h4>5. 홈페이지 URL 변경</h3>
<p>_config.yml에서 <code>url</code>, <code>baseurl</code> 설정 가능</p>

<h4>6. 사이트 전반적인 설정 및 레이아웃 변경</h3>
<p>_config.yml에서 이미지, 텍스트 등 변경 가능<br>
사이트 레이아웃 및 메인 화면은 <code>index.html</code>에서 수정 가능<br>
<code>index.html</code>은 루트 폴더 (main branch)에 위치</p>


## Manual
### - set up
Sign up github -> Install git, Ruby, Jekyll
### - For building a new blog 
clone github blog theme(minimal mistakes) -> make repository(SimPL-Lab.github.io) -> rename the folder (SimPL-Lab.github.io)(maybe not necessary) -> push into repository
### - For updating this blog
clone this repository(SimPL-Lab.github.io) -> update content -> open cmd -> push into repository (see below process)  
**Update would take 5~10 minutes**

~~~md
git init
git remote remove origin
~~~
git remote remove origin (To prevent just in case when you already have remote origin)
~~~ 
git remote add origin https://github.com/SimPL-Lab/SimPL-Lab.github.io.git
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
