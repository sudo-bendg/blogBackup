---
layout: '../../layouts/BlogLayout.astro'
title: "bengodfrey.dev - the stack"
author: "Ben Godfrey"
---

# bengodfrey.dev - the stack

## Design

Another step closer to starting work. Now I can start making design choices.

### Serving Pages

My primary concern while thinking about how I should go about serving pages is my second non-functional requirement, keeping things green. If I can avoid any compute while preparing pages that would be good, let's try to stick to serving static html files where possible.

Now to burst my own bubble - static html files are not going to work across the board. This is because of my blog/comment requirement. I will require some amount of dynamic logic to put together my html pages and to include the comments which have been submitted for a given blog post. How can we integrate this with our "keep things static where possible" idea?

Caching!

What we can do instead is keep a cached version of each blog post page, and create and cache a new version each time a comment is added to the post. Now, this approach is not what modern social media sites use. If I have users posting comments multiple times a minute, this strategy may start to get a bit much, but I will not.

### Creating Pages

We have decided that we need a way to create html pages, so let's find a nice way to do this. Straight away I want to rule out things like React. This will certainly be more functionality than I am requiring. What I want is a tool or a framework which will let me **generate** html files.

There is a handy wee site [here](https://jamstack.org/generators/) which breaks down some of my options. To decide between these, I will turn back to the morals which I am trying to let guide me.

- Simple
    - I know Javascript/Typescript. Familiarity with the language will make learning a new framework easier. Also, these languages, and the frameworks which come with them are popular, meaning plenty of help is out there. Simple.
    - My decision based primarily on this factor would be Astro.
- Green
    - I am, at the end of the day, just making a personal portfolio/blog. I am more than happy to throw away functionality in favour of speed and a small footprint. For that reason, I would prefer to lean towards something compiled.
    - My decision based primarily on this factor would be Hugo.

The verdict? Based on looking around at the documentation for both frameworks, it is clear that Hugo would better fit my green non-functional requirement during the build of my pages. **However**, the build will be a fairly small part of the process, and I will expect many more reads than I will writes. This, combined with my requirement for commenting etc., points me towards Astro, where these sorts of features are easier to integrate. We have our winner, Astro.