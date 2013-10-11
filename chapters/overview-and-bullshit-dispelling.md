# Overview and bullshit-dispelling.

You have models and collections (the data layer), views (or controllers, name it as you will), and URLs. As is with nearly every other popular and decent framework/lib of this kind.

The rule of thumb is get the hell away from the DOM. You won't read from it ever (e.g.: getting an element's class name, or the length of a list counts as that), because your data layer knows what has what value and in what state anything is at at any given time. You’ll write to the DOM only by rendering views. If you don't agree, then just use regular JS or jQuery.

Small modules built outside of Backbone (read: are not a model/view/router) **are ok**. So long as they perform **one** function and are clear in what they in turn require, it’s all good.

Common architecture mistakes involve getting one or more of the previous statements wrong, “bending the rules a little”, or however else you excuse it.

This is what every JavaScript framework powered app does: they get views to track changes in data, and re-render the associated view(s) in more or less granular fashion depending on the tool (Angular for instance would be very granular by default).

It’s entirely possible to make stupid mistakes with any framework. To say one is less prone to idiocy than the other is a cheap attempt at misguiding you. As is stupid to say framework X focuses on URLs (if you heard it, you know it). It either has the feature or it doesn't. Then it's up to you to know why/when to use it.

The goal is creating a fast, beautiful, and maintainable build, and that’s achieved by doing things right through the entire stack (so HTML and CSS too), as well as a great design, not just the application logic. No tool will save you from that. Citing an app as evidence of a framework “being better” conveniently leaves this out, which means it’s an attempt at selling it to you.

Pick a tool and go with it. Stop asking questions such as “Is Angular better than Backbone?”. It’s a huge waste of time even thinking about it until you’re well into a handful of apps and made **a lot** of mistakes which you learned from.

You can create patterns on top of Backbone once you mastered it. A lot of projects out there consist of that, like [Chaplin](https://github.com/chaplinjs/chaplin). Though most of the time you’ll get away without needing any of that.

Sadly, you don't need a license stating that you're capable of using functions and modules correctly before you're legally allowed to use OOP. Throughout this text I'll refer to modules many times because it's the best way to structure your code. Read about [browserify](http://browserify.org/) and learn it.

Think twice before adding a plugin. It doesn’t matter how awesome your favourite website says it is. $100 says they never used it themselves. Hell is other people's code, and the way to it is paved by assumptions that shit just works. **Really** try to solve the problem first. You'll get good at that, and then nothing will stop you.