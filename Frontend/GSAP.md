### What is GSAP ?

  

![alt](https://cdn.prod.website-files.com/67053868fc01e494462e71c9/671105b65973fbf64381e14a_6553277ada073bf147891afb_thumbnail-gsap-animation%2520.jpeg)

  

GSAP (for Green Sock Animation Platform) is a JavaScript library that allows to animate elements in a webpage. It makes it possible to create complex and performant animations, while yet offering a very friendly and versatile API. It also comes with a variety of plugins, some of which are paid, offering powerful and customizable tools to help animate almost anything, from text to SVG, and even include some effects based on physics.

  
  

### Concepts that this library introduces:

1. **Tween:** A Tween is what does all the animation work - think of it like a high-performance property setter. You feed in targets (the objects you want to animate), a duration, and any properties you want to animate and when its play head moves to a new position, it figures out what the property values should be at that point applies them accordingly.

**Methods for creating a Tween**

```
gsap.to() // <---- it allows you to define the destination values

gsap.from() // <---- it allows you to define the starting values

gsap.fromTo() // <---- it allows you to define both the starting and destination values
```

2. **Timeline**: The timeline answers the following question: how can I trigger my animations in sequence, or relative to one another, without having to calculate all the delays myself? The solution is to use a timeline to group the tweens together, optionally specifying where the tweens should be placed in the timeline with the position parameter.

  
**WITHOUT Timelines (only using delays):**

```
gsap.to("#id", { x: 100, duration: 1 });

gsap.to("#id", { y: 50, duration: 2, delay: 1 }); //wait 1 second

gsap.to("#id", { opacity: 0, duration: 1, delay: 3 }); //wait 3 seconds
```


 **WITH Timelines (clean and easy to control):**

```
const tl=gsap.timeline(); //<-- This line is creating a timeline object which is like a container for our animations

tl.to("#id", { x: 100, duration: 1 }); // <-- This line is creating a tweens and adding it to the timeline (at the beginning)

tl.to("#id", { y: 50, duration: 2 }); // <-- This line is creating a tween and adding it to the timeline (at the end of the previous tween)

tl.to("#id", { opacity: 0, duration: 1 }); // <-- This line is creating a tween and adding it to the timeline (at the end of the previous tween)
```

  
### How to setup in your project ?
 
**1. CDN**
  
<script  src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.2/gsap.min.js"></script> // <-- This line is adding the GSAP library to your project (in the <head> tag)

  
 **2. NPM**

  `npm install gsap // <-- This line is installing the GSAP library to your project (in the terminal)`

  import gsap from "gsap"; // <-- This line is importing the GSAP library to your project (in the <script>  tag) // <-- This line is importing the GSAP library to your project (in the <script> tag)

  

**Refer this link for more information:** [](https://gsap.com/resources/)

  
  

**Visit this link for checking projects made using GSAP:** [](https://gsap.com/showcase/)