---
layout: essay
type: essay
title: Let's Talk Semantics
# All dates must be YYYY-MM-DD format!
date: 2021-10-07
labels:
  - Web
  - UI
  - Semantic UI
  - Frameworks
published: false
---
  This week was my first experience with Semantic UI, and UI Frameworks in
general. Up until this point, I've designed all of my projects in pure HTML,
JavaScript, and CSS. Writing in pure HTML with some simple CSS does have
some advantages, and I think it's somewhat unfairly maligned - these pages
load remarkably quickly and require very little bandwidth, have excellent
compatibility with older devices, and are easily accessible for the
disabled. Some large news sites - CNN and NPR, I know for sure - maintain
basic, text-only versions of their main websites, precisely so that people
on low bandwidth connections in times of disaster or who require certain
accessibility devices can still access information.

  However, these websites are also extremely difficult to give a modern
appearance to, you're quite limited in the type of elements you can
introduce, and they tend to break on mobile devices, owing to the small
screen sizes. Relying on bitmaps for icons and backgrounds also has the
issue that it doesn't scale to different screen resolutions, as your site
will either look freakishly large on a lower resolution or absolutely tiny
on a modern 4K display. This is where a UI Framework, such as Semantic UI,
comes in handy - Semantic UI provides a bunch of useful models with nifty
features, such as automatically adjusting for a smaller screen size,
dynamically resizing based on the amount of content in a component, and
making it really easy to create complex layouts.

  How easily, you ask? I wondered that myself at first - does the additional
work of importing another dependency and needing to maintain it, as well as
the effort to learn an additional toolkit on top of base Javascript, offset
the benefits from the library? In turns out, the answer is definitely not.
For one of our very first assignments, we were required to create a replica
of a real website, [islandsnow.com](https://islandsnow.com). The replica
version we created wasn't an exact match - the fonts were slightly
different, some of the spacing was off, and it was missing some of the
auto-generated content. However, it was a *stunningly* close recreation,
including not only the original set of icons and layout, but also the
advanced drop down menus, the input field for an email address, and so on -
it really looked like a professional website, with relatively little work
needed to achieve it. Even though I've fallen quite a bit behind this week
and haven't mastered Semantic yet, I'm very impressed with its capabilities
so far and I'd be hard pressed to design a website without it.

  That said, I'm a little concerned about how Semantic UI (and UI frameworks
in general) play with each other once you start using multiple in the same
project. Semantic UI seems to be pretty benign at this from my experiences
so far, but generally speaking, frameworks impose a particular design model
on your project. In Semantic UI's case, this seems to be that in exchange
for using Semantic's components, you get a design that scales well to a wide
variety of screen sizes, without having to worry about manually rearranging
your site's contents or adjust for the lower precision of a finger instead
of a mouse or stylus. However, in exchange, you're making the bargain that
Semantic gets to decide how your components (and potentially entire website)
look at any given time. By itself this is pretty harmless, as the only
alternative is native HTML components - but once we introduce other
frameworks that might also be designed to adjust for mobile clients, I
wonder how I'm going to keep a cohesive layout and style between Semantic's
and other frameworks' components.
