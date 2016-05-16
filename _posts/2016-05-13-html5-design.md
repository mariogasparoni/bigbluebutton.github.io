---
layout: page
title: "HTML5 Design"
category: html
date: 2016-05-13 17:34:41
order: 2
---

---
<br>

# Overview

BigBlueButton is an open source web conferencing system for on-line learning.  Our focus is to provide remote students a high-quality online learning experience.

To achieve that goal, we are always looking at ways to improve the teacher and learning experience within our product.  The user interface for BigBlueButton is a major component of that experience. 

Recently, we’ve been working on developing a mobile client for BigBlueButton that has a new user interface.  This document gives you the motivation and design goals for creating a consistent BigBlueButton user interface across platforms (mobile, tablet, and desktop).

<br><br>

# Motivation For Change

project’s inception in 2008, it has evolved and improved with each product iteration (over 14 releases since the initial version), but it has largely remained consistent to the interface in the first release.

Today, with our efforts to create an HTML5 version of BigBlueButton that will target multiple platforms, and the advancement of WebRTC and HTML5, we are able to create one application works across all devices.  In creating the newer version we wanted to also upgrade the user experience.


## Cross platform capability

There are technical challenges to creating a cross-platform product that implements similar functionality on all devices.  The platform provide by the browsers -- especially those that support web real-time communications (WebRTC) frameworks -- are nothing short of amazing.
If you are a busy student, commuting into campus, or a business professional conducting a collaborative online training session, we would like to provide multiple options (web, tablet, phone) to join and participate in a session across different devices.

## User expectations

With the increase of web applications being developed, new standards and best practices have evolved -- such as CSS frameworks, grid systems, layouts, placement and sizing of elements -- that are creating a fairly consistent means of interaction with mobile devices.  

For example, if you used the Slack, Facebook, Twitter, or gMail mobile application, you would notice they all share similar UI conventions that have evolved over the past few years.

When updating the BigBlueButton user interface, we didn’t need to create any entirely new way of interaction; instead, we wanted to provide users a modern, consistent, modular and accessible interface that would be familiar to users based on their experience with other applications.

## Consistent and easier experience

In the beginning when designing the BigBlueButton HTML5 client, we started with the mobile experience having a completely different experience from the web client.  After all, they are different forms of interaction: touch vs. mouse and keyboard.

As we developed designs for the mobile interface -- starting from a very small set of design goals -- we knew it didn’t need to work exactly the same on all platforms to succeed; rather, it needed to share a common design language that was consistent across all platforms.

<br><br>

# Design Goals

## Mobile first approach

Designing for mobile first allows us to take a step back from the current user experience and think about the minimal set of features required for a participant to engage in a session. 

The current user experience has a series of windows and layouts to accommodate different users.  However, mobile applications don’t have windows.  Instead, they have a core set of elements that intelligently overlay as the user needs to access them.

We have a similar set of elements in BigBlueButton 

* The presentation area
* Group or private chat
* Participants list
* Video (webcam and desktop sharing)
* Preferences

## Unified experience

Providing a unified experience will allow our users to quickly become familiar with the product and reduce the overall learning curve. If you are using the web, tablet or mobile client, our goal is to have consistent styles and placement of elements. This will also make the experience of contributing or building on top of BigBluebutton a lot easier for developers. 

## Accessibility

Accessibility has played a large role with transitioning to an HTML5 enriched client. It will allow us to provide our users with a variety of accessibility best practises, such as Aria landmarks, Aria labels, Aria polite. These constructs cover a variety of accessibility use cases and will lay the foundation for BigBlueButton to become a more accessible product. 

## UI structure developer can build on

BigBlueButton is not only a solution, but it’s a platform that individuals can build on top of. 

There are many current use cases of the product which has helped with the creation of the new client. Our goal is to provide our community with a modular design so that new features or components can be created with ease. 

We would also like to provide a detailed style guide, that will help guide developers in choosing and placing elements. If it’s shared notes, or additional volume controls, we want to make sure the look and feel are consistent with the existing user interface. 

<br><br>

