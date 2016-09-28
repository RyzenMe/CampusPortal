# CampusPortal (Doorkeeper) [![Build Status](https://travis-ci.org/PENGZhaoqing/UcasPortal.svg?branch=master)](https://travis-ci.org/PENGZhaoqing/UcasPortal)

CampusPortal is a campus portals information system for Chinese Academy of Science, which is developed to provide as unified access entrance for the faculties, students and campus application developers.

## Motivation

CampusPortal ultizes [OAuth 2.0](https://oauth.net/2/) protocol to achieve the interactive communication within mulitple heterogeneous web apps, therefore, UcasPortal can act as the main login panel for campus users and web app developers who are going to conncet their apps with CampusPortal. 

* For the campus users, which means faculities and students, UcasPortal is a SSO (Single Sign-on) platform. Once campus users logined in UcasPortal, they could have access to all relative campus applications without providing other username and password.

* For campus applications developers, which means the developers owning the inner campus applications (Campus Libaray System...) and the third-part applications (those ultizes the campus users info to provide their service such as selling take-out food), UcasPortal is the OAuth provider and inforamtion holder.

* Developers could login in UcasPortal and create new apps and configue the OAuth conncetion to owned app. Besides, in UcasPortal, Developers can also decide the target users who they are providing service to. 

And we also have an sample course selection system [CourseSelect_en](https://github.com/PENGZhaoqing/CourseSelect_en) to demonstrate the OAuth interaction. 

## Features

* Multi-role Login (students, teachers, developers and admins)
* Account Mail Acivation (and Password Reset by mail)
* OAuth Provider (other apps can use our OAuth service)
* Access Management (by authorizaiton data tree) 

## ScreenShoot 

<img src="/lib/screenshoot1.png" width="700">

<img src="/lib/screenshoot2.png" width="700">

<img src="/lib/screenshoot3.png" width="700">

<img src="/lib/screenshoot4.png" width="700">

<img src="/lib/screenshoot5.png" width="700">

<img src="/lib/screenshoot6.png" width="700">


## Getting Started

CampusPortal is built based on the [Doorkeeper](https://github.com/doorkeeper-gem/doorkeeper) gem to achieve related OAuth function.
This app also relies on rails_admin gem for back-end management and bootstrap for front end rendering.

Before getting started, make sure your system has the follwoing requirements:

#### System Prerequisities (Mac OS/Linux)
* [Bundler](http://bundler.io/)
* [Git](https://help.github.com/articles/set-up-git)
* [Rails 4.2.x](http://rubyonrails.org/download)
* [RubyGems](https://rubygems.org/)
* [Ruby 2.2.x](https://www.ruby-lang.org/en/downloads/)
* ...

#### Ruby Dependencies

* [Doorkeeper](https://github.com/doorkeeper-gem/doorkeeper)
* [Rails_admin](https://github.com/sferik/rails_admin)
* [Bootstrap](http://getbootstrap.com/) 
* ...

### Installation

Execute the following code in local machine and go to `localhost:3000` in your browser

```
$ git clone https://github.com/PENGZhaoqing/CampusPortal
$ cd CampusPortal
$ bundle install
$ rake db:migrate
$ rake db:seed
$ rails s 
```

### Configuration

* Mail Service

1.create a file `conf/local_env.yml`, and fill in as followings:

```
163MAIL_USENAME: 'your_mail_account@163.com'
163MAIL_PASSWORD: 'your_mail_account_password'
```
 
2.modify the the code in 'app/mailers/application_mailer.rb'





### Usage

1.Student Login

account:`student1@test.com`

password:`password`

2.Teacher Login

account:`teacher1@test.com`

password:`password`

3.Developer Login

account:`developer1@test.com`

password:`password`

4.Admin Login

account:`admin@test.com`

password:`password`

the number in account can be replaced by 2,3... and so on

## Deployment

### Prerequisities
* Ubantu 14.04 
* [Phusion passenger](https://www.phusionpassenger.com/)
* [Apache] (https://httpd.apache.org/download.cgi) 




 
 

