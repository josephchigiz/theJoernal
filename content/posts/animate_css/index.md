+++
title = 'Add basic animations to your site using "Animate.css" and  "wow.js"'
date = 2024-04-14T18:21:41+05:30
draft = false
tags = ["animation", "css", "html", "cdn", "animate.css", "wow.js"]
+++

I have been working on my [personal portfolio](https://ochego.netlify.app) website _(although not complete)_ for the past few weeks, taking it really slow, revising designs and ensuring I get my persona represented accurately. One of the visual elements I've had to have from the inception of the idea was **animations**.

You might have just shrugged, thinking, "Another complex guide on implementing web animations...". Far from it. This is probably the simplest way you can use animations in your site using **_CSS classes_**.

That's it? - Most definitely! And I'll cover, albeit very briefly, how you can implement this right in your `.html` file and see your beautiful lifeless _(for dramatic effect :D)_ site brought to life. For this, you need two libraries, **[Animate.css](https://animate.style/)** and **[wow.js](https://wowjs.uk/docs.html)**.

## [Animate.css](https://animate.style/)

"**Animate.css** is a library of ready-to-use, cross-browser animations for use in your web projects. Great for emphasis, home pages, sliders, and attention-guiding hints.", as they say it on their site. Plain and simple.

### Installation

There are three ways of installing **animate.css**:

- Using npm
- Using yarn
- Using cdn, directly in our file _(our way)_

Based on the promise of simplicity, we'll use the `CDN` method, adding the link directly into out head tag as shown:

```html
<head>
  <link
    rel="stylesheet"
    href="https://cdnjs.cloudflare.com/ajax/libs/animate.css/4.1.1/animate.min.css"
  />
</head>
```

### Usage

Once you've installed **animate.css**, add the `animate__anmated` class to your target element, followed by the class-name of the animation you wish to use; always starting with the `anmate__` prefix.

Here's an example:

```html
<img src="image.png" class="animate__animated animate__fadeInLeft" />
```

_This adds a fade-in from the left animation to our image element._

Note that these animations are displayed only when the page loads; forcing you to have the element in the viewport during loading to see it.

**However!!** There is a way to delay the loading of each animation and only load it and display it when the target element is scrolled into the viewport. We use a JavaScript library called **[wow js](https://wowjs.uk/docs.html)** to achieve this. And as promised we'll still do it simply:

## [Wow JS](https://wowjs.uk/docs.html)

Wow.js reveals animations when you scroll and the animated elements come into the viewport. Using it ensures that your visitors don't miss your wiggles, fades, bounces and spins.

Wow.js is very animate.css friendly. Exactly why we're working with both in this turorial.

### Installation

Installing wow.js is as simple as adding a `script` at the the end of the `<body>` in your `.html` file:

```html
<body>
  <script
    src="https://cdnjs.cloudflare.com/ajax/libs/wow/1.1.2/wow.min.js"
    integrity="sha512-Eak/29OTpb36LLo2r47IpVzPBLXnAMPAVypbSZiZ4Qkf8p/7S/XRG5xp7OKWPPYfJT6metI+IORkR5G8F900+g=="
    crossorigin="anonymous"
    referrerpolicy="no-referrer"
  ></script>
  <script>
    new WOW().init();
  </script>
</body>

<!--make sure you have the latest version at the time of implementation-->
```

Although wow.js can also be installed using **npm** and **yarn**, I opted for the simplest way - using a **CDN** link.

### Usage

Simply add the `wow` CSS class to the element and it will be hidden until the user scrolls it into the viewport.

```html
<img src="image.img" class="wow" />

<!--Then add your animation class-->

<img src="image.img" class="wow animate__animated animate__bounce" />
```

And you're done!

There are a few more cool customizations you can do with the wow script, which you can check out on [wow.js](https://wowjs.uk/docs.html)

###### Have Fun Learning 😁

#### Links

https://wowjs.uk/docs.html - wow.js

https://animate.style/ - Animate.css
