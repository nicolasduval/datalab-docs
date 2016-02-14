---
title: Datalab API Reference

language_tabs:
  - JSON

toc_footers:
  - <a href='http://github.com/tripit/slate'>Documentation Powered by Slate</a>

includes:
  - companies
  - projects
  - timecode
  - errors

search: true
---

# Introduction

Welcome to the Datalab API! 

# Installation
- Clone the repository [datalab-api](https://github.com/nicolasduval/datalab-api.git)
- Make sure you have postgresql 9.3 installed

Run the following commands

- ```$ bundle install```
- ```$ rake db:migrate```
- ```$ rails console```



# API Versions

Specify the version of the API in the request header.

`Accept : apllication/json.v1`

<aside class="notice">
  If not set the the current version of the API will be used.
</aside>

