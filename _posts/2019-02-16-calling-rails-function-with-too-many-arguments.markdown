---
layout: post
title:  "Calling Rails functions with too many arguments"
date:   2019-02-16 19:30:00 +0530
categories: [rails,coding-convention]
---

A lot of times I end up with models that have too many fields. When I need to create an object for the model I end up passing too many arguments to the create method. My code ended up being too difficult to read. Finally I started following a better way to call such functions.

#### The Bad Way

It's really difficult to read the code here. Specially when I am looking for a specific argument. The code goes out of screen and I need to scroll to check all the arguments. It always frustrates me.

{% highlight ruby %}

order = Order.create! app_id: user.app.id, user_id: user.id, mobile_number: user.mobile_number, email: user.email, name: user.full_name, order_total: order_total, status_code: OrderStatusCode::STARTED, order_type: OrderType.paytm, platform: platform, currency_country_id: user.app.country_id

{% endhighlight %}

#### The Good Way

This seems to be a more natural way of calling a function with large number of arguments. Instead of specifying all the arguments in the same line I started listing them one on each line. The code is now more readable and its a lot easier to find arguments.

{% highlight ruby %}

order = Order.create!(
  app_id: app.id,
  user_id: user.id,
  mobile_number: user.mobile_number,
  email: user.email,
  name: user.full_name,
  order_total: order_total,
  status_code: OrderStatusCode::STARTED,
  order_type: OrderType.payment_gateway,
  platform: platform,
  currency_country_id: user.app.country_id
)

{% endhighlight %}