

[![Version](https://img.shields.io/gem/v/bay_jekyll_theme)](https://rubygems.org/gems/bay_jekyll_theme)
[![Downloads](https://img.shields.io/gem/dt/bay_jekyll_theme)](https://rubygems.org/gems/bay_jekyll_theme)

Bay is a simple theme for Jekyll. [[view live]](https://eliottvincent.github.io/bay)

Inspired by [dangrover.com](http://dangrover.com/). Current theme used at [eliottvincent.com](http://eliottvincent.com/).

![](/screenshot.png)

### Installation


The easiest solution is to [fork this repo](https://github.com/eliottvincent/bay/fork).
If you want to start from a clean website, follow the steps bellow:

Create a new Jekyll website:
```
jekyll new mysite
```

Open `Gemfile` and replace the line:
```
gem "minima"
```
with:
```
gem "bay_jekyll_theme"
```

Open `_config.yml` and replace the line:
```
theme: minima
```
with:
```
theme: bay_jekyll_theme
```
or, for GitHub Pages:
```
remote_theme: eliottvincent/bay
```

Finally, install the dependencies:
```
bundle install
```

and build the website!
```
jekyll serve
```


The website will look somewhat empty at first. That's normal. Follow the next instructions to complete the header and footer components, and the home and blog pages.

### Header
Open the `_config.yml` file and add the following:
```yml
header:
  pages:
    - name: Home
      slug: /     # <-- index.md
    - name: Blog  # <-- blog.md
    - name: Whatever  # <-- whatever.md
```
Re-run `jekyll serve` to see the header updated.

### Footer
Open the `_config.yml` file and add the following:
```yml
footer:
  show_powered_by: true
  contact:
    - name: Email
      value: yourmail@domain.com
      link: mailto:yourmail@domain.com
    - name: WeChat
      value: YourWeChatUsername
      link: "#"
  follow:
    - name: Twitter
      link: http://twitter.com/YourTwitterUsername
      username: "@YourTwitterUsername"
    - name: Facebook
      link: http://facebook.com/YourFacebookUsername
    - name: LinkedIn
      link: http://linkedin.com/in/YourLinkedInUsername
    - name: GitHub
      link: http://github.com/YourGitHubUsername
    - name: Dribbble
      link: https://dribbble.com/YourDribbbleUsername
    - name: Weibo
      link: http://weibo.com/u/YourWeiboUsername
    - name: RSS
      link: /feed.xml
```
Re-run `jekyll serve` to see the footer updated.

### Home page
Create (or edit) the `index.markdown` file and add the following:
```yml
---
layout: home
profile_picture:
  src: /assets/img/profile-pic.jpg
  alt: website picture
---

<p>
  Welcome to mysite!
</p>
```

### Blog page
Create `blog.markdown` file and add the following:
```yml
---
layout: blog
title: Blog
slug: /blog
---

This is an example of a "Blog" page, displaying a list of posts.
<br />
```


Your website is ready!


### Development

#### Run development instance (with hot-reload)
```sh
bundle exec jekyll serve
```

#### Build and publish the gem
```sh
gem build bay_jekyll_theme.gemspec
```

```sh
gem push bay_jekyll_theme-1.x.x.gem
```


###### Git, add commit push를 기억하자!

######  master branch 에서 가지치기 --> 가지 친 branch에서 작업 후 master branch로 다시 편입 

######  _config.yml 에서 내용 변경
######  1. 수정 --> 저장 ctrl+s --> 왼쪽 창에서 + 눌러서 add --> 우측 위, 변경내용간략 설명 후 엔터 
  ######  --> 왼쪽 창 제일 위에서 check버튼 누르기 (commit) 

######  bay
######  마크다운 문법에 맞춰서 글 쓰면 됨 