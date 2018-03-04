---
layout: post
title: AWS EC2
category: clouds
excerpt_separator:  <!--more-->
---

EC2 Definition, Setting, Connect, Stop/Start/Restart/, CLI, Summary

### Definition

Amazon EC2(Elastic Compute Cloud)
Virtual Server, running based on various hardware types provided by AWS.

AMI(Amazon Machine Image)
AWS pre-built OS template(OS,APPs), provided by AWS or built by customers

EC2 Storage Type
```scss
  * Instance Store-Backed (Only for instance)
  ; Instance store won't be available once the instance stop/terminate
    Sequential process for temporary files, cache, swap(could be deleted)
  * EBS (elastic Block Store, High availability and durability)
  ; EBS would be available still although the instance create/delete
    Persistent operation such as OS, DB
```

### Setting

[pre-requisite]

Required:

  * Key pairs for SSH between instance and administration PCs
    Security group and firewall rules

[EC2 Creation]

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



To override these variables, create your own `assets/css/main.scss` file.
Define your own variables, then import in Hydeout's SCSS, like so:

```
---
# Jekyll needs front matter for SCSS files
---

$sidebar-bg-color: #ac4142;
$link-color: #ac4142;
$sidebar-sticky: false;
@import "hydeout";
```

See the [_variables](_sass/hydeout/_variables.scss) file for other variables
you can override.

You can also insert custom head tags (e.g. to load your own stylesheets) by
defining your own `_includes/custom-head.html` or insert tags at the end
of the body (e.g. for custom JS) by defining your own
`_includes/custom-foot.html`.

### New Features

* Hydeout also adds a new tags page (accessible in the sidebar) and a new
  "category" layout for dedicated category pages.

* Category pages are automatically added to the sidebar. All other pages
  must have `sidebar_link: true` in their front matter to show up in
  the sidebar.

* A simple redirect-to-Google search is available. If you want to use
  Google Custom Search or Algolia or something with more involved,
  override the `search.html`.

* Disqus integration is ready out of the box. Just add the following to
  your config file:

  ```yaml
  disqus:
    shortname: my-disqus-shortname
  ```

  If you don't want Disqus or want to use something else, override
  `comments.html`.

* For Google Analytics support, define a `google_analytics` variable with
  your property ID in your config file.

There's also a bunch of minor tweaks and adjustments throughout the
theme. Hope this works for you!
