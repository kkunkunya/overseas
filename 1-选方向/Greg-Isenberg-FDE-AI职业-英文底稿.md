# Greg Isenberg × Voss：FDE: The $1M/Year AI Job Explained（Forward Deployed Engineer / AI 前线部署工程师）

> 来源层级：**辅源**，不覆盖赫兹主源（ADR-0001）。
> 视频：https://www.youtube.com/watch?v=zXysLUTLjw4
> 形态：YouTube 自动字幕转录（英文原文，未经人工校对，存在识别误差）。
> 用途：完整底稿，供精读 / 检索；提炼见同目录主笔记（`Rob-Walling-...md` 等）。

---

[00:01] I know it's crazy, but there are people
[00:02] making a million dollars a year as Ford
[00:04] deploy engineers. But what exactly is an
[00:07] FDE? I know you've probably seen it, but
[00:10] I feel like a lot of people aren't clear
[00:12] as to what it is and how they could
[00:15] become one. [music] Well, in this
[00:16] episode, I brought on my friend Voss.
[00:18] And Voss is a leading expert when it
[00:20] comes [music] to FTEEs with his company,
[00:22] Veric Agents. And in this episode, he
[00:25] gives you his entire playbook, how you
[00:28] could become an FTE in 30 days. Now,
[00:32] this episode is for people who want to
[00:34] become an FTE, but also for people who
[00:36] are just interested in what it [music]
[00:38] means, how they can actually use FTEEs
[00:41] in their business to be make more money,
[00:44] to be more productive. And I just think
[00:46] this is the clearest episode, the
[00:49] clearest piece of content on the
[00:51] internet, the clearest master class for
[00:54] how to understand clearly what an FDE
[00:58] is, how you could become one, and why it
[01:02] matters. Enjoy the episode, and I'll see
[01:04] you at the end.
[01:16] Voss is here. And Voss, by the end of
[01:16] this episode, what are people going to
[01:19] learn?
[01:20] &gt;&gt; They're going to learn exactly how to
[01:21] break into forward deployed engineering
[01:23] or become a better FTE in 30 days. The
[01:26] full road map for AI forward deployed
[01:28] engineering.
[01:28] &gt;&gt; And I don't feel like this has been
[01:29] shared anywhere. I feel like the term
[01:32] forward deploy engineer is just like on
[01:35] my X feed everywhere. So, what I'm
[01:37] hoping for, Voss, is for you to clearly
[01:39] explain what this means and just like
[01:42] all the concepts to it and just break it
[01:44] down for me in a clear, easy to
[01:46] understand way. So, so I could uh so I
[01:51] could, you know, learn from it, but so
[01:53] others could learn from it, too.
[01:55] &gt;&gt; Absolutely. And there's a lot of
[01:56] different definitions. Everyone has
[01:57] their own. And I'm going to give you
[01:59] what I think is the clearest
[02:00] explanation.
[02:01] &gt;&gt; Okay, let's do it.
[02:02] &gt;&gt; Sweet. So, yeah, this has never been
[02:04] shared before. our team put together uh
[02:06] it's how to break into FD in 30 days.
[02:09] Let's start off with uh recent
[02:11] developments and the facts of today. The
[02:13] reality is every company can now buy
[02:16] intelligence. You know, you have a
[02:17] frontier model being released every
[02:19] single day. Just yesterday we had Kimmy
[02:21] 3 being released. Uh last week was Fable
[02:24] uh 5, you know, or GPT 5.6 Soul. Every
[02:27] company can now buy intelligence and the
[02:30] reality is intelligence is becoming
[02:31] commoditized. So the same foundational
[02:34] capability is becoming available to
[02:36] anybody who can pay for it and that's
[02:38] most companies today. So you'll see here
[02:41] is a graphic where every company has
[02:42] access to the same foundational model.
[02:45] So if everyone can access it,
[02:47] intelligence can no longer be the mode.
[02:49] I think there was this huge theory that
[02:52] you know people will be priced out of
[02:54] intelligence and that could be the case
[02:56] in the future but the reality is today
[02:58] everyone has access to the same tools.
[03:00] If you go and talk to 50 different
[03:02] enterprise clients, they're all using
[03:03] the same stack. They're all using cloud
[03:05] codeex. They're using cursor for model
[03:07] agnosticism. Uh they're using GitHub
[03:09] copilot. It's all the same thing. So the
[03:12] reality is everyone has the same
[03:14] capability in terms of what intelligence
[03:16] tap they have access to.
[03:19] So where does the advantage go? It goes
[03:22] into deployment. So the edge is no
[03:24] longer who has the intelligence. It's
[03:26] where, how, and why they use it. And
[03:28] that is the role of an AI for deployed
[03:31] engineer. It's allowing companies to
[03:33] harness and take advantage of AI
[03:36] intelligence or software previously to
[03:39] make sure that they apply it the best to
[03:41] their specific company context. Every
[03:43] single company is different in terms of
[03:46] how their business is structured, what
[03:48] processes they have, how things run,
[03:50] etc. And the job of an FD is to make
[03:53] sure that the intelligence which is
[03:54] general is specifically applied to this
[03:57] company in a way that benefits them the
[03:59] most. And the advantage will start to
[04:01] become who has that best bridge that
[04:03] connection between their own processes
[04:06] and the intelligence stack that they
[04:08] have access to.
[04:09] &gt;&gt; And Voss this was a term that correct me
[04:12] if I'm wrong was popularized by the
[04:15] Palunteer team. Right.
[04:16] &gt;&gt; That's right. So can you know can you
[04:19] tell me about like how Palunteer I think
[04:23] how Palunteer works with FDES? I mean I
[04:25] feel like for a lot of people Palunteer
[04:27] is this black box. Can you can you go a
[04:29] little more into that?
[04:30] &gt;&gt; Yeah it's funny. So I lived in New York
[04:32] for a few years and I had a ton of
[04:33] buddies who are Palunteer for deployed
[04:34] engineers. So I have a little bit of
[04:35] insight into this.
[04:37] &gt;&gt; Um without sharing what I what I think
[04:39] is proprietary. Palunteer has an
[04:41] ontology. They have a software stack
[04:42] that they work off of and this is full
[04:45] of connectors to software but also data
[04:47] links which allow people to which allow
[04:49] enterprises to pipe their data into a
[04:51] unified interface and what Palanteer
[04:53] FDES then do is they'll actually be
[04:55] deployed on site. So this is either like
[04:57] enterprise customers or the military the
[05:00] government um and learn their workflows
[05:02] and then spin up kind of workflows
[05:04] dashboards you know agents that will
[05:07] solve the problem for these companies.
[05:09] So Palunteer really popularized the idea
[05:11] of essentially which was what was
[05:13] consulting but for the software space
[05:15] they coined the term for a deployment
[05:16] engineer and it really started to allow
[05:19] their business to take off. They had a
[05:20] centralized platform but its beauty was
[05:23] not in like how tech forward it was. It
[05:25] was it was in how customizable it was
[05:28] and then these forward deployment
[05:29] engineers would go on site customize it
[05:31] per client and it would really solve
[05:32] their pain points better than a
[05:34] generalized servers.
[05:36] &gt;&gt; Cool. And I guess like the the thesis is
[05:39] that if it works for Palunteer, it can
[05:42] work for everyone else, right?
[05:45] &gt;&gt; That is sort of the thesis. Yeah. And
[05:47] the Palunteer I think really solved it
[05:48] when it came to the data age where you
[05:51] wanted to unify your data sources and
[05:52] then visualize it in more unique ways. I
[05:55] think the AI age is going to demand that
[05:57] 100 times more where every single
[05:59] company is going to need customized
[06:00] agents. And uh that's actually what
[06:02] we're here to solve as well with our
[06:04] with our OS. But everyone is sort of
[06:07] coming to this same realization that
[06:08] forward deployed engineers are a massive
[06:10] reason why AI is going to be powerful
[06:12] for businesses.
[06:14] &gt;&gt; Cool. Let's keep going.
[06:15] &gt;&gt; Sweet.
[06:17] So someone has to decide where
[06:19] intelligence belongs not just where it's
[06:21] applied. And that person is a forward
[06:22] deployed engineer as well. So there's
[06:24] kind of three stages to a forward
[06:26] deployed engineer's involvement at a
[06:28] company. The first is understanding the
[06:30] business reality. So it's how the work
[06:33] actually happens today. And I think this
[06:35] is the part that gets glossed over by
[06:37] people who are you know very deeply in
[06:39] tech. You know in Silicon Valley we have
[06:40] a mindset where like okay well the
[06:42] beauties in the software like it doesn't
[06:43] really matter what the business
[06:44] processes are. But I can tell you
[06:46] firsthand every business is so different
[06:49] even in terms of like the same process
[06:52] across multiple businesses. Let's go
[06:53] like accounts payable for example or or
[06:56] sales for example at two different
[06:57] companies. The way that they do that is
[07:00] so different. One has a 10-step process,
[07:02] one has a 30-step process. One is using
[07:05] Salesforce Gong uh and uh Chili Piper.
[07:09] The other one is using HubSpot and uh
[07:12] Apollo and Clay. There's the software
[07:15] differences, but there's also the
[07:16] process differences, and there's the
[07:18] things that matter most to the business
[07:20] being very different. Um when things go
[07:22] wrong, like exception handling, the way
[07:24] that that's being done at a company
[07:25] needs to be documented as well. So Ford
[07:28] deployed engineers go on site, they'll
[07:31] either interview people or just observe
[07:33] them work or get, you know, access to
[07:35] their systems like their ERPs, their CRM
[07:38] to figure this stuff out. And this is
[07:40] where the bulk of the time goes in my
[07:42] opinion. Um, it cannot be understated
[07:44] how important this is both in terms of
[07:46] understanding the business, but also to
[07:48] bring that business along the journey.
[07:50] And this is where communication and
[07:52] analytical ability is incredibly
[07:54] important for a forwardlook engineer.
[07:56] Um, the way I like to think of an FTE is
[07:58] the best combination of someone very
[08:01] deeply technical who can understand it,
[08:02] but also someone with fantastic
[08:04] communication ability and the ability to
[08:07] get the information out of people that
[08:08] they need to. Um, and this is
[08:11] all-encompassing for business reality.
[08:13] &gt;&gt; And you know, you say the FDE goes on
[08:16] site. When you say onsite, is that like
[08:18] literally like walks in the office and
[08:21] starts like speaking to people and stuff
[08:22] like that or do you mean like you know
[08:26] &gt;&gt; it can it can certainly be done
[08:27] remotely?
[08:28] &gt;&gt; Yeah.
[08:29] &gt;&gt; Um and you know there's there's certain
[08:31] times where that's you know required
[08:33] because a company itself is remote or
[08:35] like the people at the function are not
[08:36] all in one office but I will say a large
[08:39] majority of the time it is on site. I
[08:41] know that Palunteer does this very
[08:43] heavily. uh we do this as well and it's
[08:45] not just because you know you can't get
[08:47] the information remotely but it's it's
[08:49] it's actually more so because the
[08:52] relationship that you build with the
[08:54] person like you know you're on site
[08:55] you're part of the team you'll uncover
[08:57] far more information that way right like
[09:00] if somebody will simp if you schedule a
[09:01] 1-hour meeting for example somebody will
[09:03] walk you through what they think is the
[09:05] job but if you're on site with them for
[09:08] the full 8 10 hours whatever it is
[09:10] you're actually experiencing the job
[09:12] like when something goes wrong that's
[09:14] not really documented in an SOP or like
[09:16] a in a word doc or a Google doc
[09:17] somewhere you're going to see that play
[09:19] out. Um you know even consultants of
[09:21] McKenzie they do this they'll go on site
[09:23] to a mine and they'll sit with the
[09:25] miners and they'll watch them do their
[09:26] work uh because it's so much more
[09:28] powerful to establish that relationship
[09:30] and get the information that way.
[09:32] &gt;&gt; Cool.
[09:34] &gt;&gt; Yeah. The second step is FD judgment
[09:36] which is where does intelligence belong
[09:38] and where does it not? I think when the
[09:40] AI wave first started, we saw a lot of,
[09:43] you know, let's just slap AI everywhere.
[09:45] Let's let's give everything to the model
[09:46] and let's let's let it figure it out.
[09:48] Um, and this is what led to token maxing
[09:51] and hallucinations. Then you have the
[09:52] the MIT stat that 95% of generative AI
[09:55] pilots fail. Um again now the industry
[09:59] is sort of shifting gears and they're
[10:00] realizing that okay we actually need to
[10:02] be very selective about where we apply
[10:04] this intelligence and we also need to be
[10:06] selective about how we design the new
[10:09] stack for this intelligence to play out.
[10:10] So again for example you have a 10step
[10:13] workflow it might be that you know that
[10:16] workflow should not be changed by AI.
[10:19] You know maybe it's too risky or maybe
[10:20] it's not high enough ROI. Maybe it's
[10:23] already pretty automated. Why do we need
[10:24] to do bring AI into it? Um, it also
[10:27] could be that of those 10 steps, only
[10:31] three of them actually need judgment,
[10:33] right? So, categorization of this, you
[10:36] know, lead in a CRM tool, that might be
[10:37] a little bit more non-deterministic. So,
[10:40] we're going to bring in an LLM there for
[10:41] for judgment. But the rest can be solved
[10:44] with with, you know, if then else
[10:46] statements. It can be solved with API
[10:48] calls. And this sort of judgment is
[10:50] actually, you know, far more complex
[10:52] than I'm making it out to be even. But
[10:54] it belongs with the FDE. So the FDE both
[10:57] has again the business reality which is
[10:59] the consulting style like communication
[11:02] style approach, but also the technical
[11:04] judgment so that they can determine
[11:06] based on their technical background.
[11:08] Okay, I think that this design is going
[11:10] to be, you know, risky. We're going to
[11:12] have 80% accuracy. It's not worth it.
[11:14] Versus this other, you know, workflow
[11:16] will will have a much higher ROI. will
[11:18] be able to build it much faster. It's
[11:19] lower risk, etc. And that sort of back
[11:21] and forth judgment is where an FD really
[11:23] shines. It's bridging the gap between
[11:25] the business and the technology.
[11:27] &gt;&gt; If you, you know, just curious like if
[11:29] if someone listening to this like wanted
[11:31] to become a foreign deployed engineer in
[11:34] New York City that's doing this sort of
[11:35] stuff, like how much money could they
[11:38] make?
[11:39] &gt;&gt; A lot of money. You have uh no idea how
[11:42] expensive it's gotten. Both from a we're
[11:44] hiring perspective, but also in terms of
[11:46] what the market's demanding. This is the
[11:48] hottest role in technology right now. I
[11:50] mean, you could make anywhere from
[11:53] 150,000 base with considerable equity to
[11:56] I've seen roles go up as high as a
[11:57] million dollars a year. And I'm not
[11:58] joking. Um, these are extremely well
[12:01] compensated roles if you are the best
[12:03] combination of consulting and
[12:05] technology.
[12:06] &gt;&gt; Cool.
[12:08] &gt;&gt; Um, deployed AI system. Finally, the
[12:11] last step is actually going out and
[12:13] building the software itself. This is
[12:15] where it varies wildly company by
[12:18] company. For example, at Palunteer even
[12:20] they have some FTEEs that you know
[12:22] you're not actually writing code. You're
[12:23] mostly like spinning up workflows like
[12:25] text. You're chatting with the software
[12:27] of the Palunteer ontology to create like
[12:30] some dashboards and to the extent you're
[12:31] writing code it's SQL. But there's other
[12:33] companies where you are fully writing
[12:36] like production code either on-site with
[12:38] a client or you'll go back and and do
[12:40] this but it varies wildly. So there are
[12:42] some FTE roles where you're going to be
[12:44] writing production code. You need to
[12:46] have a background in software
[12:47] engineering and like really be confident
[12:49] in your ability there. There's other FTE
[12:51] roles where it's far more technically
[12:53] light and you can you know chat to build
[12:56] um on top of an existing platform. So
[12:58] this is the part that varies wildly. But
[13:00] either way, you need to have a very good
[13:02] understanding of the software because
[13:04] when the client has an issue with, hey,
[13:05] this doesn't work right or we have an
[13:07] issue in production, it's basically your
[13:09] ass on the line and you have to know who
[13:11] to call, what to do, and how to fix it.
[13:14] &gt;&gt; Totally.
[13:14] &gt;&gt; In summary, FTEEs are in demand because
[13:17] they control how intelligence enters the
[13:19] business, how it's used, and that is
[13:22] where all the value is today in the AI
[13:23] age. Everyone is coming to this
[13:25] consensus, and that's why FDS are
[13:26] extremely valuable. Well, it's also in
[13:29] demand because it's new as well. Like
[13:32] this, like there wasn't intell super
[13:34] intelligence on tap five years ago. So,
[13:38] not only is the idea of super
[13:41] intelligence on tap just absolutely
[13:44] absurd. Many trillion dollars of, you
[13:48] know, money is going to be changing
[13:49] hands over the next few years. But the
[13:51] idea that now you need a person to
[13:53] actually like people are realizing hey
[13:55] you actually need judgment and hey you
[13:57] actually need to like you know be a
[13:59] systems thinker and hey like actually
[14:02] token maxing isn't the best strategy.
[14:05] Like there was like a moment in time
[14:06] where token maxing like people were
[14:10] people basically were agreeing that
[14:12] token maxing was the strategy. It was
[14:14] just like hey these models are so good
[14:16] let's just let them do their thing. That
[14:18] was like the thinking.
[14:20] Yeah, that was a a funny period in time.
[14:23] I would argue we're still not fully out
[14:24] of that. But yeah, um yeah, you're
[14:26] totally right. I mean, this is a brave
[14:28] new world for everyone involved. And
[14:30] &gt;&gt; I mean, I I have horror stories of of
[14:33] people of of like seuite executives I've
[14:35] talked to who have blown through their
[14:36] entire $10 million claw budget in like 3
[14:40] months. It was supposed to last them a
[14:41] year, but because they gave it to
[14:42] everybody, it's token maxing and
[14:44] everyone's spinning up whatever they
[14:45] need. And and and the sad reality is it
[14:48] didn't really move the needle for the
[14:49] business either. And it's because that
[14:50] business didn't really invest heavily
[14:53] into forward engineering. And so I think
[14:55] you're totally right.
[14:56] &gt;&gt; Cool. Let's keep going.
[14:59] &gt;&gt; Sweet. So we we've already alluded to
[15:01] this, you know, pretty heavily prior,
[15:03] but I want to really make sure I hammer
[15:05] down this point, which is that there's
[15:07] two uh sort of streams of of kinds of
[15:11] judgment that are required, and it's
[15:13] very rare in a in a single person. So I
[15:15] think the the unfortunate reality is and
[15:17] this is what's going to happen. It's
[15:18] already starting to happen is as you
[15:21] know we go from the token maxing let's
[15:23] go all in on token maxing go to now the
[15:26] same thing on FD let's go go go let's
[15:27] hire a bunch of fes I want to be very
[15:30] clear about what the role really
[15:31] demands. I think there's a lot of fees
[15:33] who are you know unfortunately neither
[15:35] the best communicators and neither the
[15:36] best software engineers. I would
[15:38] strongly urge them to strengthen both of
[15:40] those skills. It's both the
[15:42] understanding of workflows, cost,
[15:44] incentives, risk, adoption, business
[15:46] value, um, you know, the politics of the
[15:48] internals of a company. These are all
[15:50] things that you have to manage and
[15:52] consultants here are incredibly strong,
[15:55] right? You'll talk to McKenzie
[15:57] engagement managers, BCG, Bane
[15:58] engagement managers, they'll be very
[16:00] good at this side. Um, the other side is
[16:02] what they might need some more support
[16:04] in. And same thing software engineers
[16:06] will be very good at the right side with
[16:07] models systems APIs data code
[16:10] reliability uh eval guardrails you know
[16:13] more AI centered terms harnesses post
[16:16] training fine-tuning these are things
[16:18] that are more on the technical side of
[16:20] the aisle and software is usually very
[16:22] good at this but they need to also then
[16:24] kind of drift towards the business side
[16:26] um by understanding the left side of the
[16:27] aisle and FTE is the best combination of
[16:30] both of these it's not an average
[16:32] combination it's not the worst
[16:33] combination of both where you know
[16:35] you're not the best communicator but you
[16:36] also can't code. It is truly the best of
[16:39] both and that is the milliondoll hire
[16:41] where the FD can turn business
[16:43] understanding into working software end
[16:44] to end. They can do both sides
[16:46] perfectly.
[16:47] &gt;&gt; Yeah. I mean put another way it's like
[16:49] if you understand art and you understand
[16:51] science
[16:52] &gt;&gt; and you could speak both
[16:55] &gt;&gt; you have what it takes to become a the
[16:58] million-dollar FD. The the hard part is
[17:00] like usually the people that are good at
[17:03] good at science are sort of good at
[17:05] science and the people that are good at
[17:07] art are kind of good at art. Um but
[17:11] there you know there is some overlap in
[17:13] the ven diagram.
[17:15] &gt;&gt; Absolutely. And that's why it's such a
[17:17] rare role. But I also firmly believe and
[17:19] that's kind of the whole point of this
[17:20] presentation is that you can become
[17:22] this. It's it's not out of the realm of
[17:24] possibility to become much better at
[17:25] both of these things. It just you need
[17:27] it cleanly laid out. you need a road map
[17:29] and that's what I hope that I can
[17:30] provide by the end of this call.
[17:32] &gt;&gt; Cool. All right. All right, boss.
[17:34] &gt;&gt; Let's go. [laughter]
[17:39] &gt;&gt; So, first you know for example, it's
[17:39] understand how the work is really done.
[17:42] Um
[17:43] because the documented process is very
[17:45] rarely the the real process, right? So,
[17:46] an email might arrive. Now, this is
[17:48] extremely simple, but the reality is it
[17:51] sounds like a clean trigger, but it's
[17:52] it's far more complicated than that. It
[17:54] arrives from 40 plus senders. No two of
[17:57] them are formatted alike. the data is
[17:58] different. Some of it's in a PDF, some
[18:00] of it's in a screenshot, some of it's in
[18:02] an Excel spreadsheet, or it's buried in
[18:04] a forwarded thread. It's it's far more
[18:06] complex than it makes out to be. So, if
[18:08] you didn't look into this, if you
[18:10] weren't an FD and you just asked the
[18:12] person for, hey, what's the first step
[18:14] of the workflow? They'll tell you an
[18:16] email arrives. And all of a sudden,
[18:18] you're building for a system that
[18:19] doesn't map to reality versus the
[18:20] reality, which is that it's so
[18:22] complicated. And half of them are
[18:24] exceptions. It's the same as last time.
[18:25] It ignores the second attachment. Sarah
[18:27] already signed off on this one. There's
[18:29] no consistent subject line, so you can't
[18:31] route without actually going into it.
[18:33] And usually the reality of how to play
[18:36] this is in one person's head. So one
[18:38] person will know like, okay, yeah, well,
[18:39] when I see this email from this person,
[18:41] they'll send it to this this vendor or
[18:43] to this part of our procurement team.
[18:45] But that's not written down. And if you
[18:47] don't sit with that person, kind of coax
[18:49] this all out of them, they're not going
[18:50] to remember to even tell you. um you
[18:52] would think about like at your job today
[18:54] I asked people viewing this how easy is
[18:56] it for you to really write down every
[18:59] single exception that [laughter] might h
[19:01] happen in your job I was a software
[19:03] engineer at meta and if people ask me
[19:04] for my job I'd say well yeah I code all
[19:06] day I'll get a task and I'll I'll work
[19:08] on it but that's not the reality right
[19:10] the reality is I have meetings you know
[19:11] this happens something breaks in prod I
[19:13] have to go fix it that's what we're
[19:14] getting at here the second step is oh
[19:17] it's copied into a spreadsheet same
[19:18] thing here you get the idea one's a real
[19:20] one two are stale data validation. It's
[19:22] rekey by hand, columns drift. Same thing
[19:24] with checking into an internal system. I
[19:27] won't get into all this. You get the
[19:28] idea. Every step is extremely
[19:29] complicated. Um, so that's what
[19:32] understanding the work really means. It
[19:34] takes time and it takes effort to sit
[19:37] with a person responsible and sometimes
[19:38] multiple people responsible.
[19:41] &gt;&gt; Usually, usually it's multiple people.
[19:43] &gt;&gt; Very, very often. Yeah. I mean, if this
[19:45] company has like 5,000 10,000 people
[19:47] working in it, chances are you have a
[19:49] lot of people working on the same thing.
[19:51] Then you decide how the work should
[19:53] operate when intelligence is built in.
[19:54] So again, where does the terministic
[19:56] software live in? Where does the agent
[19:57] act? Where does the human approved?
[19:59] Where does the record get updated? I
[20:01] think the best combination of sorry, the
[20:03] best solution of AI for most companies
[20:05] is a very good combination of
[20:08] deterministic software. Probably the
[20:09] majority of it is that, but then
[20:11] obviously the the judgment that API
[20:13] calls to LM can provide. And then
[20:16] finally, human loop.
[20:18] So this is just a fancy little little
[20:20] digest, but it's really the agent that
[20:22] can then be deployed into existing
[20:23] systems. It's doing the first half,
[20:26] which is intake, validation, agent
[20:27] drafting, and then you have a human in
[20:29] the loop for approval. This is something
[20:30] that I strongly recommend my FDES to
[20:32] push for in a in a in an agent
[20:34] implementation. Once you hit approve,
[20:37] it'll then go through the latter half of
[20:38] the steps, and that's what you're
[20:40] building. So the job of an FTE when
[20:42] you're building has three parts. It's
[20:43] obviously auditing, then creating
[20:45] evaluation suites to make sure the
[20:47] system behaves correctly. This is
[20:48] extremely important in the AI age. And
[20:50] then finally, deployment, which is both
[20:52] handholding the client to make sure
[20:53] they're adopting it, it's working well
[20:55] for them, but then also the software
[20:56] side, making sure that nothing breaks.
[20:58] You're monitoring all the metrics that
[20:59] matter. You're monitoring KPIs, SLAs's,
[21:02] and everything needs to be topnotch for
[21:04] somebody to really trust you as an FD.
[21:06] And every stage is a prerequisite for
[21:08] the next. So for an eval so prove the
[21:12] system behaves correctly. So in a
[21:14] scenario where uh the outcome you know
[21:18] is non-deterministic meaning like it's
[21:21] tough to say what success looks like how
[21:24] do you create an eval or can you create
[21:26] an eval for more creative task or tasks
[21:30] that are hard to like understand if it's
[21:34] successful or not.
[21:36] &gt;&gt; Yeah. for for obviously for you know
[21:38] more non-deterministic tasks it's much
[21:40] harder right it's much easier to say
[21:41] okay was this email categorized
[21:43] correctly because we have 10,000
[21:45] previous emails to go off of and it'll
[21:47] be the basis for our email set but even
[21:49] for tasks where it is non-deterministic
[21:51] like for example creating a presentation
[21:55] right there's a million different ways
[21:56] to do it and
[21:58] sort of the beauty is in the eye of the
[21:59] beholder where you know one thing looks
[22:01] good to me might look bad to you um here
[22:05] it's very helpful to have as much
[22:06] previous data as possible. Obviously, if
[22:09] you have 5,000 previous presentations to
[22:11] go off of, it makes it a lot easier to
[22:12] create this golden data set of what we
[22:14] think matters. You know, you can say,
[22:16] you know, always put the logo in the top
[22:18] left, always have larger font of this
[22:20] styling, etc., etc. But this is
[22:23] obviously where you'll never get to a
[22:25] perfect result with just evals. need
[22:27] human in the loop feedback to make sure
[22:29] that going forward you at least have a
[22:31] feedback mechanism that improves your
[22:33] harness if not like post- train uh or
[22:36] fine-tunes the model that you're working
[22:37] under. So on one hand like get as much
[22:40] data as you can and kind of determine
[22:42] like what looks good, what looks bad,
[22:43] identify like what matters to you, but
[22:45] also then always bake in human loop
[22:47] feedback because even with a good data
[22:49] set, even with good evals, you'll need
[22:52] to have them constantly improved. And
[22:54] that's where that feedback mechanism
[22:55] comes into play.
[22:56] &gt;&gt; And I've noticed like in this entire
[22:59] presentation, this entire podcast, we
[23:01] haven't really spoken about which LLM to
[23:05] use. Are you like basically agnostic in
[23:07] terms of like working with Anthropic or
[23:10] OpenAI or Google or like if you're an
[23:13] FDE basically, how do you think about
[23:17] which
[23:19] LLM to work with?
[23:21] &gt;&gt; Yeah, great question actually. Um,
[23:22] something I probably should have touched
[23:23] on. Uh, we as a company are extremely
[23:26] model agnostic. So we think our value
[23:28] lies in our ability to be switching from
[23:31] one model to the next and making sure
[23:32] that your accuracy only improves, your
[23:34] cost only goes down and you're not
[23:36] marrying to one intelligence provider,
[23:38] which we think will be an asset going
[23:40] forward. Um, you don't want to
[23:42] monopolize your intelligence, your
[23:43] inference layer. That being said, if I
[23:45] was an FTE today or if I was trying to
[23:47] become the best FTE today, I would stick
[23:50] to one model and one agent building
[23:52] platform. OpenAI has one, Cloud has one,
[23:55] agent SDK, etc. every single model
[23:57] provider has one. Get very very good at
[24:00] one of them because that will be the
[24:02] foundation that you then you know okay
[24:04] let's let's try out claude tomorrow if
[24:05] I'm already good at open AI's you know
[24:07] Asian building platform okay I feel more
[24:08] confident about that let's go to Kimmy 3
[24:10] or GLM 5.2 too. Let's see what the open
[24:12] source models can do. Let's build a
[24:14] proprietary harness. That's how I would
[24:16] go about it. Um, but I wouldn't really
[24:19] worry about being model agnostic when
[24:20] you're starting out as an FD because
[24:21] that's again not where your value lies.
[24:23] Your value lies in how good are you at
[24:25] understanding both sides of the aisle
[24:27] because that can then apply to any
[24:28] model.
[24:29] &gt;&gt; Totally. And it's we're getting to a
[24:32] point where
[24:34] the models
[24:36] are
[24:38] very similar in a lot of ways.
[24:40] &gt;&gt; Yeah. And a lot of the big players are,
[24:43] you know, they have like Google will
[24:45] have their frontier model, but they'll
[24:47] also have an open source model, for
[24:48] example. And so now you're getting to
[24:50] this place where it's like, okay, you
[24:52] can play with their open source model,
[24:53] you can play with their um, you know,
[24:56] frontier model. And and so I I expect
[24:58] that the arrow of progress around LLMs
[25:02] is they're going to have a bunch of
[25:04] different products for you to play with.
[25:06] So yeah, I agree. Like if you want, you
[25:09] know, pick pick an ecosystem, bet on an
[25:12] ecosystem that you believe in for
[25:14] whatever reason, be the best at that
[25:17] ecosystem. And then as you become the
[25:19] best, then it's like, okay, if you want
[25:22] and you're working with a client, for
[25:23] example, and for whatever reason,
[25:27] another model makes more sense, then
[25:29] great. You know, you
[25:31] &gt;&gt; Yeah,
[25:32] &gt;&gt; you can go and recommend that.
[25:34] &gt;&gt; Absolutely.
[25:36] Yeah,
[25:36] &gt;&gt; I would say that that's exactly right.
[25:37] And then just to really hammer the last
[25:39] point in, your ability to determine what
[25:42] model is best for a task relies on your
[25:44] understanding of various different
[25:46] models. You're benchmarking them along
[25:47] the way. But to your point, don't put
[25:49] the card ahead of the horse. Like really
[25:51] get good at one before you then try to
[25:53] venture out and make that understanding.
[25:54] I would totally agree.
[25:55] &gt;&gt; Yeah. I mean, that's like
[25:59] Yeah. You don't want to like hammer a
[26:00] specific, you know, model
[26:04] and you don't understand
[26:06] what the system and the set of tasks
[26:09] are. It's like
[26:10] &gt;&gt; the equivalent of, you know, you're a
[26:12] waiter and you just hand someone a glass
[26:14] of pino noir and they're like, I didn't
[26:18] ask for that. You know, you you know, a
[26:20] good restaurant has a sleier and and and
[26:24] sier's job is to understand what is your
[26:26] pallet? Um, do you like dry wines? Do
[26:28] you like wines from, you know, uh,
[26:32] France, you know, southern France or
[26:35] northern France or, you know,
[26:38] &gt;&gt; Yeah.
[26:39] &gt;&gt; I'm not the biggest wine guy, so I, you
[26:42] [laughter] know, the analogy might break
[26:44] down, but that idea, I think, of just
[26:46] like understanding what people want
[26:48] first and then deploy makes a lot of
[26:51] sense.
[26:52] &gt;&gt; Yeah. I mean, honestly, I thought that
[26:53] was pretty good. Like, familiarity of of
[26:56] agents is an FTE. Like you really go in,
[26:58] figure out what they want and then you
[26:59] give it to them, right? You might give
[27:01] everybody pen noir. It might work for
[27:02] some of them, but it's not going to work
[27:03] for most. And that's why again most AI
[27:05] pilots fail
[27:06] &gt;&gt; 100%.
[27:08] &gt;&gt; Cool. All right, let's let's keep going.
[27:10] &gt;&gt; Sweet. This is again more of the same.
[27:13] Find the workflow worth rebuilding. I'm
[27:15] going to link this I'll have Greg link
[27:17] this this document, you know, in the in
[27:18] the in the channel. So, if you guys want
[27:20] to dive in deeper in here, but the idea
[27:22] is again the same. collect the context,
[27:24] trace the FD findings, figure out the
[27:25] bottlenecks, the repetitive work, the
[27:27] judgment points, all that stuff, and
[27:29] then produce the operating map. And this
[27:31] back and forth is why having the
[27:33] understanding of the business and the
[27:34] tech is super important.
[27:37] &gt;&gt; Cool. By the way, if you go back to the
[27:39] audit, like if you want to be an FDE, um
[27:44] you know, we just had an episode with um
[27:47] Corey Ganim who he came on the podcast
[27:49] and he basically he was he talked about
[27:52] selling audits as a way to to learn
[27:55] about someone's business and then deploy
[27:56] AI afterwards. Like you can sell the
[28:00] audit, right? like
[28:02] &gt;&gt; in charge for the audit
[28:04] &gt;&gt; and then
[28:05] &gt;&gt; the implementation you can charge like a
[28:08] monthly fee or you can charge a onetime
[28:10] fee. How should people think about that?
[28:12] &gt;&gt; Yeah. So actually we're in this exact
[28:13] business of you know implementing AI
[28:15] across the largest companies on the
[28:17] planet and we require every single
[28:20] engagement to start with an audit which
[28:23] you know obviously costs money to the
[28:24] business. Um this is extremely valuable.
[28:27] I think again like there's a lot of
[28:29] misunderstanding like you know you can
[28:31] just throw AI on the on the on the on
[28:34] the uh the company. The audit is worth
[28:36] so much money to a business. I mean
[28:38] we've had companies that tell us like
[28:40] the audit was worth 10 times what they
[28:42] paid for. It's it's better than McKenzie
[28:44] because it's so telling. AI is so new
[28:47] like you said no one really understands
[28:49] how to go about an audit. But if you're
[28:51] able to say like look here is in your
[28:54] department here are all the different
[28:56] workflows and we've mapped them out very
[28:58] cleanly right we have the full steps the
[29:00] back and forth the exception handling
[29:01] we're going to map that out for you and
[29:03] we're also going to tell you what we
[29:05] think is worth automating versus what
[29:07] isn't give them that priority map give
[29:09] them that matrix that ROI matrix and
[29:12] then go ahead and show them how you
[29:15] would build it and show them the ROI
[29:16] show them the use case that is worth so
[29:19] much money to a company I I think this
[29:21] is something that even most consulting
[29:23] firms are not able to figure out and
[29:25] this is where you have an edge if you
[29:27] are really up to date on AI and you
[29:28] actually know live and breathe it
[29:30] yourself. Um the audit is worth a ton of
[29:33] money to a business.
[29:35] &gt;&gt; Totally. It's also a chance for you to
[29:37] like build trust with them.
[29:39] &gt;&gt; Yeah.
[29:40] &gt;&gt; You know what I mean? and and and show
[29:43] them how you work and underpromise and
[29:45] overd deliver and and and it gets their
[29:49] creative juices flowing around like okay
[29:51] I didn't realize that you know cuz
[29:53] you're producing like an operating map
[29:55] right so you didn't realize like oh hey
[29:57] like you know I never thought about that
[29:59] use case or I didn't think that you know
[30:02] this would produce this expected
[30:04] business value um maybe it's worth
[30:07] investing in
[30:08] &gt;&gt; absolutely it's funny you When we first
[30:11] started, you know, the company, it was
[30:12] last year. This is before FDUs were
[30:14] really a big thing. Um, we used to call
[30:17] the audit the medicine that neither one
[30:19] of us wants to take, right? Like a lot
[30:22] of companies are like, "Oh, like, do I
[30:23] have to do an audit? Can't you just like
[30:24] token max and start building?" But it
[30:27] really is so valuable and they realize
[30:29] that as the audit goes on. So, I totally
[30:31] agree.
[30:32] &gt;&gt; Yeah. We um cuz we we we also have an
[30:36] agency called LCA. Um and
[30:40] LCA is well known for building like
[30:44] working with the biggest companies on
[30:45] the planet and then taking their
[30:46] products from a product perspective and
[30:49] bringing them into the AI age. So like
[30:51] from a you work with like a Dropbox and
[30:53] what is an AI first version of Dropbox
[30:55] or Slack and AI first version of Slack
[30:57] look like? And we started doing audits
[31:00] as like, hey, let's audit your product
[31:02] first. What we noticed was the word
[31:04] audit
[31:07] was a tough pill for people to swallow.
[31:10] And we just rebranded audit as a sprint.
[31:13] So it would be like it was a design
[31:15] sprint. We just kind of like and we
[31:17] like, you know, brought in the the the
[31:20] concept of an audit um with it. Um so we
[31:24] noticed that that that worked better.
[31:26] So, um just just a little uh tip for
[31:29] folks.
[31:30] &gt;&gt; Super helpful. Yeah. [laughter]
[31:32] &gt;&gt; For some reason, people have an allergic
[31:33] reaction to the word audit. Um
[31:35] &gt;&gt; well, I mean, they think of they think
[31:36] of like a tax audit.
[31:38] &gt;&gt; Yeah. Yeah. Fair enough. The AI audit
[31:42] doesn't have the same ring to it for
[31:43] sure. [snorts]
[31:47] &gt;&gt; Yeah. Cool. All right.
[31:48] &gt;&gt; Let's keep going. Again, deterministic
[31:49] software versus an agent versus a human
[31:51] in control. I'm not going to beat a dead
[31:52] horse. You got to prioritize the high
[31:54] volume workflows where the improvement
[31:56] is large enough to matter. That's your
[31:57] job as an FD is to figure that out
[31:59] firsthand.
[32:01] &gt;&gt; Um, eval turn non-determinism into
[32:04] evidence. You got to make sure that you
[32:06] have the right data, the required steps,
[32:07] it matches the expert, um, and it's safe
[32:10] to act on and you got to make this kind
[32:11] of matrix and wherever you feel like
[32:14] it's not safe to act on, you know, you
[32:15] route it to a human and you create an
[32:18] evaluation report, right? So you have
[32:21] 50 runs and 41 of them passed. Of the
[32:23] nine that didn't, let's investigate why.
[32:25] You know, five of them had missing data,
[32:27] four of them had the wrong record
[32:28] pulled. And then you use that to improve
[32:30] the system. Greg, you touched on this
[32:32] earlier, like how do you set up evals?
[32:33] This is sort of the the framework that I
[32:35] would use.
[32:37] &gt;&gt; This is cool. By the way,
[32:40] &gt;&gt; yeah, just it it helps to just have like
[32:42] a a decision tree, a matrix when you're
[32:44] thinking about things. again like
[32:45] because everything is so new you could
[32:47] go a million different ways but you know
[32:49] I'm sure there's other ways to do this
[32:51] but this is ours and this is just how we
[32:52] kind of think about things at a high
[32:53] level it depends on a case by case basis
[32:56] for sure
[32:58] so how do you make it deploy and work
[32:59] inside the business this is again phase
[33:00] three the first one is the audit the
[33:02] second one was eval third is deployment
[33:04] one we really preach about like
[33:05] integrating with what already exists um
[33:08] I think a lot of AI folks are forcing
[33:11] migrations to like new software and And
[33:14] the reality is, and this is a tip that I
[33:15] give to all my FDE, you have an edge if
[33:17] you're able to build on top of their
[33:18] systems. So, you know, one of our
[33:20] clients, for example, said that they
[33:21] spent, you know, a couple of years, a
[33:24] couple million dollars moving to
[33:25] Netswuite, which is an ERP software. And
[33:28] if your AI solution is like, hey, we
[33:30] have to make you move off of Netswuite,
[33:32] they're going to tell you to get lost.
[33:34] But instead if you're saying which is
[33:35] what we do build on top of Netswuite
[33:38] make it much better and integrate that
[33:39] Netswuite with your Salesforce with your
[33:42] SAP with your Concur Expensify Gong uh
[33:45] you know every other piece of software
[33:47] workday that is a much more powerful
[33:50] system and that is where all the value
[33:52] lies
[33:54] than if you can test it in a controlled
[33:56] environment and really scale up from you
[33:59] know deployment to shadow mode to
[34:03] increasing autonomy. to then being
[34:04] deployed in production. That is going to
[34:06] be your edge as well where you're not
[34:08] forcing a massive shift. You're kind of
[34:10] walking them through that journey. And
[34:11] to our point earlier of why you meet
[34:13] them in person, it's because it's a lot
[34:15] easier to kind of guide them along that
[34:17] journey if you've met them face to face
[34:18] versus if you're just a guy behind a
[34:20] computer screen saying, "Hey, now we're
[34:22] going to flip a switch and AI is going
[34:23] to run your business." That's a a much
[34:25] different much more uh polarizing
[34:28] approach.
[34:28] &gt;&gt; I mean, it makes sense, right? like
[34:30] you're you did the audit and then if
[34:33] you're going to pitch to them, hey,
[34:34] you've been working with this software
[34:37] stack for the last 20 years. All of a
[34:39] sudden, go switch to this thing and it's
[34:41] going to cost you a bunch of money and
[34:43] there's just like so many unknowns. Like
[34:46] that is a tough pitch to sell. You know
[34:50] what I mean? And like you want to if
[34:52] you're pitching anything, you want to
[34:54] pitch something that feels like you're
[34:56] fishing with dynamite. So, it's like how
[34:58] can you, you know, how can you fish with
[35:01] dynamite? You just say like, "Hey,
[35:03] you're you have this system and this
[35:06] stack. You're it's it's worked for you.
[35:10] Um, I'm going to make it better and it's
[35:15] going to help you all be more efficient.
[35:18] It's it's going to help you uh reach
[35:21] customers faster. It's going to drive
[35:22] value for customers. It could increase
[35:25] revenue." Like when you start saying
[35:26] things like that, it's like, okay,
[35:28] no-brainer, no brainer, no brainer.
[35:30] Also, you have to keep in mind that
[35:31] you're pitching to people at a company.
[35:34] And people at a company, I'll say the
[35:36] thing that people don't say, which is
[35:39] they don't want to get fired,
[35:41] right? Like they want to get promoted
[35:43] actually. So your job is to help them
[35:46] get promoted. How do you help them get
[35:49] promoted is probably not by moving from
[35:51] one ERP to another ERP that may be
[35:54] marginally better. You help them get
[35:56] promoted by driving value
[36:00] cost effectively. If you can drive value
[36:03] cost effectively, everyone's high five
[36:06] high-fiving, right? Cuz when performance
[36:08] reviews comes around, you know, you the
[36:11] the employee, the executive can point to
[36:14] I worked on this project. Yes, I worked
[36:16] with an outside agency like LCA or Veric
[36:19] Agents or individual FDE
[36:23] um freelancer. Um but as long as you
[36:28] help them do that, that's what's going
[36:30] to help them get promoted.
[36:33] &gt;&gt; Yeah, totally. And and and just like to
[36:35] again like double down on that, they
[36:38] view you as a risk, right? They can just
[36:40] sit by and let things stay the same and
[36:43] status quo. They'll be fine. But if they
[36:45] instead bring in an FTE who's going to
[36:48] change stuff up and maybe it fails, like
[36:50] they're worried if this fails, it's a
[36:52] terrible look on me. Forget like
[36:54] migrating to another ERP. Even just you
[36:56] being involved at all is a risk to them.
[37:00] So you have to de-risk this as much as
[37:02] possible for them if you really want to
[37:03] sell yourself into a company. And what I
[37:06] strongly recommend is like do the audit
[37:09] for free. like get your foot in the
[37:11] door, prove value there, come up with a
[37:13] plan, and then only get paid when you
[37:16] really prove measurable value. That is
[37:19] what I strongly because that derisks the
[37:21] whole thing. Your first few customers,
[37:23] if you're really starting this out, will
[37:25] teach you so much. They are genuinely
[37:27] worth more to you than you are to them.
[37:29] But after you have one, two, three of
[37:31] those, then you can start charging for
[37:33] this because you're going to be leagues
[37:36] and miles ahead of everyone else in the
[37:37] space. I promise you it's still so
[37:39] early. I know this from our company as
[37:42] well. There is so much demand for people
[37:45] who really know how to do this. And
[37:48] quite frankly, there aren't that many
[37:49] people who know how to do this. Get
[37:51] started, get your feet wet, um, and
[37:53] really prove that you know what you're
[37:55] doing. And that's d-risking the whole
[37:56] thing for them.
[37:58] &gt;&gt; Totally. And it's just going to give you
[38:00] the confidence too, you know.
[38:01] &gt;&gt; Yeah.
[38:02] &gt;&gt; Right. Which is important.
[38:04] &gt;&gt; Yeah. And you'll know what matters to
[38:05] them when you're selling. like you can
[38:06] touch on different aspects that speak
[38:08] better to this person in the function.
[38:10] Um it's all really valuable. If I had to
[38:13] put one page cemented burned in
[38:15] everyone's brain, it's this one which is
[38:18] you go from audit to eval to deployment.
[38:21] There's some steps in the way you build,
[38:23] you observe and you improve and the loop
[38:25] runs again because once you improve one
[38:28] system, the next one becomes extremely
[38:29] clear. There's always interconnected
[38:32] bottlenecks where one workflow is
[38:34] impacted by something upstream and it
[38:37] frees up something downstream. And this
[38:39] is why AI is so pervasive in an
[38:41] organization. It's because once you have
[38:43] it in one place, you're going to need it
[38:45] everywhere else so that you're not just,
[38:47] you know, 10xing one workflow, 10xing
[38:50] another, you're 100xing the entire
[38:52] business as a whole. Um, and that's your
[38:55] job as an FTE is to go from audit to
[38:57] eval to deployment over and over again.
[39:00] And the next stage that I'm going to
[39:01] show is the 30-day plan of how you can
[39:04] get there from zero to one. If if I was
[39:06] starting from scratch, how would I go
[39:08] about it?
[39:09] &gt;&gt; And you did this, by the way. You you
[39:11] started from scratch, right? I didn't
[39:12] know this, but you were you're an
[39:14] engineer at Meta, right? And then you
[39:16] sort of learned how to do this. So,
[39:18] you're speaking from experience.
[39:20] &gt;&gt; Yeah, absolutely. I was an engineer at
[39:22] Meta for um uh a few years working on a
[39:25] different a couple different products,
[39:27] but I was never a consultant. I never
[39:29] really understood what mattered to
[39:31] businesses as deeply as I do now. And we
[39:32] got started again just by by doing it.
[39:35] Um and we we we had this thesis that
[39:38] like AI needs to be applied and it
[39:39] allows us to get ahead of the curve. Um
[39:42] but you never learn by,
[39:45] you know, reading and and you only learn
[39:48] by doing it. So the goal from this is is
[39:51] to do like if I could condense what I
[39:53] did over a year and really had the
[39:55] biggest learnings, the biggest wins in
[39:57] just 30 days. This is what I would do.
[40:01] So the first step is build an agent that
[40:03] can complete a real loop, right? Build
[40:06] an agent that's actually useful as a
[40:08] workflow. So like ask Chad PT what is
[40:10] one real enterprise workflow in a
[40:15] function of the back office, right? It
[40:16] could be finance, it could be HR, it
[40:19] could be procurement, logistics, it
[40:20] could even be for it, it could be sales,
[40:22] anything. Get the workflow in as
[40:24] granular of a detail as possible and
[40:27] build an agent for it. Um, even today,
[40:30] it's very hard to build agents, right?
[40:33] We think that it's a solved science.
[40:34] It's not. There's a thousand different
[40:36] ways to do this. Everyone has different
[40:38] definitions of an agent. My definition
[40:39] is this. If I give you a task, can you
[40:44] solve it in as much
[40:46] detail and as high enough accuracy as
[40:48] possible. It's different than me
[40:51] prompting Claude to go do it. It's far
[40:53] more in the background and it has much
[40:55] more of a repetitive motion where I'm
[40:58] not relying on somebody prompting
[40:59] perfectly to make it happen. I can
[41:01] prompt like an idiot and it will still
[41:03] happen. That's my kind of requirement
[41:05] for you when you're solving for this.
[41:07] There's a bunch of different, you know,
[41:08] aspects to this, but if you have 7 days
[41:10] to work on this, you'll be able to pick
[41:12] it up. agent looping, then tool usage,
[41:15] then guard rails, then context and
[41:17] memory, then the audit trail, which is
[41:19] incredibly important. I want to hammer
[41:20] down here a little bit. If you can't
[41:22] show the client what the agent is doing,
[41:25] they will never trust you. There's a big
[41:27] fear in AI agents today that okay, it's
[41:30] going to go off and do something. It's
[41:31] horrible. There's a lot of
[41:32] fear-mongering as well. I won't say from
[41:33] who, but everyone knows who I'm talking
[41:34] about. [snorts] Um, you need to show
[41:37] that the agent traces are logged
[41:40] everything. And this is a software
[41:41] engineering problem. So, if you can do
[41:42] that, you're a step ahead. And again,
[41:44] there's a full day for each of these
[41:45] things. Um, to clarify, if you're, you
[41:49] know, working 12 hours a day, I don't
[41:52] expect you to be able to pick all this
[41:53] stuff up perfectly on each every single
[41:54] day, but this is what I mean by like a
[41:56] 30-day plan. You can space it out as you
[41:58] need. It's not like you have to get it
[41:59] done in 30 days. Then a real workflow,
[42:02] then a checkpoint. The checkpoint, the
[42:03] last day is you have a working agent
[42:05] with tools, guardrails, deliberate
[42:07] memory, and a full audit trail for one
[42:09] task. You might not even understand the
[42:10] task the best, but this is just to get
[42:12] you well-versed in building agents.
[42:16] &gt;&gt; Fair.
[42:18] &gt;&gt; The second week is turning that demo
[42:20] into a system that can recover. Again,
[42:22] very heavily on the engineering side.
[42:24] So, a defined JSON schema not free form
[42:26] text. You're validating schema. You have
[42:29] failure modes and again I want to call
[42:32] it failure modes. exception handling and
[42:35] we also see in 13th days failure
[42:36] handling is also extremely extremely
[42:40] important. This is where going in deep
[42:42] into a client matters because if you
[42:45] understand hey when something goes wrong
[42:47] how does it go wrong and let me build
[42:49] the agent around that is extremely
[42:53] important. It's far more effective than
[42:55] you're building an agent that solves for
[42:56] just the happy path. It's called the
[42:58] happy path. If you're building for the
[43:00] unhappy paths, the 1,500 different ways
[43:02] it can go wrong, your agent is worth a
[43:05] million times more. The way I say it is
[43:07] this. There's only one way that
[43:08] something can go right, but there's a
[43:11] thousand different ways something can go
[43:12] wrong. So, if you're only building for
[43:14] the way it goes right, you're worth
[43:16] nothing. If you're solving for all the
[43:18] exceptions, that's where you are worth
[43:20] something as an agent.
[43:22] That's week two.
[43:24] Then week three is where you start to
[43:26] make it measurable and economically
[43:28] viable. Right? So you'll have the retry
[43:31] logic. Yes, this is more engineering.
[43:32] You'll have the golden data set for
[43:34] evals. You'll make sure that it improves
[43:35] over time. But you'll also start
[43:38] understanding, okay, this is what we
[43:39] talked about earlier, Greg. Looking at
[43:41] cheaper models for subtasks, looking at,
[43:44] you know, less soda, less Frontier
[43:46] models. Can we get this job done with a
[43:48] Gemini Flash or can we get it the job
[43:51] done with a a Muse Spark or probably not
[43:54] a Llama 4, but you know, there's other
[43:55] models that can that can be a good fit
[43:57] there. Um, this is where you start to do
[43:59] more or more of this test, which is we
[44:02] have an agent now. Now, let's try to
[44:04] optimize it. Let's try to measure, okay,
[44:05] how much is it really moving the needle?
[44:06] If I deploy this in production, how much
[44:08] time am I saving? How much risk am I
[44:10] mitigating? How much revenue uplift do I
[44:13] have? There's only three buckets of me
[44:14] measurement that matter for a business.
[44:16] It's those three, revenue uplift, risk
[44:18] mitigation, and cost savings. So, you
[44:20] need to measure your agent across all
[44:22] three of those buckets. And at this
[44:24] checkpoint, you have, you know, an
[44:25] evaluated agent with known failure
[44:26] modes, measured costs, and a golden data
[44:28] set. And the final week is defend the
[44:32] system like an FTE, which is all of the
[44:35] business around it. It's the pain
[44:37] points, it's why AI belongs, it's the
[44:40] architecture behind it, it's the
[44:41] iterations. is you know when you first
[44:43] built the agent it got this wrong but
[44:45] then it improved over time accuracy went
[44:47] from you know 70% to 95%. and the
[44:51] economics around it. So how much time
[44:53] did you save the error reduce again risk
[44:55] revenue costs? We talked about this and
[44:57] you rehearsse this as an engineer. So
[44:59] what was the architecture? What were the
[45:00] decisions that you made? And then you
[45:02] also rehears this as a VP. Like what was
[45:04] the problem that you solved? What was
[45:05] the outcome? What was the evidence? What
[45:06] was the risk? And this week is where
[45:09] you're going to know, you know, was the
[45:12] system that you built worth the salt?
[45:14] Was it worth the investment? How much
[45:17] could you charge for this when you build
[45:19] it for a customer? That's what this week
[45:21] is for. And I strongly recommend that
[45:23] during this week, you pitch your agent
[45:26] to businesses because they will tell you
[45:29] like, you know, did I get you you'll
[45:32] pitch them, did I get this right? Did I
[45:33] get the economics right? Am I thinking
[45:34] about this the right way? And they'll
[45:35] tell you point blank, no. Or I want it
[45:38] built in this way. and you'll start to
[45:40] see like okay now for my next FD
[45:43] engagement starting out with an audit
[45:45] when you're actually embedded with a
[45:46] customer you'll learn much more about
[45:48] that obviously this is 30 days is you're
[45:50] not embedded with a customer because you
[45:52] can't because you have to become an FTE
[45:53] first that's when you can finally start
[45:55] to pitch yourself and be involved in a
[45:57] company
[45:59] so if I had to zoom out this would be
[46:02] the 30 days it's doing the job before
[46:04] you have the title so on day 30 you
[46:05] understand forward deploy engineering
[46:07] but you also have evidence that you can
[46:08] do it and if you pitch this to a
[46:09] company, they'll be much more likely to
[46:11] give you a shot. And that's my goal.
[46:15] &gt;&gt; Foss, [snorts] this is ex this is
[46:17] perfect. Like, this is exactly what I
[46:19] would recommend, too. What would be so
[46:22] cool is if
[46:24] is if you actually taught people how to
[46:27] do this, right? Um, and like spent 30
[46:31] days with people to actually do this.
[46:34] Um, maybe maybe we do it together. Just
[46:38] an idea. Uh if people are interested,
[46:41] I'll just include a link uh in the
[46:44] pinned comment on YouTube. Um I'm just
[46:47] curious if people
[46:49] people are interested in like cuz it
[46:51] might it might feel overwhelming for
[46:53] people to do this
[46:55] on their own. I mean, I still think you
[46:57] could do it on your own, by the way, but
[46:58] I wonder and and by the way, I'm not
[47:00] promising anything. I'm just curious,
[47:02] are people into
[47:04] into some sort of program for this?
[47:08] They don't teach you this at school.
[47:10] &gt;&gt; They don't. They should. Uh I'm sure
[47:12] we'll have university courses on FTE
[47:14] soon. But yeah, people want to
[47:18] [laughter] like it just takes so long. I
[47:20] remember I was in computer science
[47:22] school in 2008.
[47:24] &gt;&gt; No, 2009
[47:27] um and at university. And I remember the
[47:31] app store had just come out.
[47:34] It was so clear in 2009 that mobile apps
[47:38] was the next wave. Just like it's so
[47:41] clear right now that AI agents and AI is
[47:44] the is the is not even the next wave is
[47:45] the wave. And I just remember the
[47:49] textbooks at the time and I went to a
[47:51] top university
[47:53] textbooks at the time and the course
[47:54] material was like you know building old
[47:59] school software and I remember going to
[48:01] a teacher a professor well-known guy and
[48:04] saying why can't we why can't you teach
[48:06] us how to build an Objective C and to
[48:10] build for the app store and he was just
[48:13] like yeah it's just not in the textbook.
[48:15] just not in the textbook. And that's
[48:18] when I like I was like, I'm going to
[48:20] drop out of this. I [laughter] I'm
[48:22] dropping out because like I don't want
[48:24] to learn yesterday's stuff. I want to
[48:27] learn tomorrow's stuff. Now, there's
[48:30] always the argument to be made that you
[48:32] need foundational work. And so, like I
[48:36] learned a lot in university around like
[48:38] foundational stuff around maths and
[48:40] physics and stuff like that. And I
[48:42] actually think that that stuff was
[48:43] really helpful just in like learning how
[48:45] to think, but like the actual tactical
[48:48] stuff did not really learn.
[48:52] &gt;&gt; Yeah, I I I do, you know, I want to say
[48:56] like this time is different like just
[48:58] because it's so powerful like AI is so
[49:01] like you said it's the wave that I'm
[49:03] hopeful that universities are going to
[49:05] pick up sooner than later, but for some
[49:07] reason I feel like you're right. I don't
[49:08] think it's going to happen anytime soon.
[49:10] Yeah.
[49:12] Well,
[49:13] &gt;&gt; there you have it, folks.
[49:16] What what FDEES are.
[49:19] Um how to become one. Uh a 30-day plan.
[49:25] Uh Vos, anything else you want to share?
[49:29] &gt;&gt; I think, you know, like you said, you
[49:31] might not find this in university, but
[49:34] you're absolutely going to find it on
[49:36] YouTube. like Greg is teaching
[49:38] everything that you need to know and
[49:39] Twitter as well. Those two sources are
[49:42] going to be where everything is
[49:43] released. I mean, even Mark Zuckerberg
[49:45] had to come back to to Twitter to
[49:47] announce, you know, the latest model for
[49:48] Meta. That's where everything's
[49:50] happening. Study the game there. Um, and
[49:53] you've got a great coach right in front
[49:54] of you with Greg. So hopefully that, you
[49:57] know, people are really taking advantage
[49:58] of this time where there's a significant
[50:00] alpha from going out, learning, doing it
[50:03] yourself, being scrappy with it versus
[50:06] waiting for a university to come by and
[50:08] and and teach you this cuz that's not
[50:09] going to happen anytime soon.
[50:11] &gt;&gt; And it's free, right? You can listen to
[50:13] this and apply. It's free. So it's just
[50:15] like why not, right? Yeah.
[50:16] &gt;&gt; Um, Vos, thank you for being generous
[50:19] with your with your, as we say on the
[50:21] channel, the sauce and the tactics and
[50:24] just like breaking this down so clearly.
[50:27] Um, I've been following you for a couple
[50:29] years now almost. And uh, you're a must
[50:33] follow. I'll include links on where you
[50:35] can follow Voss um, from Veric Agents in
[50:39] the show notes, in the description. you
[50:41] know, please comment what you what you
[50:43] thought of this episode because I
[50:46] enjoyed myself with Voss. I'd like to
[50:48] have him back on the podcast again.
[50:49] Hopefully, he he's down to come back on.
[50:52] Uh, but please let us know. I read every
[50:54] single comment. Uh, you want to like and
[50:57] subscribe for more of this in your feed?
[50:59] Voss, any last words for for the people?
[51:02] &gt;&gt; Greg, you're a legend. Thank you for
[51:03] having me on. To the people, I believe
[51:05] in you. I really believe this is a
[51:06] fundamental shift in in how work is
[51:08] done. And you are if you're if you're
[51:11] listening to Greg and you're and you're
[51:12] you're on this p you're watching this,
[51:13] you're already a step ahead. I'll be
[51:15] reading every single comment, too. If
[51:16] any questions you have for me, let me
[51:17] know. But I would say like go out and
[51:20] get it. Go out and get the job done.
[51:22] Make make the most of of your ability to
[51:25] understand AI. And it's still so early,
[51:27] so get ahead of it while you can. Greg,
[51:28] thank you for having me on, man. You're
[51:29] a legend.
[51:30] &gt;&gt; Amen. All right. Catch you next time.
[51:32] Kiss.
