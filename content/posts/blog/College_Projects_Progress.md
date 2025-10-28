+++
title = "College, Projects, Progress ☺️"
date = "2025-10-20T19:44:10+01:00"
#dateFormat = "2006-01-02" # This value can be configured for per-post date formatting
author = "Hailey"
tags = ["transition", "college", "projects", "life"]
keywords = ["transition", "college", "projects", "life"]
description = "An update on college, some personal projects that I've undertaken, and progress on my transition."
showFullContent = false
readingTime = true
hideComments = false
+++

# To begin with

Hello! 👋 It's been a while I know, but life has been busy as usual, getting everything sorted out. I'm doing well, in a good place, and can only see things getting better! 🤗

Also, it would appear that people are actually finding this blog randomly on the internet, which is really cool!! Welcome, and thank you for reading ❤️ I hope you appreciate my yammering 😅

# College 📚

So college is going really well, quite different from my first year I must say (probably due to the subject I'm in, software dev now but I was in engineering last year pre-RAF). It's different in good ways that may not be immediately obvious...

For one, due to me being in the city centre this year instead of the outskirts, during our breaks my class tends to disperse quite a bit more, meaning I'm able to get a lot more done in between sessions since I don't really "hang out" with anyone 😂 I know that may seem a bit boring, or sad to some, but it's ideal for me, that's when I can do my best work.

Since I'm doing a T-Level this year which is very industry-focussed, with a required work placement, I'm really making extra-curricular a top priority in these two years to gain experience and credibility. 

My current extra-curricular focus is my participation as a Seminar Leader at [ExCode 2025](https://excode.co.uk), where I, along with two other Seminar Leaders, teach Python fundamentals to a class of ~20 students (the actual cohort is ~1200 students large, all split into multiple classes). I do that every Tuesday night, and it's a blast! 🚀

# Projects 👩‍💻

I've got two software projects on the go that I work on in my free time at home and between classes 👩‍💻

## Project One - A macOS Colour Wheel 🎨

So, yeah, I've gone all-in Apple which is weird for me to say since I've spent the last four years on the opposite end of the spectrum with various Linux distributions on several-generation-old ThinkPads 🐧 But no, I bit the bullet, and got something that'll last me throughout college and potentially further education.

Initially I went for an M4 Mac Mini, but realised that this was utterly stupid considering I'm away from my desk for eight hours every weekday; I returned it and took advantage of Apple's current university student offer (even though I'm not in uni, I still qualify 🧐). So now I have an M4 MacBook Air (base model, 16GB unified memory, 256GB storage), and paid an extra £50 and got AirPods Pro 3 on top, sweet deal if you ask me 🤩

It's not my first time on macOS, I had an M2 MacBook Air briefly while in engineering college.

I'm not sure if I've mentioned this before, but I used to be an Apple **addict** as a kid. Little me would literally spend hours in an Apple store, I loved it, the vibe, the tech, the **aesthetic**. I turned off from them for years, but gave them another go a couple years ago with an iPhone 15 Pro, and I have to say they do make good hardware 🙌

Pricey, sure, and closed-source, but end of the day, if I can do my best work on it...

Now then, I'm building a colour picking utility, why? Doesn't macOS have one?

Yes, there is technically a built-in one, but it isn't really that quick to use, and doesn't have any sort of history at all 😩

I'm rather baffled that I can't seem to find such utility, being that macOS is rather popular amongst designers and creative types... But oh well, it's a good way to learn Xcode and SwiftUI I suppose 🤷‍♀️

And I must say, SwiftUI is one, **gorgeous** (I absolutely love Liquid Glass), and very nice to **write**. Everything is declarative in code, no extra config or CSS styling, button colours, shapes, sizes, etc, fonts, it's all declared with **code**. An absolute dream come true.

The Colour Wheel I'm building (aptly named, Colour Wheel), has the following features:

- macOS 26 "Tahoe" UI consistency, native SwiftUI 🐦‍🔥
- Temporary history of colours 🎨
- Ability to copy HEX and RGBA codes to the clipboard, automatically when picking and in a details view on a specific colour #️⃣
- Menubar integration 🛠️
- Keyboard shortcuts to pick colours ⌨️
- Permanent colour history, with the ability to gave colours names (i.e. picking a Pantone and saving is as "Pantone 187C" in a list, for example) 💾
- Automatic whimsical names via RGBA distance mapping and comparison (e.g. "Metallic Grey", or "Electric Blue") ✍️
- Multiple colour preview widgets, such as Circle, Square, and Full-Width Rectangle modes 📐

If you'd like to get this utility, I'll be releasing it for free soon. I can't give an estimation for dates yet, but the app is coming along **very** nicely, it shouldn't be too far into the future. Do note that the free version won't include the permanent colour history feature however, and will have a limited temporary storage. But the full version won't cost a bomb, just a few quid ☺️

## Project Two - The Big One. Chorus 💬

So this project is far too big in scale to discuss properly in a blog post here, but [this is the GitHub Organisation](https://github.com/Chorus-Social). In short, it's an **anonymous-by-design** alternative to Reddit, or Lemmy.

Why?

Because Reddit is a cesspit of data collection, processing, AI training, and all manner of other privacy red-flags. And Lemmy, or the Fediverse in general, is a very good alternative and please do not take this as me shit-talking it, that is a fantastic alternative that I use myself every day, and I highly recommend others do to. But, it is not **anonymous**, at least not to my standards.

A lot of instances will require an email address to sign-up, or at least some form of personal information. Furthermore, the platform uses cookies and other forms of client-side storage for session tokens, user prefs, etc.

The platform I'm building, Chorus, won't store anything beyond what it needs to function.

And what is that exactly?

User IDs, Post IDs, Post Bodies, Post Votes, Moderation Information (Chorus implements a democratic moderation system where anyone can moderate the platform, via "Moderation Votes"), Community IDs, Community Names, Community Members (a composite key of User IDs and Community IDs), User Public PGP Keys, and User Display Names which are optional.

The platform doesn't take any information from the user beyond an optional display name and a public PGP key for end-to-end encryption on **all** communications. This public key is how you log into your account to, by decrypting a message containing the login code. This system was inspired by Darknet services.

To prevent against spam, Chorus implements a proof-of-work challenge that scales in difficulty depending on the action being performed. So voting on a post is a very easy challenge, but creating a post is much harder, and creating an account is the hardest. But these shouldn't cripple your device, they're just designed to make botting impractical without ASICs (if you use an ASIC to bot this little platform, then to be honest go ahead you deserve it 😂, also, seriously, get a life).

The platform is still in very early days, and doesn't have a release yet or any release date in mind. But I'm developing it in the open from day one for maximum transparency. If you'd like to take a look, that GitHub Org has all the components of the network on it, so please, feel free to go on and judge my abysmal coding skills 🙈 (a lot of the libraries and technologies used are new to me, such as FastAPI, Pydantic, SQLAlchemy, and Poetry itself to be honest).

Chorus will be funded purely through donations, so if the projects sounds cool or interesting to you, please keep a bookmark to the Organisation page and check every now-and-then for potential information on a launch (which is when a donation system will come online). Donations will be used to cover running costs and potential infrastructure expansion first and foremost, any more will allow me to allocate more time to work on the project 💪

Chorus is open-source, and the network welcomes the development of third-party clients via it's open API. So if you'd like to give back to the project in other ways, development work is always welcome 🙏

# Transition Progress 🏳️‍⚧️

So, my DIY HRT didn't work out 😔 My parents discovered what I was up to, and confiscated it, and also forced me to come out to them even though I told them I wasn't ready...

Either way, that was a chaotic week right as I came back from the air force. So they know, and haven't been the most on-board unfortunately 🙄

My partner, she is still as supportive as she always was, which is great, and my college is also very supportive and have organised external support for me, general counselling and transition-specfic support with a charity ⭐️

The transition support is roughly a three-month waiting list, and will help with getting family on-board, supporting with the medical process with supporting documents, and navigating the social transition. As well as just being someone to talk to, which is all good stuff that'll really help me, since I don't really have anyone impartial that I can speak with.

I'll be creating an unenrolled deed poll to change my name soon, just as soon as I get some time, which will probably be the upcoming half-term. I'm going with Hailey! ☺️

Speaking of, that charity, I had the first meeting "initial assessment" last friday, and that was the first time I was actually referred to by that name. It was... AMAZING! I walked into the room, greeted, and the person I was speaking with said,

"Hailey? Right.", in the usual polite name-exchange manner.

It took me by surprise I'll be honest, I don't know why but I wasn't expecting it? Took me an extra brain cycle to confirm the name than if it was my birth-given name, but it did feel good after I confirmed it. The name hits, and I like it. Now that I've changed a lot of my online platforms to use that name too, I see "Hailey" more often than my legal name now, so it is starting to actually feel like my name ❤️

# Jorb 💼

Since I'm now back at college, I'm looking for a little part time job to pay for mainly my motorbike and my private HRT, most of my other expenses are covered by my parents thankfully, although I would greatly appreciate financial independence right about now 😅

# Fin

That's about everything for now, I'll be back again soon(er), promise 😘

You are loved, you are beautiful, and you are awesome 🤩,
Hailey
