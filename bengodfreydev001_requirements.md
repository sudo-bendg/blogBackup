---
layout: '../../layouts/BlogLayout.astro'
title: "bengodfrey.dev - requirements"
author: "Ben Godfrey"
postTitle: "testpostname"
---

# bengodfrey.dev - requirements

As a junior software engineer in the age of AI, when I want to start a new project the usual approach is:

1. Use an npm package with a bulky boilerplate
1. Ask my dear friend Claud to give me all of the functionality that I want
1. I end up with a codebase that I do not fully understand

This final point is tricky, because I cannot say for certain if it is the code that I do not understand, or the frameworks I am using. I admit, this is a slightly exaggerated version of things, but without actively choosing to slow down one's own productivity, the tools available today make it very easy for junior engineers to not learn.

What can we do then? I would suggest the following. Firstly, with regards to our product:

- Get a clear picture of what we *want*

Without deciding this, we will be spinning our wheels but not going anywhere. Next, with regards to our technology:

- Consider options before jumping into any decisions around languages or frameworks
- Slow down our own productivity (within reason)
- Take time to understand what we are doing

With that in mind, let's start.

## What do we want?

The aim for this project in particular is to produce a personal portfolio sort of website. Think developer's blog, CV, place to post projects. All the other stuff that junior devs pretend is important. For me, the content of this is fairly simple:

- Static web pages
    - About me
    - Projects
    - CV
    - Contact
- A blog
    - The bulk of this can be static pages, **but**,
    - I want to provide the ability to comment on posts

Now everything until this final point about comments is extremely easy to do. I could write some html and be done. This second requirement adds some more thought. Now instead of talking about html files, I need to use horrid words like "architecture" and "layers".

### Non-Functional Requirements

Above, I have talked about what I want my site to be able to do. Before I go about planning my tech stack, I want to think a bit about how I want it to work. I think this is best stated as a few rough 'morals'.

1. Simple
    - As mentioned earlier on, I want to be able to understand my stack, keeping things simple will help here.
    - I can always add things later on, but it may be trickier to take things away. Let's try to keep our stack tailored, not baggy.
1. Green
    - This one is a little harder to put a finger on. I am of the opinion that the modern internet lets people build up a carbon footprint without seeing it directly. There are two aspects to tackling this perceived issue
        - Observability - *Showing* users the impact that their actions take.
        - Reduction - From a provider point of view, we should do what we can to lower the impact we cause.