---
title: Surveillance
tags:
  - government
  - privacy
date: 2017-03-06 06:59:30
categories:
  - ethics
layout: post
---


This post is a reply to FBI Director James Comey and Deputy Attorney General Sally Yates's joint 2015 statement to the Senate Judiciary Committee.

I found the rhetoric of the statement refreshing: you can see in it the careful consideration to not frame this issue as *security vs. privacy*. Instead, the authors explicitly stated privacy as a right of the American people, supported by both the Constitution and by Congress. Of course, this was not the primary thesis of the statement. It felt as though the statement's purpose was to ease its readers into more harsh stances on encryption; it's always "privacy through encryption is great, but...".

<!-- MORE -->

I can totally see where they're coming from. They are two of the highest-ranking justice officials in the nation, and encryption is a growing barrier to their jobs and the jobs of their agents. Within our lifetimes, a huge swath of global communication has gone from "ripe for the picking" for justice officials, to "mathematically un-scrambleable". For this reason, I'm not opposed to my government coercing the provision of physical keys for encryption systems (in the same way it can coerce entry to a physical premises) when that coercion does not infringe on other rights (this goes back to the password vs. fingerprint discussion).

With that being said, there's definitely a line to be drawn in the sand. For instance, getting a secret warrant from a secret court for some secret operation is more than a little seedy in a democracy like ours. The reason this sort of practice is so unsettling to many is that it inverts the natural control in a democracy, from people over government to government over the people. And, as famed cryptographer Bruce Schneier put it, the debate over surveillance is not about security vs. privacy but instead about liberty vs. control.

In the tragic case of the San Bernadino shooting, this principle was seen in practice. To summarize, the shooter's phone was an iPhone running iOS 9. After obtaining the device, the FBI were unable to access the data because of the encryption it used. The FBI tried to make Apple engineer a workaround (backdoor), which Apple refused to do, pointing out, among other things, that enabling a backdoor on one device would set the precedent to do so on any or all devices. In the end, the FBI accessed the phone's data without Apple's help, ultimately deciding to drop the case against Apple and not to disclose the vulnerability (presumably to exploit in future cases involving iOS 9).

I think Apple made the right call here.

From a strictly non-technology standpoint, I think citing the All Writs Act (written in the 18th century) was shaky legal ground to start with. Compelling a private company to divert its own resources to government projects is, in my opinion, undemocratic (and un-capitalist come to think of it). It was pointed out in class the backdoor would pretty much just be commenting out a couple `if` statements. First off, there's a lot more overhead in modifying *and deploying* a mobile operating system than just writing a couple tweaks. I know the people who made this argument know this, so I can't even figure out why they said it other than that it sounded funny or cute. Hey, let's even say that all they needed to do was tap on the keyboard for a minute and be done. In that case, where's the line? If it's okay for the government to compel you to write 5 lines of code, what about 15? 50? 500? The only way to draw that line is arbitrarily, and I'd like to think our government has stronger reasons for its laws than "it's what we felt like."

---

In the statement, Comey and Yates seem to hint at creating tools to break encryption:

> We should also continue to invest in developing tools, techniques, and capabilities designed to mitigate the increasing technical challenges associated with the Going Dark problem.

I could be totally wrong here, but it sure does sound like that's what they're talking about. If this is the case, it is deeply worrying. The capability to break modern encryption is like a backdoor into any encrypted system. This is **awesome** power (and not in the "super rad" sense of the word). This conflict is almost reminiscent of the second amendment, which at its core, is about ~~maintaining state militias~~ liberty vs. control, in a way that's more direct than most of the other amendments.

**TL;DR** I think the government has every right to access digital systems in the same way and within the same bounds that they access physical systems. Likewise, I think private citizens have every right to live out their digital lives un-snooped and that their governments should not wittingly weaken the systems provided to them through the free market.


#### Sources

- [*Going Dark: Encryption, Technology, and the Balances Between Public Safety and Privacy*](Going Dark: Encryption, Technology, and the Balances Between Public Safety and Privacy), James Comey and Sally Yates

