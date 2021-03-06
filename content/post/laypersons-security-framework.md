+++
date = "2019-10-06"
title = "Towards a Layperson's Security"
linktitle = "Layperson's Security"
menu= "main"
+++

## Overview

As techincal breaches and vulnerabilities are in the news nearly every day, getting [no less sinister](https://www.propublica.org/article/the-new-target-that-enables-ransomware-hackers-to-paralyze-dozens-of-towns-and-businesses-at-once), and the US Presidential elections are beginning to heat up. Looking backwards, much of the Mueller Report appears unabsorbed by folks who either should or need to know better, and the propagation of an increasing amount of tough-to-explain information which confuses and contradicts a reasoned understanding of the security landscape is annoying, at best.

To help, I'll present a simple security model for non-technical folk, for use both in one's political and private life, drawn from public information. A snoopy reader may find I have "Security Engineer" in my title these days, but none of this is the opinion of any employers past or present.

Let's dive in. First, an overview of three core pieces to security:

1) **Security Players** are (a) *Threat Actors*, who seek in some way to harm you or your mission using some technical exploit, and (b) *Security Partners*, who seek to frustrate those efforts or help you by providing services whose security matches your understanding of them,

2) **Maturity Behaviors** are habits you can learn to work better with Security Partners or otherwise reduce the risk of a Threat Actor succeeding in their goals, and

3) **Security Frameworks** are ways you choose to combine your behaviors with personal life decisions to achieve your mission.

While "leveling up" your maturity helps against a sometimes abstract notion of cyber attackers, it also helps you keep things in order (e.g. passwords) that will help greatly even in your day-to-day life.

## Threat Tiers

The multitudes of Threat Actors and the resources available to them vary drastically, and so it helps to create a spectrum with four coarse categories:

