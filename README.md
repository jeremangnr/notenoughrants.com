# notenoughrants.com
Source code and articles for notenoughrants.com, a blog about technology, iOS development and anything else I feel like writing about.

This repository contains the source code for the whole site and the articles (those will be moved to a separate repo eventually).

Getting started
---------------

notenoughrants uses [Jekyll][Jekyll], and is deployed to S3 using the [s3_website][s3_website] gem. The setup is for running locally is quite simple:

- Clone the repo: `git clone https://github.com/jeremangnr/notenoughrants.com.git`
- Run `jekyll serve`

Deploying to S3
---------------

To deploy the site to S3 you need to add a `s3_website.yml` in the notenoughrants.com folder. This file is used by the s3_website gem to store client/secret id's and other info about your S3 bucket. Here's what it basically looks like:

```yml
s3_id: SOMEID123
s3_secret: S0M3S3C43T/abc%/123 
s3_bucket: yoursite.com
cloudfront_distribution_id: A1B2C3D4E5 # optional
s3_endpoint: sa-east-1 # optional, set this if you're not using the default region
```

After creating the file you need to run `s3_website cfg apply` to setup your bucket, **this only has to be executed on the first run**.

To deply just run `s3_website push` and watch the site flying out into the cloud.

License
-------

All code is licensed under the MIT license, as specified by the LICENSE file. All assets and content are release under the Creative Commons BY-NC License.

Contact
-------

You can find me on Twitter ([@jereahrequesi][twitter]) or email me at jeremias.np@gmail.com.

[twitter]: https://twitter.com/jereahrequesi

[s3_website]: https://github.com/laurilehmijoki/s3_website
[Jekyll]: http://jekyllrb.com

