---
published: false
layout: post
title: Error Installing Magento 1.7
date: "2014-03-02 18:08"
categories: magento
---

## Why installing Magento 1.7?

Some businesses consider this version because lots of plugins support it.

## When is an error appearing on Magento 1.7 installation?

Always.

The error message is **PHP Extensions “0” must be loaded**

But Keep Calm, let's solve this just modifying one line in config file.

Look near **line 71** in file **app/code/core/Mage/Install/etc/config.xml**

You will find this

    <extensions>
      <pdo_mysql/>
    </extensions>

Change it to the following

    <extensions>
      <pdo_mysql>1</pdo_mysql>
    </extensions>

Source: [PHP Extensions “0” must be loaded , while installing magento-1.7.0.1.tar.bz2 - Magento Forum](http://www.magentocommerce.com/boards/viewthread/284882/)
