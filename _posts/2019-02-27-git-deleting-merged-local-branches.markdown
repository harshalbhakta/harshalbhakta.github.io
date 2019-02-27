---
layout: post
title:  "Git : Deleting merged local branches"
date:   2019-02-27 19:48:00 +0530
categories: [git]
---

Once I have worked on a project from sometime, it usually becomes a graveyard of merged branches. These branches have been merged into master and they have probably been deleted from the remote repository.

#### Marie Kondo's Git nightmare

{% highlight bash %}

$ git branch
  19octfixes
  23oct-fixes
  27oct
  2checkout
  activity_tracking
  add-api-for-collection-category-courses
  add-enrolled-course-collection
  add-order-filters
  add-orders-tab
  add-report-mailer
  add_support_for_full_offer_price
  api-calls-for-automated-builds
  apibugfix
  bannerssort
  blog-crud
  bug-fixes
  bugfix
  bugs
  bumprubyrails
  capistranolock
  categories
  categories-api-bug-fix
  category-fix
  clean-up-code
  course-collection-view-all-api-call
  custom-text
  development
  domains
  enrollment-calls
  expanded-categories
  expanded_categories
  expanded_categories_api
  favicon
  favicons
  fix-Contact-us-About-us
  fix-apple-payments
  fix-category-cover-image
  fix-checkout-page
  fix-collection-ratings
  fix-comments
  fix-dashboard
  fix-enroll-for-free-collection
  fix-mailer-function
  fix-overview
  fix_user_show_page
  footer
  forgot-password
  fortrainer-to-teachmore
  imagefixes
  instructors-crud
  ios-in-app-purchases
  ios-in-app-purchases-2
  ios-payments
  landingbugs
  login-signup-fix
  main-landing

{% endhighlight %}

#### The cleanup

Use below commands to check and delete the branches that are merged and are safe to delete.

{% highlight ruby %}

# Check the branches before deleting.
$ for b in `git branch --merged | grep -v \*`; do echo $b; done

# Delete the branches.
$ for b in `git branch --merged | grep -v \*`; do git branch -D $b; done

{% endhighlight %}