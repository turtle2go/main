---
layout: post
title: AWS EC2
category: clouds
excerpt_separator:  <!--more-->
---

EC2 Definition, Setting, Connect, Stop/Start/Restart/, CLI, Summary

### Definition

`[Amazon EC2(Elastic Compute Cloud)`

Virtual Server, running based on various hardware types provided by AWS.

`AMI(Amazon Machine Image)`

AWS pre-built OS template(OS,APPs), provided by AWS or built by customers

`EC2 Storage Type`

  * Instance Store-Backed (Only for instance)
  : Instance store won't be available once the instance stop/terminate
    Sequential process for temporary files, cache, swap(could be deleted)
  * EBS (elastic Block Store, High availability and durability)
  : EBS would be available still although the instance create/delete
    Persistent operation such as OS, DB

### Setting

`Pre-requisite`

  * Key pairs for SSH between instance and administration PCs
  * Security group and firewall rules

`EC2 Creation procedure`

  ```scss
  * Select AMI Type
  * Select instance Type
  * Configure instance settting
  * Add Storage
  * Define instance tags
  * Congigure security Setting
  * Check instance status for Creation
  * Define Key pairs with existing key or new one
  * Assign EIP and link to EC2 service through internet
  * EC2 service testing
  ```
  
  ```
  ---
  # Jekyll needs front matter for SCSS files
  ---

  $sidebar-bg-color: #ac4142;
  $link-color: #ac4142;
  $sidebar-sticky: false;
  @import "hydeout";
  ```

  ```scss
  $sidebar-bg-color: #202020 !default;
  $sidebar-sticky: true !default;
  $layout-reverse: false !default;
  $link-color: #268bd2 !default;
  ```
