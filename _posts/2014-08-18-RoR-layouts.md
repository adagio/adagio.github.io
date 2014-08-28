---
date: "2014-08-18 14:15"
categories: Rails
title: Layouts in Ruby on Rails
---

## RoR Layouts

1. default layout is: application.html.erb

2. if we want to define a layout for name_controller.erb, then we can create name.html.erb

3. if we don't want to use that automatically association by name, then we can explicitly define the layout in the controller. This way:


    layout 'mylayout'