# Client Designs
The following are the latest user interface designs for the web, tablet and mobile client. To view all designs, please visit our [InVision project.](https://invis.io/FW6L8OYR4)

## Mobile 

**Participants View**

<img src="/images/mobile_presentation.png" width="225" /> 
<img src="/images/mobile_presentation_portrait.png" width="225" /> 
<img src="/images/mobile_chat.png" width="225" />
<img src="/images/mobile_settings.png" width="225" />


<img src="/images/mobile_presentation_landscape.png" width="475" />
<img src="/images/mobile_actions.png" width="475" />

<br>

## Tablet

**Participants View**

<img src="/images/ipad_landscape_presentation.png" width="475" />
<img src="/images/ipad_landscape_presentation_nav.png" width="475" />
<img src="/images/ipad_landscape.png" width="475" />
<img src="/images/ipad_landscape_sidebar.png" width="475" />

<br>

## Web

**Presenter Views**

<img src="/images/bbb-html5_presenter_no_presentation.png" />
<center> Presenter's first time experience </center>

<br>

<img src="/images/bbb-html5_presenter_presentation.png" />
<center> Populated presentation</center>

<br>

<img src="/images/bbb-html5_presenter_sidebar_chat.png" />
<center> Multiple opened components</center>

<br>

<img src="/images/bbb-html5_presenter_whiteboard_tools.png" />
<center> Whiteboard tools</center>

<br>

<img src="/images/bbb-html5_presenter_deskshare.png" />
<center> Desktop sharing</center>

<br>

<img src="/images/bbb-html5_presenter_settings_audio.png"  style="border:1px solid #ccc;" />
<center> User settings</center>

<br>

**Participants Views**


<img src="/images/bbb-html5_participants_no_presentation.png" />
<center> Participants first time experience</center>

<br>

<img src="/images/bbb-html5_participants_presentation.png" />
<center> Populated presentation</center>

<br>

<img src="/images/bbb-html5_participants_presentation_actions.png" />
<center> User action buttons</center>

<br>

<img src="/images/bbb-html5_participants_presentation_sidebar_alert.png" />
<center> Alert message</center>

<br>

<img src="/images/bbb-html5_participants_presentaton_notifications.png" />
<center> Session notifications</center>


<br>


## Style Guide

<img src="/images/bbb_style_guide.png" style="border:1px solid #ccc;" />

<br>

## Modular Design Example

The HTML5 client consists of three main areas

1. Presentation
- PDF presentation
- Webcams
- Deskshare
- Polling

2. Participants
- Presenter
- Audio user
- List only users

3. Conversations
- Group
- Private

<br>

<img src="/images/bbb-html5-presenter-cropped.png" />

<br>

By grouping features and content into their own blocks, allows us to associate content and their actions together. For example, providing presentation actions within the presentation area vs. in the top right left corner. 

Also, this provides our development community with a framework for building on top of the existing client. If they are adding a new action for the presentation, they will know exactly where to place this button. Or if they are looking to build a new module, they will know that modules are their own block. 

Below we'll outline two examples of building on top of the HTML5 client.

<br>


### Shared Notes

The ability of collaborating together on notes for the session.


**Presentation**  - Uploaded a presentation

<img src="/images/bbb-html5_wireframe_presentation.png" />

<br>


**Exploded View** - Webcam, users list and public chat are turned on

<br>

<img src="/images/bbb-html5_wireframe_presenter_sidebar_chat.png" />

<br>

**Presentation Actions** - The presenter would like provide their participants with the ability of contributing to a set of shared notes. To do so, the presenter will need to select “Public Notes” from the action button. 

In the new client, we’ve decided to group all our presentation actions into a single button. This allows us to scale the presentation to multiple actions without cluttering the interface. 

If you’re looking to add a new actions to presentation, this is where you’ll place the button to activate it.

<br>

<img src="/images/bbb-html5_wireframe_presenter_actions.png" />

<br>

Since the action is to activate a new module, it will appear to the right of the presentation block. 

<br>

<img src="/images/bbb-html5_wireframe_presenter_new_module.png" />

<br>

Introducing new modules to the right of the presentation will provide developers with a dedicated area and real estate to build a variety of different features. Also, by dedicating a specific areas, will limit the interference to BigBlueButton’s core interface. 

<br>

### Multiple Presentation Windows

Multiple presenters sharing content. 

<img src="/images/bbb_multiple_presentations.png" />

In the screenshot above, you’ll see an implementation of the BigBlueButton client with multiple presentation screens. 

<br>


**Multiple presentation view**

A general rule we’d like to establish for adding to the BigBlueButton core interface, is to make sure any new item is contained within their appropriate block. 

Below you’ll see a series of layouts that following this rule. We are introducing multiple presentation windows to the interface and they are grouped within the presentation block. 

<br>

<img src="/images/bbb-html5_wireframe_multiple_presentations.png" />

<br>

<img src="/images/bbb-html5_wireframe_multiple_presentations_sidebar.png" />

<br>

<img src="/images/bbb-html5_wireframe_multiple_presentations_full.png" />


Thanks for reading through the current progress of the HTML5 client designs. If you have any questions, thoughts or feedback, please email [the BigBlueButton community](bigbluebutton-dev@googlegroups.com). 

