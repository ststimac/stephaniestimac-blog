---
title: Using the ':not()' pseudo-class to remove styles from ':last-child'
description: A brief CSS tip when displaying items in a row
date: 2024-12-01
tags:
  - css
  - notes
layout: layouts/post.njk
images:
    thumb: /img/2024/not-pseudo-class.webp
permalink: posts/2024/12/not-pseudo-class/index.html
---

I was re-designing the footer for my blog when I added a list of social icon links. I needed to add some padding between them, as one does, and was preparing to apply padding to the left of each icon so the final icon on the right remained aligned right. 

On smaller screens, when my footer wraps, this means I would need to write some more CSS to switch the padding to the right so the icon on the far left is then flush with the left. 

Sure there are many ways one could approach handling how to layout a line of icons but I decided to Google how to apply styles to everything except the `:last-child`. It seems I wasn't aware of the `:not()` pseudo-class which has been widely supported in major browsers for sometime. 

With the following line of CSS, I can apply padding to everything except the `:last-child`. 

```
.social-links a:not(:last-child) {
  padding-right: .6rem;
}
```

This also means I don't have to write any code to change the padding when my layout wraps to smaller screens so that's less code for me! 

CSS is pretty neat. 