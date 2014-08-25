---
title: "Embedded Gists"
description: "Perhaps it is better to embed gists than have inline markup in blog posts."
date: "2014-07-05"
categories: 
    - "tech"
    - "github"
    - "gists"
    - "hugo"
---

## Syntax Highlighting - or Embedded Gists

I was quite excited by the inline syntax highlighting that Hugo provides via the python plugin [Pygments](http://pygments.org/). But also wanted to try embedding gists 

<!--more-->
So here is an example...

{{% highlight html %}}
<div></div>
{{% /highlight %}}



But then thought perhaps it is better to embed gists than have inline markup in blog posts then folk can fork the code and comment there. 

So on embedding a gist as follows (but without syntax highlighting) failed...

{{% highlight html %}}
<script src="https://gist.github.com/danmux/042fa69bed3791afe658.js">
</script>
{{% /highlight %}}

Putting it in another block partially worked 

{{% highlight html %}}
<p>
    <script src="https://gist.github.com/danmux/042fa69bed3791afe658.js">
    </script>
</p>
{{% /highlight %}}

I was left with an unclosed script tag.

A git of googling turned up this thread...

https://groups.google.com/forum/#!topic/hugo-discuss/3GW56aMYQF8

and this pull request ...

https://github.com/spf13/hugo/pull/305

which missed the latest release by a few days...

https://github.com/spf13/hugo/releases/tag/v0.11

So I went ahead an built the master head - from my fork (ya know just in case I can help)

and added the script tag in....

<script src="https://gist.github.com/danmux/042fa69bed3791afe658.js"></script>


### And it worked ! 

Nice work [jmitchell](https://github.com/jmitchell) and [Steve Francia](https://github.com/spf13).

So gists it is for me
