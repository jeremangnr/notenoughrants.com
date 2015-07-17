---
layout: post
title: "Metablogging: A blog is born."
date: 2015-07-17
---

It’s been a long time since I’ve wanted to put the stuff I write somewhere. It started out as notes on my phone, then google docs, and one day I thought “Hey, this is blogging but without the blog” so I went [on the line][on the line] to get up to speed on some of the blogging platforms/tools used today (last time I had a website was on _Geocities_) and finally built one. A good way to kick it off is to write about the process, in case someone feels curious.

I ended up choosing **Jekyll** as a platform, which seemed like the most simple and complete feature-wise for my purposes. The theme used is called [Long Haul][theme] from Brian Maier Jr. with some style/code modifications, it includes Google Analytics code and some other pretty cool stuff.  My main source of [inspiration aesthetically was NSHipster][Colophon], I just loved that buttery feel and simplicity the colors and fonts had.

The Jekyll platform runs on an **S3** instance under a custom domain name registered with **DNSimple**. The setup was dead simple, setup a bucket, create a user to generate access/secret key pairs and create a group with admin and full S3 privileges.
For DNSimple there was a little gotcha, since I chose a region different than default for the S3 bucket (I’m from Uruguay, so Sao Pablo was the closest to me) I had to modify the `ALIAS` record in DNSimple to accommodate for the different region (`sa-east-1`, default is `us-east-1`)

Deployment is done using a Ruby gem called **s3_website**, which supports Jekyll out-of-the-box (yes, I’m THAT lazy).

You can find the whole source for the site [on Github][github link], as well as the articles, in case anyone wants to make corrections/suggestions.

The whole setup took about 3-4 hours (considering [third-world internet][welcome to the tercer world] that's great time) and went along quite smoothly. 

So, let the blogging begin!

[on the line]: https://youtu.be/CewJ-ihIqaM?t=25
[theme]: https://github.com/brianmaierjr/long-haul
[Colophon]: http://nshipster.com/colophon/
[github link]: https://github.com/jeremangnr/notenoughrants.com
[welcome to the tercer world]: https://en.wikipedia.org/wiki/List_of_countries_by_Internet_connection_speeds#Akamai_2014_rankings
