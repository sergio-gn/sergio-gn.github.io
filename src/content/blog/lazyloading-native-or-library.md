---
title: "Lazy Loading Native or Library?"
description: "We know that Lazy Loading is important on your website. But when it comes to decisions, which one should we choose, Native or Library? I asked myself this question many times during my career, and here is my conclusion..."
pubDate: "Sep 12 2023"
heroImage: "/lazy.webp"
badge: "New Post"
---
 
Lazy loading is a technique that improves the performance and user experience of web pages by delaying the loading of non-critical resources until they are needed. This way, the browser can focus on rendering the visible content faster and save bandwidth and memory.

There are two main ways to implement lazy loading on web pages: using native HTML attributes or using JavaScript libraries.

### Native Lazy Loading

Native lazy loading is a new feature that allows developers to use the loading attribute on img and iframe elements to indicate how they should be loaded. The loading attribute can have one of these values:

```
<img loading="{attribute_here}" src="example.webp">
```

+ lazy: The element is a good candidate for lazy loading and will be loaded only when it is near the viewport.
+ eager: The element is not a good candidate for lazy loading and will be loaded as soon as possible.
+ auto: The browser will decide whether or not to lazy load the element based on its own heuristics.

### Native lazy loading is supported by most modern browsers, such as Chrome, Edge, Firefox, and Safari. You can check the current browser support here.

### The advantages of native lazy loading are:
+ It is easy to use and does not require any additional scripts or libraries.
+ It is standardized and consistent across browsers that support it.
+ It is efficient and optimized by the browser.

### The disadvantages of native lazy loading are:
+ It is not supported by older browsers, such as Internet Explorer, which will load all the elements regardless of the loading attribute.
+ It does not offer much customization or control over the loading behavior, such as the threshold distance, the placeholder image, or the loading animation.

## Library Lazy Loading
Library lazy loading is a technique that uses JavaScript libraries or frameworks to detect when an element is in or near the viewport and load it dynamically. There are many libraries available for lazy loading, such as Lozad.js, lazysizes, lazyload.js, and Layzr.js.

### The advantages of library lazy loading are:
+ It is compatible with older browsers that do not support native lazy loading.
+ It offers more flexibility and customization over the loading behavior, such as the threshold distance, the placeholder image, the loading animation, and the event triggers.
+ It can handle more types of elements, such as backgrounds, videos, scripts, fonts, etc.

### It can handle more types of elements, such as backgrounds, videos, scripts, fonts, etc.
+ It requires an additional script or library to be loaded and executed on the page, which can affect the performance and user experience.
+ It may not be as efficient or optimized as native lazy loading, depending on the implementation and configuration of the library.
+ It may conflict with other scripts or libraries on the page or cause unexpected errors.

## Conclusion
Lazy loading is a useful technique that can improve the performance and user experience of web pages by delaying the loading of non-critical resources until they are needed. However, there are different ways to implement lazy loading, each with its own pros and cons.

Native lazy loading is a new feature that uses the loading attribute on <mark>img</mark> and <mark>iframe</mark> elements to indicate how they should be loaded. It is easy to use, standardized, consistent, and efficient, but it is not supported by older browsers and does not offer much customization or control.

Library lazy loading is a technique that uses JavaScript libraries or frameworks to detect when an element is in or near the viewport and load it dynamically. It is compatible with older browsers and offers more flexibility and customization, but it requires an additional script or library and may not be as efficient or optimized.

If you are working on a modern website with modern standards, native lazy loading is the preferred option, as it provides a better performance and user experience without any extra overhead. According to browser usage statistics, more than 90% of users worldwide use browsers that support native lazy loading. However, if you need to support older browsers or have more specific requirements for your lazy loading behavior, you may consider using a library instead.

### Note: 
Lazy loading can be beneficial for your page performance and user experience, but you should be careful not to use it on the LCP (Largest Content Paint), basically the first screen you see on the website, usually navbar + hero. The reason why you shouldn't use it, is because it cause layout shifts that affect your CLS. You don't want the images on the first impression of your website loading just after your entire page, right? I hope this helps!