---
published: false
layout: post
title: "I can't pay"
date: "2014-03-02 18:20"
categories: magento
---

It's great to use One Page Checkout, but it's broken. We can't continue after Shipping step.

We can fix the base template

    app/design/frontend/base/**default/template/checkout/onepage/payment.phtml**

Or our custom template (e.g. magento-foundation theme)

    app/design/frontend/magento-foundation/**default/template/checkout/onepage/payment.phtml**

There we need to **add an id** attribute to the following **fieldset** html element (this loads the payment methods):

    <fieldset>
      <?php echo $this->getChildHtml('methods') ?>
    </fieldset>

Change it to the following code

    <fieldset id="checkout-payment-method-load">
      <?php echo $this->getChildHtml('methods') ?>
    </fieldset>

We have added this

    **id="checkout-payment-method-load"**


Source: [Can’t checkout on CE 1.8 - Magento Forum](http://www.magentocommerce.com/boards/viewthread/441003/)
