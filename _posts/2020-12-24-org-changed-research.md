---
layout: distill
title: Org Mode Changed My Research Workflow
date: 2020-12-24
description: A high-level overview of my current personal setup with Emacs and Org Mode for research and task management.
tags: [Task Management, Organization, Workflow, Text Editor]
categories: productivity-posts
giscus_comments: true
thumbnail: assets/img/blog_post_images/12_2020/research_roaming.png
---

<div class="l-page">
  {% include figure.liquid path="assets/img/blog_post_images/12_2020/research_roaming.png" class="img-fluid rounded z-depth-1" zoomable=true %}
</div>

## What is Org Mode?

[Org Mode](https://orgmode.org/) is a popular extension of the text editor Emacs. It has often been praised as a means of codifying one's daily activities and agendas. In an age when a litany of productivity apps and toolkits promise to increase your efficiency while at work, Org Mode remains a steadfast choice for the do-it-yourself (DIY)-oriented crowd.

## Why is task management important?

[Task management](https://en.wikipedia.org/wiki/Task_management) is necessary for making continuous progress on any project. Many different methodologies aim to encompass all the best principles of task management, and one of the most well-known and successful of these methodologies is called [Getting Things Done](https://gettingthingsdone.com/) (GTD) introduced by David Allen. Its core philosophy is relatively simple: document each task you must accomplish in a given day to free up your mind to exert maximum focus on the task at hand. This process, as you can imagine, requires consistent discipline to execute it effectively.

## What is the connection between GTD and Org Mode?

Org Mode allows its users to build [custom agendas](https://orgmode.org/manual/Agenda-Views.html) as they see fit, further letting users connect documents, web content, and even emails together using generic links (e.g. Think hyperlinks for any kind of resource). Given this functionality, [others](https://orgmode.org/worg/org-gtd-etc.html) have taken the liberty to create entire GTD-inspired workflows using Org Mode. Once again, the purpose of doing so is to ease the intellectual burden of having to remember each thing you have to accomplish each day.

<div class="l-body">
  {% include figure.liquid path="assets/img/blog_post_images/12_2020/gtd_with_org_mode.png" class="img-fluid rounded z-depth-1" zoomable=true %}
</div>

## GTD Configuration

After several weeks of research (no pun intended), I discovered an [Org Mode setup](https://blog.jethro.dev/posts/org_mode_workflow_preview/) designed by [Jethro Kuan](https://www.jethro.dev/) that met many of my needs for a productive, organized GTD workflow. Like several others, I opted to house my GTD workflow directories inside my Dropbox directory to enable cloud-based syncing between all my devices (i.e. smartphone, desktop, laptop, etc.).

<div class="l-body">
  {% include figure.liquid path="assets/img/blog_post_images/12_2020/dropbox_gtd_org_dir.png" class="img-fluid rounded z-depth-1" zoomable=true %}
</div>

Out of the box, simply changing the GTD directory file paths to point to my newly-created Dropbox GTD directories worked great for getting my laptop and desktop quickly configured for syncing my daily agenda with Org Mode. However, I had to use a slightly different approach to sync my Org Mode agenda to my Android smartphone.

<div class="l-body">
  {% include figure.liquid path="assets/img/blog_post_images/12_2020/dropbox_gtd_calendars_dir.png" class="img-fluid rounded z-depth-1" zoomable=true %}
</div>

For this use case, I chose to download and install [Orgzly](http://www.orgzly.com/), an (at the time of my writing this) Android-only mobile app that can correctly parse and understand Org Mode syntax in .org files. What appears to be an IOS-equivalent to Orgzly, [beorg](https://apps.apple.com/us/app/beorg-to-do-list-agenda/id1238649962), may also allow you to conveniently manage your cloud-synced Org Mode agendas. I cannot confirm this, nonetheless, as I do not currently own any iPhones with which to test the notion.

In Orgzly, after configuring the app to point to my Dropbox-designated GTD directories (i.e. (1) dropbox:/Documents/Org/GTD/Org/ and (2) dropbox:/Documents/Org/GTD/Org/Calendars), I also chose to add a few custom [searches](http://www.orgzly.com/help#search) that display tasks that are scheduled today (i.e. "Scheduled") and tasks that are due today (i.e. "Due"). I tend to use the "Scheduled" search more than other searches as it quickly gives me an overview of what I have lined up for the day without distracting me with tasks to be completed in the future (GTD, remember?).

<div class="l-body">
  {% include figure.liquid path="assets/img/blog_post_images/12_2020/orgzly_searches.png" class="img-fluid rounded z-depth-1" zoomable=true %}
</div>

## MindMeld Configuration

So by now, we have a robust means of scheduling each task for the day in a platform-agnostic manner. But how did all this affect my research workflow? To answer this, we'll have to turn to **MindMeld**, a collection of thoughts, notes, and writings for my digital exobrain largely inspired by [Braindump](https://github.com/jethrokuan/braindump) (also by Jethro Kuan).

<div class="l-body">
  {% include figure.liquid path="assets/img/blog_post_images/12_2020/dropbox_mindmeld_dir.png" class="img-fluid rounded z-depth-1" zoomable=true %}
</div>

Much of the layout and ideas behind MindMeld has already been well-documented by Jethro in his [blog posts](https://blog.jethro.dev/posts/capturing_inbox/) on pairing GTD and Org Mode. However, MindMeld builds on top of Braindump by adding several new [org-capture](https://orgmode.org/manual/Capture.html) templates and directories. MindMeld also incorporates a running BibTeX bibliography that, with [org-ref](https://github.com/jkitchin/org-ref), can be used to cleanly arrange and index a copious number of BibTeX entries.

I have used MindMeld to write several reports, proposals, and [Beamer](<https://en.wikipedia.org/wiki/Beamer_(LaTeX)>) presentations to-date, and I can say from my initial impressions of the system that it has drastically improved the speed at which I can put together well-formatted technical documents (references and all!). I have also been able to make connections between concepts that I wouldn't have been able to make before thanks to wonderful Emacs add-ons like [org-roam](https://github.com/org-roam/org-roam). As it turns out, the diagram listed at the beginning of this article was generated using org-roam, and it hopefully gives you a taste of what is possible for making new connections between related ideas with Org Mode.

I continually update a GitHub repository called [dots](https://github.com/amorehead/dots) that houses my most up-to-date Emacs and Org Mode config files to make it easier for others to reproduce this GTD research setup. I have been primarily using the Emacs extension [Doom Emacs](https://github.com/hlissner/doom-emacs) for most of my desktop/laptop use of Emacs, and I include in [dots](https://github.com/amorehead/dots) a [directory](https://github.com/amorehead/dots/tree/main/doom_emacs/.doom.d) dedicated to Doom Emacs-related configuration.

My next focus will be on finding out whether MindMeld can be used to facilitate the entire research and development process, that is, whether one can effectively write entire manuscripts in Org Mode. I have suspicions that this may prove more difficult than initially expected, but I am still [optimistic](https://www.youtube.com/watch?v=AP4LX8L7MFM&feature=emb_logo) about the possibility.

That's all from me for now. Take care, and keep in mind with great productivity comes great responsibility (or so I tell myself).

**Alex**
