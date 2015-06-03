---
layout: post
title: "Awesome Social Icon Hover Effect"
date: 2015-06-03 11:16:08 -0500
comments: true
categories: CSS
keywords: Hover, Icon, CSS
---
In this tutorial, we take a look at creating one beautiful, yet simple, icon hover effects using CSS3 transitions and transforms.

Icons. They exist everywhere, in all our apps and websites these days, and they all perform important functions. They guide users into various interactions, or send them to external links such as various social media platforms. Icon sprites are commonplace and important from a development standpoint, and allow us to engage users a bit with hover classes. These hover classes have the potential to add a neat layer of interactivity and style to our apps/sites. In this tutorial, I'm going to guide you through one icon hover states, each utilizing CSS3 transitions and transforms, engaging the end users a bit more, and possibly leading to higher click-through rates.
<!--more-->

## Making Up Icons?

So in general, our icons will follow this structure (HTML file):


```
<link href="//netdna.bootstrapcdn.com/font-awesome/4.0.3/css/font-awesome.css" rel="stylesheet">

<a class="social" href="https://webbb.be" target="_blank">
     <div class="front">
		<i class="fa fa-facebook"></i>
     </div>
     <div class="back">
		<i class="fa fa-facebook"></i>
     </div>
</a>

<a class="social social-twitter" href="https://webbb.be" target="_blank">
     <div class="front">
		<i class="fa fa-twitter"></i>
     </div>
     <div class="back">
		<i class="fa fa-twitter"></i>
     </div>
</a>

<a class="social social-github" href="https://webbb.be" target="_blank">
     <div class="front">
		<i class="fa fa-github"></i>
     </div>
     <div class="back">
		<i class="fa fa-github"></i>
     </div>
</a>

<a class="social social-pinterest" href="https://webbb.be" target="_blank">
     <div class="front">
		<i class="fa fa-pinterest"></i>
     </div>
     <div class="back">
		<i class="fa fa-pinterest"></i>
     </div>
</a>

<a class="social social-googleplus" href="https://webbb.be" target="_blank">
     <div class="front">
		<i class="fa fa-google-plus"></i>
     </div>
     <div class="back">
		<i class="fa fa-google-plus"></i>
     </div>
</a>

<a class="social social-skype" href="https://webbb.be" target="_blank">
     <div class="front">
		<i class="fa fa-skype"></i>
     </div>
     <div class="back">
		<i class="fa fa-skype"></i>
     </div>
</a>

<a class="social social-linkedin" href="https://webbb.be" target="_blank">
     <div class="front">
		<i class="fa fa-linkedin"></i>
     </div>
     <div class="back">
		<i class="fa fa-linkedin"></i>
     </div>
</a>

<a class="social social-skype" href="https://webbb.be" target="_blank">
     <div class="front">
		<i class="fa fa-skype"></i>
     </div>
     <div class="back">
		<i class="fa fa-skype"></i>
     </div>
</a>

<a class="social social-dribbble" href="https://webbb.be" target="_blank">
     <div class="front">
		<i class="fa fa-dribbble"></i>
     </div>
     <div class="back">
		<i class="fa fa-dribbble"></i>
     </div>
</a>
```

Now, let's dig into some CSS.

```
/**
 * CSS3 social icon hover effect
 * Read more on my blog: http://webbb.be/blog/
 */

body {
	background: #f06;
	background: linear-gradient(45deg, #f06, yellow);
	min-height: 100%;
}
a,a:visited { color: #fff; }
a:hover { color: #fff; }

.social {
	float: left;
	margin: 2em 2em; width: 100px; height: 100px; 	
	display: block; text-align: center; line-height:103px; color: #fff;
	
	position: relative;
	transform:rotateY(0deg);
	transition:transform .25s ease-out;
	transform-style:preserve-3d;
}
.social > div {
	width: 100px; height: 100px; background: #000;
	position: absolute; top: 0; left: 0; right: 0; bottom: 0;
}
.social >.front {
	transform:translateZ(40px);
}
.social >.back {
	background: #3B5998; font-size: 3em;
	transform:rotateY(-100deg) translateZ(40px);
}

/*  Social Media Colors 
	Facebook #3B5998
	Flickr #FE0883
	Foursquare #8FD400
	Google+ #C63D2D
	Instagram #4E433C
	Linkedin #4875B4
	Tumblr #2B4964
	Twitter #33CCFF
	Vimeo #86B32D
	Youtube #FF3333
	Dribbble #ea4c89
*/
.social.social-twitter > .back { background: #55ACEE; }
.social.social-github > .back { background: #f3f3f3; color: #000; }
.social.social-pinterest > .back { background: #e3262e; }
.social.social-googleplus > .back { background: #dd4B39; }
.social.social-skype > .back { background: #12A5F4; }
.social.social-linkedin > .back { background: #4875B4; }
.social.social-dribbble > .back { background: #ea4c89; }

/* Hover */
.social:hover {
	transform: rotateY(100deg);
}
```
<a style="background-color:#44c767;
	-moz-border-radius:28px;
	-webkit-border-radius:28px;
	border-radius:28px;
	border:1px solid #18ab29;
	display:inline-block;
	cursor:pointer;
	color:#ffffff;
	font-family:Arial;
	font-size:17px;
	padding:16px 31px;
	text-decoration:none;
	text-shadow:0px 1px 0px #2f6627;"href="http://dabblet.com/gist/8255020" class="myButton">DOMO</a>