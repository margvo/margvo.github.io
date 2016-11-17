---
layout: post
comments: true
title:  "My reflections over the first assignment for 1DV022"
date:   2016-11-14 19:34:25
categories: blog
---

* **_What do you think of pre-compiling your CSS?_**

Just like static site generators CSS preprocessors require some time to get used to it.
As for me, I felt slightly nostalgic for good old regular CSS in the beginning,
but in the process I realized and experienced that pre-compiling is not that bad,
especially in combination with a good IDE it really makes your life easier.

  * **_Compare to regular CSS_**

In comparison to regular CSS pre-compiling makes code more readable and  well structured
thanks to the system of mixins, partials and imports as well as using variables and nesting.
With pre-compiling you can avoid code duplication which is often found while using standard CSS.

   * **_Which techniques did you use?_**

I used variables to define, for example, colours or font size. In order to achieve a better visual hierarchy
I applied nesting as well as mixins for media-query. Extends are used to share clearfix and imports help
to separate the code in small pieces. I also used two colour operations (darken, lighten) and one math operation
to calculate a smaller font size.

   * **_Pros and cons?_**

Pre-compiling provides cleaner, better structured and reusable code, decreases the amount of code,
allows you to make calculations directly in CSS, generates "cross-browsing" code. At the same time
it makes it harder to debug your code (wrong line numbers are shown in error messages), increases
building time and requires extra tooling.


***

* **_What do you think of static site generators?_**

This website was my first time when I worked with static site generators. I can say that it is not
a good option for learning web site development as newbie due to possible problems with installation
and relatively difficult content management. But at the same time when you get used to working with
static site generators, it turns out that it is quite convenient and helps you to avoid the duplication
of code which in its turn eases the process of development. Not to mention their other advantages associated
with security, speed, traffic, version controlled content and so on.

  * **_What type of projects are they suitable for?_**

It is hard to name some definite kind of projects because static site generators become more and more
popular and I believe that in combination with other services such as Disqus, Firebase, Swiftype or Olark
they can be a good substitute for almost any traditional dynamic platform. As for now blogging seems to
be the most striking example of applying SSG.

***

* **_What is robots.txt and how have you configured it for your site?_**

It is a file in the TXT format that gives instructions to Web Robots about how to or how no to crawl the website.
In my case I allow the Googlebot service to crawl and index my website by specifying its name as a user-agent
and leaving the "Disallow" directive with no value. At the same time in order to avoid spam messages I tell all other robots
(`User-agent: *`) to stay away from specific files such as contact.html and the folder with my blog posts.

***

* **_What is humans.txt and how have you configured it for your site?_**

It is a file in the TXT format that as a rule contains information about the people who have been involved
in the website developing process as well as some technical information about the website and the software
that has been used to create it. In my case I divided it into four sections: TEAM where I mentioned all people
that had contributed to building my website (not so many actually, only me), SITE where I specified
the last update, language and doctype, SOFTWARE where I listed the programs and services that had been used,
and the THANKS section where I expressed gratitude to some tutorial course that helped me to build my website as well as to a few resources with free images and fonts.

***

* **_How did you implement comments to blog posts_**

I used Disqus, a blog comment hosting service, that generated a piece of the Embed Code. I  provided every
Markdown file that contains the post itself with a variable called `comments` and set its value to TRUE. Then
I placed the Embed Code between `% if page.comments %` and a `% endif %` in my HTML-file with the layout for posts
(after the section with the post content).

***

* **_What is Open Graph and how do you make use of it?_**

Open Graph is a protocol that lets the developer (by adding metadata in the head of the web page) control the visual
representation of the content (preview of the link) on social media. We make use of it first of all by sharing on social media
(for example, Facebook or Twitter) in order to draw more attention and hence a wider audience. In my case I have added five meta tags
in the `head` section of the pages, specifying title, type, image, url and description,
