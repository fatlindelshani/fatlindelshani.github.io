---
layout: post
title: "Hyrje në WordPress"
modified:
categories: blog
excerpt:
tags: []
image:
  feature: blog-code-hero.jpg
date: 2015-07-29T15:39:55-04:00
---

Ka kaluar kohë qysh se u ngazëlleva me faktin se po mbaja diplomën e studimeve të mia në duar, pas plot tri vitesh peripecishë dhe angazhimi studioz serioz.

## Çka është WordPress

### Nën Titull i Dytë

Më poshtë po vendos një copëz code që na mundëson ndryshimin e posteve në faqen bazë:

{% highlight php %}
// Show posts of 'post', 'page' and 'movie' post types on home page
add_action( 'pre_get_posts', 'add_my_post_types_to_query' );

function add_my_post_types_to_query( $query ) {
  if ( is_home() && $query->is_main_query() )
    $query->set( 'post_type', array( 'post', 'page', 'movie' ) );
  return $query;
}
{% endhighlight %}

Për më shumë vizitoni [WordPress Codex][wp-codex] për të lexuar më tepër mbi mundësitë e shumëta që ofron kjo platformë. Për çdo pyetje potenciale më kontaktoni në profilin tim në [GitHub][fe-gh].

[fe-gh]: https://github.com/fatlindelshani
[wp-codex]:  https://codex.wordpress.org