**Tier 4** actors are marginally technical, have significant time to spend, and are OK at using it to find something embarassing or otherwise exploitable about you and further their goals. They might find your address and [dox](https://en.wikipedia.org/wiki/Doxing) or [swat](https://en.wikipedia.org/wiki/Swatting) you, attempt to shame you by scrutanizing your public records or things you've written, or try to guess your email password reset questions.

It's important not to discount these methods as "not real hacking". While they aren't sophisticated, there are a lot of opportunities to do harm (a large "attack surface"), and they are very cheap and [enormously successful with miniscule effort](https://www.telegraph.co.uk/news/worldnews/sarah-aalin/7750050/Sarah-Palin-vs-the-hacker.html). The IRA activity [described by Mueller's team](https://www.brookings.edu/blog/order-from-chaos/2019/04/18/what-the-mueller-report-tells-us-about-russian-influence-operations/) included a $35 million disinformation, influence, and suppression campaigns to influence the 2016 election (among others), exclusively at this tier.

**Tier 3** actors take a big leap in technical sophistication. Often they are not amateurs but career professionals operating outside of western law and jurisdiction. They might have a budget to spend on markets to pay someone for passwords you've used on hacked services or they might run well crafted phishing campaigns: tricky emails linking to counterfeit websites which try to get you to give up your passwords, one-time login codes, or answers to security questions.

The GRU activity [described by Mueller's team](https://www.justice.gov/file/1080281/download) falls into this category. A definitive "upper bound" on this tier is that all their tools and explits are either available publicly or from many vendors at commodity prices. This makes attacks cheap and the damage from a foiled attack minimal.

**Tier 2** actors have a significantly bigger budget to purchase non-public weaponized exploit kits and so take significant steps to prevent being caught. Often, the foiled attack cost to successful attack benefit ratio flips at this tier, with a [public outing](https://blog.coinbase.com/responding-to-firefox-0-days-in-the-wild-d9c85a57f15b) costing the attacker more than the victim. According to [The Report Podcast](https://www.lawfareblog.com/report-episode-2-hack-dump-divide), the FSB was an actor at this tier before and during the 2016 election, although public information about those attacks is notably scant in detail.

**Tier 1** actors spend significant amounts researching novel vulnerabilities that nobody else knows about and deploy monitoring infrastructure to [copy](https://boingboing.net/2019/05/06/cyberspy-vs-spy.html) or [neutralize](https://googleprojectzero.blogspot.com/2019/08/a-very-deep-dive-into-ios-exploit.html) them. A recent notable example is the mass hacking against Uyghurs (Apple's [original press release](https://www.apple.com/newsroom/2019/09/a-message-about-ios-security/) and [a more recent story](https://www.volexity.com/blog/2020/04/21/evil-eye-threat-actor-resurfaces-with-ios-exploit-and-updated-implant/) are both worthwhile), a small piece of a largely physical-space operation learning about which is worthile, as well. [Here](https://www.youtube.com/watch?v=v7AYyUqrMuQ) is a great Vice piece on it.

As you may have noticed, these tiers describe technical sophistication and cost / benefit risk ratios, not impact, nor persistence, and some actors can constitute coordinated groups of threats at multiple tiers. They are the building blocks of creating a **Threat Model**, the kinds of attacks you expect and would like to defend against.

## Maturity Levels

Parallel to threat tiers, let's set out some maturity levels you can operate in to keep them at bay —

At **Level A** you think hard about what you say on the internet, realize that strangers on the internet are real people, and act accordingly. You empathize with folks and think about how it would look if someone were to take a screenshot of what you say and send it to your employer or your family. You think twice before posting your address online, pictures of your house, or your keys.

You review your password reset flows and don't pick security questions that strangers could answer. You know that there's a big difference between talking with someone who calling from the IRS and talking to someone after *you* dialed the phone number you know belongs to the IRS.

This prevents or mitigates Tier 4 attackers, ones I like to imagine as exeptionally bright and dedicated, albeit a bit mis-guided middle schoolers, from embarassing or harassing you.

At **Level B** you use a password manager (PM) to manage all of your passwords and security questions. You recognize that typing a password into anything other than your PM is a strange and dangerous thing. You realize you can be fooled with a well crafted phishing email and website sent your way at the right time. You're OK with that, because your memorized passwords go to your PM, and never to computers that are not yours, and your PM double checks for you that you're sending the right password only to the right places. My favorite PM is [1Password](https://1password.com), but [Dashlane](https://www.dashlane.com) appears good and I hear it's more usable. I recommend against LastPass because they've had embarassingly bad mistakes in their code and architecture, but I'm sure it's gotten better, so I'd recommend you keep using it if there's another reason (e.g. your company or family has gotten you used to it).

You use a PM because you realize that if you give a password to one website, you shouldn't give it to another website, because you even though *your* screen shows `******` when you type your password, the people who make and maintain the website can see it, and [sometimes](https://www.troyhunt.com/the-javascript-supply-chain-paradox-sri-csp-and-trust-in-third-party-libraries/) even a strangers whose code they reused could see it, or maybe [their colleagues who can read the logs](https://krebsonsecurity.com/2019/03/facebook-stored-hundreds-of-millions-of-user-passwords-in-plain-text-for-years/) can see it. Bad behavior is hard to catch and harder to prove, but [unethical developers](https://www.businessinsider.com/how-mark-zuckerberg-hacked-into-the-harvard-crimson-2010-3) could easily program a website to say "wrong password" just so you try some of your others.

You use a PM because it lets you easily have random passwords for every website and you let it check that you're logging into the site you think you are to defeat phishing attacks. You look forward to a glorious future where we're logging into website with fingerprints or face scans, but are very comfortable knowing your memorized passwords stay local and your remote passwords are uniqe to every security partner.

Most importantly, you rest easy because you know these behaviors protect you against [credential stuffing](https://www.owasp.org/index.php/Credential_stuffing) attacks and well crafted phishing, the attack that [breach Democratic leadership emails](https://apnews.com/dea73efc01594839957c3c9a6c962b8a) in 2016.

At **Level C** you install security patches within hours of their release. The timing on how quickly a security update is reversed into a weaponized attack varies greatly and you don't gamble with that, realizing that if you have time to shower at night, you have time to update your laptop.

For me, the biggest behavior that helped improve my time-to-update is to wind down my work and shut down my laptop at night. Just as with automatically managed passwords, I find a great sense of organization in keeping my work environment minimal as well as reviewing and closing down everything to wrap up my day.

If you aren't sure whether things you download and run come from reputable sources, you may also get a virus scanner. On a Mac, I would trust anything recommended as "[friends of Objective-See](https://objective-see.com)" with [Sophos](https://www.sophos.com/) being the one with the most resources and also cross-platform offerings. I don't personally use it, but if someone I cared about asked for a recommendation, that's the one I would recommend they try first.

This will frustrate many of the efforts of Tier 3 attacks, but not all of them. Making sure you download programs only from companies you trust and using an ad blocker like [uBlock Origin](https://duckduckgo.com/?q=ublock+origin) will help limit the number of places your browser talk to, but will (rarely!) break some sites until you learn the advanced settings. If decide to do this, you'll be taking the "red pill" into the world of peeking behind the curtain of the machines and juggling many minor inconveniences for real but questionably sized benefits.

At **Level D**, you dive into this world of doing the relatively inconvenient and marginally helpful things like using [uMatrix](https://github.com/gorhill/uMatrix) to cut out third party contents in your browser by default, and investing in a separate virtual machine (e.g. on macOS, $220 should get you Parallels running Windows 10 running Chrome) for your "miscellaneous" app installation and web browsing outside of trusted Security Partners. This stops the impact of an unknown or unpatched browser vulnerability being exploited, or spyware getting installed by accident.

Getting to the more extreme, you could start using separate hardware for tasks of varying sensitivity, e.g. a ChromeOS laptop for your web browsing that's on a separate network than the OpenBSD laptop dedicated to checking your email. These increase further the cost of a successful attack via a website you visit moving into your sensitive systems. Let's not worry about this level too much, as threat actors here face great risks and adversaries of their own with every attack and vastly exceed the value of a successful attack against most.

These levels provide building blocks for your personal Security Framework, and do not include the kinds of resources a larger organization may be able to throw at the problem. Take a moment to think about what kinds of things attackers you should worry about and what the best ways to get to 100% on Levels A, B, and C might be. Think of Level D as an enthusiast playground, there as a catch-all for all the minor inconveniences you can add on to chip away attackers with various abilities.

## Take-aways and wrap-up

This framework is meant help you organize your thinking about leveling up your cyber security, not to be done one at a time nor in any order: for you, updating your devices at lunch will be easier than migrating all your passwords to long random ones. You might be very organized but also used to being a jerk to strangers on the internet, and so maybe Level A will be the most difficult for you. The levels are ordered to match tiers, and the order in which you take them on is up to you and your needs.

Worth noting that some folks may prefer to change their lifestyles in less effort-intensive but more viscerally accessible ways: by simply being careful they type into a computer or say near a phone (or a watch!), or [not using computers at all](https://www.washingtonpost.com/world/2018/11/14/hes-supposed-shape-japans-cybersecurity-he-just-admitted-he-doesnt-use-computers/). This seems an increasingly losing proposition. The benefits of technology to both individuals and organizations have been and will continue to be exponential, not linear, and so for those of us not tasked with [operating nuclear centrifuges](https://en.wikipedia.org/wiki/Stuxnet), it's a clear-win proposition to simply move to ace the A-B-C's of security outlined above.

Also, worth noting the framework presented, intentionally, leaves a lot of ground uncovered — you might be wondering "what about enabling one-time login codes via SMS or 2FA?" or "what if someone steals my laptop bag?". Yes, 2FA helps a bit at Tier 2, but against fewer attacks than a PM will, and has [semi-expected problems](https://www.google.com/search?q=sms+2fa+breach). Physical security is a very large topic, and while common in families, where it's better addressed by non-technical means, it's a really risky and sophisticated attack for other threat actors.

Some folks [argue](https://www.vice.com/en_au/article/wjbzzy/your-phone-is-listening-and-its-not-paranoia) that this is all safe to ignore, that

> unless you’re a journalist, a lawyer, or have some kind of role with sensitive information, the access of your data is only really going to advertisers

As I [wrote in 2015](https://thlog.anfedorov.com/post/https-part-1/#ii-a-serious-problem), I don't think this is true. An open society built on rule of law depends on certain "base" security of "everyday folks". Because some of them, every day, decide to become whistleblowers, or begin talking to a lawyer about what leads to an important class action suit, or reach out to regulators to inform them of something they should be aware of. Their security is paramount to our society's functioning, and thus everyone's is.

Thanks for all those who helped me proofread and expound. If you feel I've missed anything else that is worth mentioning, please feel free to raise it on [the lobste.rs thread](https://lobste.rs/s/hapedv/towards_layperson_s_security_log), or email me directly at [com@anfedorov.me](mailto:com@anfedorov.me). Last I checked, your email will pass through Google and Apple servers and be stored by Apple on Google Cloud Storage. Please don't encrypt it, as I'm certain the internal controls on their laptops are better than ours.
