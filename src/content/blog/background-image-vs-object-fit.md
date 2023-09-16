---
title: "Background Image Vs Object Fit"
description: "When developing a website, it's normal to question, should I use Background Image from CSS or Object Fit with Img tag?"
pubDate: "Sep 16 2023"
heroImage: "/object-fit-vs-background-image.webp"
---

# Object fit vs background image: which one should you use for your website?

If you are a web developer, you might have faced the challenge of displaying images on your website in a way that looks good and performs well. You might have used the CSS properties background-image and background-size to set an image as the background of an element and scale it to cover or contain the element’s area. However, there are some drawbacks to this approach, such as:

+ Background images are not part of the document flow, which means they are not accessible to screen readers and other assistive technologies.
+ Background images are not printed by default, which might affect the user experience if they want to print your page.
+ Background images are not responsive by default, which means you have to use media queries or other techniques to adjust them for different screen sizes and resolutions.
Alternatively, you might have used the HTML `<img>` element to display an image in your document. This has some advantages, such as:

+ Images are part of the document flow, which means they are accessible to screen readers and other assistive technologies.
+ Images are printed by default, which might improve the user experience if they want to print your page.
+ Images are responsive by default, which means they automatically adjust their size and aspect ratio to fit their container.

However, there is also a problem with using the `<img>` element: how do you control how the image is resized to fit its container? By default, the image will maintain its original aspect ratio and leave some empty space around it if the container has a different aspect ratio. This might not be what you want, especially if you want to create a full-screen or full-width image effect.

This is where the CSS property object-fit comes in handy. This property allows you to specify how an `<img>` element should be resized to fit its container. It has five possible values:

+ fill: stretches the image to fill the container, ignoring its aspect ratio.
+ contain: scales the image to fit the container, preserving its aspect ratio. The image will be letterboxed if its aspect ratio does not match the container’s.
+ cover: scales the image to cover the container, preserving its aspect ratio. The image will be cropped if its aspect ratio does not match the container’s.
+ none: leaves the image unchanged, regardless of the container’s size.
+ scale-down: compares the difference between none and contain, and chooses the smaller one.

Using object-fit, you can achieve similar effects as using background-image and background-size, but with more flexibility and accessibility. For example, you can use object-fit: cover to create a full-screen or full-width image effect with an `<img>` element, without losing any semantic or accessibility benefits.

However, there is also a downside to using object-fit: it is not supported by all browsers. According to Can I use, as of September 2023, object-fit is supported by 94.8% of global browsers, but not by Internet Explorer or Opera Mini. This means that if you use object-fit, you should provide a fallback solution for browsers that do not support it. One possible fallback is to use a `<picture>` element with multiple `<source>` elements that provide different versions of the image for different screen sizes and resolutions. Another possible fallback is to use a polyfill script that mimics the behavior of object-fit using JavaScript.

So, which one should you use for your website: object fit or background image? The answer depends on your design goals, your target audience, and your performance budget. Here are some factors to consider:

Object fit provides more semantic and accessible images than background image, which might improve your SEO and user experience.
Object fit allows you to use inline images instead of background images, which might improve your performance and Web Vitals metrics. According to web.dev, inline images can take advantage of features like lazy loading, responsive images, and compression formats that can reduce their impact on loading time and bandwidth usage. Background images, on the other hand, are not affected by these features and might increase your page weight and loading time.
Object fit requires browser support or a fallback solution, which might increase your development time and complexity. Background image is widely supported by all browsers and does not require any fallback solution.
In conclusion, there is no definitive answer to which one is better: object fit or background image. Both have their pros and cons, and you should weigh them according to your specific needs and preferences. However, if you want to create modern and performant web experiences that work on any browser, you might want to give object fit a try.