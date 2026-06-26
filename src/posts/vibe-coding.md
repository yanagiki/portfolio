---
title: "Vibe coding: What it is, and why you should give it a miss"
publication: "Digital Trends"
pubDate: 2026-06-30
url: "https://www.digitaltrends.com/computing/what-is-vibe-coding-and-is-it-useful/"
---

# Vibe coding: What it is, and why you should give it a miss
We all know programmers are using AI tools to supplement their work, but there’s a new trend in town taking things to the next level. The term “vibe coding” was coined by OpenAI co-founder Andrej Karpathy just last month, but what started as a [random X post](https://x.com/karpathy/status/1886192184808149383) has quickly spiraled into a whole new community.

<figure>
  <img src="../images/karpathy-tweet.webp" alt="screenshot of a tweet from @karpathy">
  <figcaption>The original "vibe coding" post, via <a href="https://x.com/karpathy/status/1886192184808149383">@karpathy</a></figcaption>
</figure>

What Karpathy describes in his post is creating software without writing any code — all he does is send prompts describing what he wants to his AI tool and accept all of the output it generates. He even uses a dictation tool to avoid using his keyboard. Sounds crazy, right? That’s because it is.

## What exactly is vibe coding?
Most AI coding tools right now do three things:
* Generate auto-complete suggestions when the user is typing a line of code
* Explain, summarize, debug, or advise on code snippets you provide
* Generate chunks of code based on your natural language prompts
They’re designed to help people who know how to code — with some also focusing on study and education. Even Cursor, one of the main tools people are using to vibe code right now, is really designed for developers. It’s meant to speed up simple processes for people who would have been coding whether the tool existed or not.

Take this random feature explanation from the Cursor website, for example: “Cursor lets you write code using instructions. Update entire classes or functions with a simple prompt.” Sure, the purpose of the feature is to save you from writing code manually — but you still need to know what things like classes and functions are to make good use of it.

Vibe coding (or what vibe coding is quickly becoming) is a trend where people take these tools and try to make something with as little as zero software development knowledge — simply describing in natural language the results they want to see as an end user.

## Why is vibe coding problematic for your users?
When a completely non-technical person opens up Cursor and starts vibe coding, the results will be pretty different from when someone like Andrej Karpathy vibe codes. Where Karpathy might ask Cursor to “Generate some code that hashes and salts passwords for user authentication,” a non-technical vibe coder might say “Hey Cursor, make a secure database to store my passwords.”

Sure, they used the word “secure” — but that’s exactly the kind of detail an LLM might randomly ignore. Alternatively, its idea of “secure” might not be up to commercial software standards, or it might add security measures in some places and not others. There’s another problem with this phrasing, too — the “store my passwords” part. It’s pretty normal to think of passwords as being “stored” somewhere but if you know what password salting and hashing are, you know that users’ passwords technically aren’t stored anywhere.

Instead, the salt and the hash value of the concatenated salt and password are stored — and despite all of the crazy terms in that sentence, it’s not an overly complex concept. However, it is something you’d never know unless you purposefully went out and learned about it. And if you don’t know it, you can’t ask for it.

So, instead, you’ve requested a secure database — but which version of the LLM genie will you get? The one that takes your prompt literally and stores the passwords as is in a random little database? Or the one that considers what you actually want to achieve and comes up with a proper authentication process for you?

I think the most accurate answer is that sometimes you’ll get the mean-spirited genie, sometimes you’ll get the kind one, and a lot of the time, you’ll get something in between — with no real rhyme or reason to it. It could do 100% of the job, it could do 90%, it could do 5%. With a prompt that vague, anything could happen, and the problem is — a non-technical vibe coder has no way of understanding the result or deciding how good it is.

You can’t even write proper tests to find out what’s going on if you don’t know what security measures you need, what you ended up with, what they should achieve, or what success and failure might look like.

After all, having bad, broken, or zero security measures implemented in your software won’t make it break. It could still look like it’s doing everything correctly on the user end — but behind closed doors, your users’ sensitive information (personal data, payment information, usage history) will be completely unprotected and ready for bad actors to steal. And that’s bad for you as well as your customers — security breaches cause nothing but stress, scandal, and financial loss for product owners.

When Karpathy described his vibe coding experiments he said the code he and Cursor produce “mostly works,” and I’m not here to claim that “mostly works” is unacceptable. There are always quick fixes, hacky solutions, bugs, and all sorts of problems hidden in every code base for every product. With the size and complexity of software these days, it’s simply unavoidable.

But if you want to release your project to the public and charge people money to use it — you have a responsibility to make it as safe as you can. Leaving sensitive information unprotected isn’t okay — and assuming it’s protected without properly confirming isn’t okay either.

If you need a real-life cautionary tale — [@leojr94](https://x.com/leojr94_) on X has everything you need. Here is his story condensed into three X posts:

<figure>
  <img src="../images/leo-tweet-1.webp" alt="screenshot of a tweet from @leojr94">
  <figcaption>Post 1, via <a href="https://x.com/leojr94_">@leojr94</a></figcaption>
</figure>
<p>&nbsp;</p>
<figure>
  <img src="../images/leo-tweet-2.webp" alt="screenshot of a tweet from @leojr94">
  <figcaption>Post 2, via <a href="https://x.com/leojr94_">@leojr94</a></figcaption>
</figure>
<p>&nbsp;</p>
<figure>
  <img src="../images/leo-tweet-3.webp" alt="screenshot of a tweet from @leojr94">
  <figcaption>Post 3, via <a href="https://x.com/leojr94_">@leojr94</a></figcaption>
</figure>

## Why is vibe coding problematic for you?
Software is expensive. Even if you cut all of the development costs through vibe coding, you still have to pay to store your data, send it around between you and your users, and interact with other services through APIs.

The services you use for this, such as AWS, are usually pay-as-you-go, meaning you only pay for exactly what you need. That’s great, right? Sure. But when you’re not in control of the software you’re developing, you’re not in control of the data usage either. Your code, generated in random chunks and spliced together, is likely to be extremely inefficient. Just a few badly designed lines could produce 3x, 5x, or even 10x more data than you actually need — and sending that unnecessary data back and forth between you and your users will cost you lots of extra money. The most explosive way this can go wrong is actually when things go right.

Imagine you have a few users, you have some bills coming in, growth is slow but steady, and you can deal with it. But one day you wake up and your social media content has gone viral, driving thousands of people to your software product. This would be great, except for the fact that your AWS bill is now huge and you notice that your network traffic costs per user are actually higher than the subscription cost they’re paying you.

## What’s the solution?
At this point, some people would start suggesting more products. Platforms designed for vibe coders and “non-techies” that provide users with extra support for security, servers, and other backend stuff. Some people might also say that with a few tweaks, vibe coding could be just the thing software development needs to become democratized and stop being exclusionary.

I have a different opinion — it’s already democratized and it’s already inclusionary (though I don’t think that’s a word). Anyone anywhere can learn about computer science, coding, programming, or software development as long as they have a computer and an internet connection — and that’s exactly what people do. Huge numbers of programmers are self-taught and they probably always will be. You have everything you need, which leads me to the “harsh truth” of the situation: if you want to make software, then tough luck — you need to learn how to do it.

If you have an idea, you either put in the effort to learn how to build it or you put in the effort to find partners and investors who can help bring it to life. There’s no grifty, zero-effort option where you magically end up with a working product in a negligible amount of time and have no partners you need to share the profits with. That’s not how the world works, and it’s not how it should work, either.

If you want to speak another language, you need to learn it. If you want to play guitar, you need to learn how. And if you want to make software — you need to learn how to make software. If the DIY path sounds good to you, then great news — anyone with the means to sit and vibe code using free or paid software also has the means to sit and study programming using free or paid courseware. Maybe you could even use AI tools to speed things up.

And I’m not kidding when I say anyone can do it — programming is actually so big on  inclusion that there’s even a “type of programming” available for just about everyone. Sure, not every person will become a software architect at a top company — but some people will learn enough to make games in C++, others will learn enough to make apps with Python, and even if you decide that coding isn’t really your thing, you’ll probably still be able to make websites with HTML. Whether you’re a professional study bug or you’ve never studied in your life, and whether you’re a math whizz or you’re terrible with numbers — you will be able to make something.

## How long will vibe coding stick around?
Now, it’s impossible to know what Karpathy intended to achieve by running this little experiment or posting it online. To me, the X post reads like this: “Man, this AI stuff is getting crazy. I can make tons of intentionally bad decisions, ask for intentionally dumb things, and somehow I end up with something that still kind of works.”

Other people seem to have interpreted it more like “Wow, you can make software even if you don’t understand how to code.” Nope. Big nope. You can’t do that. You might think the barrier between you and the app you want to make is that cryptic nonsense programmers sit and type all day — that you can’t make anything because you don’t know how to type code.

But that’s not it. You can start to understand all that stuff after just a handful of hours studying it. It’s just language, just the method of communication between you and the computer, and it pales in importance compared to the actual information you want to communicate. If your goal in life is to have a deep and thoroughly technical conversation with a Spanish experimental physicist in their native language — you won’t achieve it just by learning Spanish.

Designing software, understanding algorithms, managing data, meeting security standards, building for scale, optimizing, and debugging — these are the skills that build software. So it doesn’t matter if Cursor lets you avoid typing code, you still can’t make a proper app if you don’t know anything about apps.

I don’t really know how big vibe coding will get or how long it will last, but I definitely don’t think it’s worth it for a non-technical person to try and vibe code a product. I also don’t think trying a vibe-coded product is worth the risk for consumers — there’s no way to know if your passwords and payment information are safe. If you see a new independently developed product you’re interested in — consider finding out who made it and how it was made before you give them money.