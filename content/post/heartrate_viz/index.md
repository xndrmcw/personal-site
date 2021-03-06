---
title: Using Fitbit heartbeat data to make a cute viz.

image:
  focal_point: ""
  placement: 2
  preview_only: true

# Link this post with a project
projects: ['heartrate_viz']

# Date published
date: "2021-02-01T00:00:01Z"

# Date updated
lastmod: "2021-02-01T00:00:00Z"

# Is this an unpublished draft?
draft: false

# Show this page in the Featured widget?
featured: true

design:
  columns: '2'

links:
- icon: github
  icon_pack: fab
  name: My Code
  url: https://github.com/xndrmcw/heartrate_vis

authors:
- admin

tags: ['Data Visualization']


---
## The graph below is interactive! Mouse over some points to see what my heartrate was, and at what time.

<iframe width="675" height="500" frameborder="0" scrolling="no" src="//plotly.com/~alexandermcw/1.embed"></iframe>


### Thanks for checking out my second post!

It's pretty easy to make visualizations, but it's really hard to make them **good**, let alone ***great***. That being said, I think this one isn't half bad for a near first attempt at fitness data! It pretty clearly illustrates what it's supposed to, and it's not particularly bulky. You might argue that using a scatterplot for heartrate is weird, but I really like being able to mouse over the individual points.

The above graph was, perhaps surprisingly, a bit of a force to get together. I'll walk through the steps I had to take to get to this point below! Even though there were some obstacles, it was a blast, and I recommend it to anyone looking to create a fun little viz project.

So, before you say it, I know!

><p style="color:white;">Fitbit provides a similar visualization in the mobile/browser app.</p>

What they <b><i>don't</b></i> do (for a reason that I'm still not sure of) is allow you to download your heartrate data in a csv format! My initial goal with this project was to get familiar with animated visualizations, and I figured that creating a pulsing heartrate graph would be pretty sweet.

I couldn't find anything on the fitbit forums about downloading heartrate data. My guess is that HR data is pretty hard to come by, so maybe they don't want to just give it out willy-nilly. I dunno. It's kind of a bummer, though! Fortunately, I found a fantastic resource that does exactly what I was hoping for!

[**Check out Neil Ricci's Pulse Watch tool!**](https://iccir919.github.io/pulseWatch/public/index.html)

If you provide this website access to your fitbit account (you'll need your signin info), it'll prompt you with the option to choose either inter or intra day data, as you can see below.

{{< figure src="/media/heartrate_viz_photos/options.PNG" caption="Inter/Intra" >}}

I used intraday, because I was only interested in one day, but I'll include screenshots of both, because it's a great website, and Neil did an amazing job with it.
>## Intra-day HR!
{{< figure src="/media/heartrate_viz_photos/intraday_hr.PNG" >}}

>## Inter-day HR!
{{< figure src="/media/heartrate_viz_photos/interday_hr.PNG" >}}


As for the actual coding - I used Python! Python is popular for data viz, and, in my experience, for good reason. The plotly package ([install guide & documentation found **HERE!**](https://pypi.org/project/plotly)) was fantastic - I had to learn the ins and outs as I went, but I didn't have any significant issues. I love their gradient color scales. The one I selected was arbitrary, I just thought it was nice to look at. If you don't like this one, here's some others they offer, as well as a [hyperlink](https://plotly.com/python/builtin-colorscales/) to the page where you can find a full list!

{{< figure src="/media/heartrate_viz_photos/gradient_colorscales.PNG" >}}

Plotly allows you to export your graphs as jupyter notebook and standalone HTML files, but it also allows for online hosting through the [**Chart Studio Cloud Platform!**](https://chart-studio.plotly.com/) I might make a post that walks line by line through my code to create this visualization later, when I get more comfortable with using Hugo (the GitHub-oriented (is that a thing? GitHub-oriented?? whatever) website builder I'm using).

Anyway, plotly was an easy package to use, and the cloud platform was great! It allowed me to export my visualization as an HTML iframe, which I easily popped into the Hugo config files. I have very little experience with HTML, but learning how to format this very blog post gave me a nice crash-course. I'm learning ways to be more efficient as I go. In the beginning, I was manually editing things in GitHub in browser, and that felt pretty terrible. Switching to the desktop app was great. I'm thinking that I must be missing another piece of the puzzle, though. Having to deploy my website through netlify and waiting for the website to load every time I want to see my changes is pretty rough. Oh well, I'll figure the rest out as I go!

Just as a fun little tradition, I'm going to include either a photo I've taken or that I really like in each of these blog posts.

>This post's photo is...

{{< figure src="/media/heartrate_viz_photos/dinos.PNG" >}}
