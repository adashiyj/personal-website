---
title: "Building Your Own Website 101 (No Stress, Easy Code!)"
date: 2025-07-13
author: "Ada Shi"
summary: "In this blog, I share my journey as a web-building newbie creating my first personal website, plus some easy-to-follow resources to get you started too." 
showToc: false
disableAnchoredHeadings: false

---

## Preface

After wrapping up my first year of the research master’s, I flew back to Yunnan, China. This week, I’m staying with my 88-year-old grandma in a tiny village near Lijiang. My days drift by sunbathing with her and soaking up an endless stream of neighborhood gossips and family sagas. Between the sunshine and the stories, though, I find myself growing a bit restless in this sleepy, charmingly uneventful town.

A few days ago, while searching for potential PhD programs, I stumbled upon some fascinating personal academic websites. I’d never imagined I’d build one myself, but with all this unexpected free time, a thought crossed my mind: Why not give it a shot?

## How did I get started?

Like 95% of people would (and no, there’s no scientific reference for that statistic), I turned to Google and typed, “How to build a personal academic website?” Naturally, hundreds of pages popped up. Perfect! Just like doing research: there’s plenty of data out there, and the next step is to take a bottom-up approach. What’s next? Sift through it all, see what’s out there, and summarize the options. Sounds good in theory, right? But am I really going to read every single page? Nee! Luckily, Google’s AI Overview came to the rescue, and here’s what it suggested:
+ Website builders: Wix, Squarespace, and WordPress offer user-friendly interfaces and templates. 
+ Free options: Google Sites, GitHub Pages (with Jekyll or other static site generators). 
+ Paid hosting: If you need more advanced features or customization, explore options from companies like GoDaddy or HostGator.

As a broke student, the free options caught my eyes right away. I didn’t know what static site generators were, but since I'm already a Git user, I decided to give GitHub Pages a shot (I know this blog sounds like Diary of a Wimpy Kid, please stay tuned!). So I searched “building personal website on GitHub Pages” and found the [academic-website](https://github.com/topics/academic-website) topic on GitHub.

## Hosting A Static Website On GitHub Pages

There are a few static site generators where you can use to generate your static websites on GitHub Pages:
+ Jekyll: a simple, blog-aware, static site generator written in Ruby [see more](https://jekyllrb.com/).
+ Hugo: a fast, flexible, static site generator written in Go [see more](https://gohugo.io/).
+ [Others](https://github.com/collections/static-site-generators)

A ***static site generator*** is a tool that helps you build a website by turning plain text files (e.g., Markdown) into a complete website with pages, layouts, and links without needing a data base or fancy server setup. Specifically, it’s called "static" because it creates fixed pages (built with HTML, CSS, and JavaScript files) that don’t change each time someone visits (so your site is fast and secure). 

There are many open-source templates. Mine was forked from Pascal Michaillat's [Minimalist Hugo template for academic websites](https://github.com/pmichaillat/hugo-website). The documentation in the repository is super clear and easy-to-follow. 

In addition, to host your personal website on GitHub Pages safely and get a clean URL like `https://yourusername.github.io/` instead of `yourusername.github.io/hugo-website/`:
+ First, fork the website template repository.
+ Then, open your terminal (MacOS) and run:
<pre> ```bash cd PATH/TO/YOUR/FORKED/REPO hugo cd public git init git remote add origin https://github.com/yourusername/yourusername.github.io.git git add . git commit -m "Deploy to root" git branch -M main git push origin main --force ``` </pre>
+ Create a new repository named `yourusername.github.io` and upload all files from the `public` folder (from the forked repository) to this new repository (Important: upload the contents only, not the entire public folder itself!).

Lastly, remember: your website will only deploy if the hosting repository is public. Sometimes deployment takes a few minutes, so be patient, and if something goes wrong, check the `Actions` tab to debug any errors in the workflows.

**Tada! Easy right?** Anyway, I just realized it’s almost 11 PM. I’d better wrap this up before my grandma gets mad. Ciao!

