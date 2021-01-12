# How it is being a Data Scientist: One year into the job


What is it like working as a Data Scientist? Generally speaking, I do not know. But I can share my first hand experience having just passed the one year mark into the job. Of course, it was different to what I expected. I have coded far less super auto-magical machines, and I got caught up in far too much unplanned work. I learnt about the importance of contextual factors and team work. First things first, let me start with how I have gotten into this.

<!--more-->

Help to **improve this post** on [GitHub](https://github.com/siegstedt/machinemind/blob/main/content/posts/being-a-data-scientist.md). Thank you for your contribution.

## How it started

In 2015, I started off as a reporting dude at a boutique agency and later on made my way to the ranks of an analytics guy at another job. I really enjoyed insightful analytics and I was thrilled by the idea of having an impact on how people would make sense of complex matter.

More than a computer nerd, I’m rather a business guy trained at Econometrics, Marketing Research and Innovation Management. Lured by the promises of how data may change the way businesses made money in the future, I engaged into the field of Data Science. I learned coding algorithms and the backbones of Data Engineering to get leveled up in Machine Learning and other miraculous data witch craft. I’m curious by nature, so it was great fun.

One year ago, I got hired by a big company with even bigger data. Among other data, the company handled transaction data on the pharmaceutical market at extensive volume. What would you want to do with such data? Well, you can look into trends, cycles, exports, imports, launches, networks, consumption behavior, data gaps, quality issues, etc. Perfect, I thought to myself, I can crack that. So I started.

## Lesson #1: Context and exploration is king

The world is a messy place. And we’re endlessly trying to make sense of it. We write wikis, documentations, and often overwrite past knowledge. We compose process flows and algorithms, and often redesign some legacy system. We collect and process data, and often clean, transform, or overthrow the sample.

Now, as you start into your new job, all kinds of documents, systems and data sets will be introduced to you. This is a very vital phase for the upcoming days and weeks. Absorb all information, be curious, ask questions and take a ton of notes.

Very probable that you may need to go through catalogs of data set description, fish in the deep seas of database systems, and decipher some legacy process flow and code. This is the point where you can shine with your skills in data exploration.

This basis work will allow for a correct interpretation of the result and a correct composition of a new ML work flow that you may have been tasked with.

Again, this is a very vital exercise. In fact, it is an exercise that would repeat itself over and over again with any new project that you’d be introduced to.

## Lesson #2: Infrastructure eats ML code for breakfast

“Let’s just introduce Machine Learning and the future will be perfect!”, the manager said. “Hooray!”, the company followed. “Hold on …”, I wondered.

Accoording to Gartner’s Data Science Team Survey (2018), over 60% of Machine Learning models never actually went to production. With this fairly new technology, gaps between Dev and Ops may hinder a swift deployment of your ML master work.

To have the right infrastructure at hand sounds as obvious as it may be hard to realize, if it is not in place. Too often at the beginning of a project and in mostly all cases driven by the business guys, we underestimate the technical dept in ML systems.

ML code may be a driver of the products value proposition. Yet, it actually is a tiny puzzle piece in a much larger and more complex platform of complementary elements. See this propular article on the technical dept in ML: https://papers.nips.cc/paper/5656-hidden-technical-debt-in-machine-learning-systems.pdf

So what you may want to start out with is a good understanding of your pipelines (batch size / stream, quality, format, anything). And what you may want to avoid is that your ML flow becomes a bottleneck in the system.

Therefore, optimize your pipeline, for instance by downsizing data samples, running parallel processes, setting up virtual environments, etc. Make anything work to support the rule of flow: increase # of shipped products per time units in your bottleneck. And, as usual, make sure to allow for feedback to your flow and reduce the amount of unplanned work if adhoc changes are required.

You know that you are on a good path if your code iterate multiple versions of prototypes on your production system every day.

## Lesson #3: Do story telling with data

Now that the results are ready, you send out invitations to people with impressive job titles and get ready for your presentation. And here the trouble is on: how to design an appropriate representation of your results?

To be honest with you, the first presentation of results I held was a total mess. I have had far too many visualizations prepared. I was jumping back and forth between the graphs and data tables. On top of it, I was pacing too fast assuming that the audience may follow me easily. Well, not so much. After 30 Minutes, the room was full of confusion and we needed to start over again.

Since that meeting, I searched for some techniques to help me get my messages communicated in an effective as well as efficient way.

At first, I split my results in a report (usual framework of academical writing), input and output data as well as my code, and the representation of my result that support the story of the presentation. I only present the latter and send out the report and data after the meeting together with my meeting minutes.

The approach of the Minto pyramid (or SCQA) helped me to structure my talk better and carefully guide the attention and cognitive processes of the audience. By today, it became a routine to frame messages, focus on the crucial points, allow people to zone out a bit, and take breaks before getting to the most important matter.

To help your story line even more, you may want to go for one anchor visualization that can carry a really heavy load of information. If you possibly can, design a physical replication of your data so that people can actually touch, feel and play with your results.

For instance, you can use a big canvas and cut out some paper or you can play with some Lego. It may sound weird to go back from digital to analog. But, a tangible experience is just easier to process then a pure virtual or theoretical idea. Your audience will be grateful.

## Lesson #4: It is a team sport

If your company is truly data driven, then data naturally flows through all departments directly catering to the #1 goal of the company: to make more money.

It flows from the market research and new product development over to production and delivery to the customer. Taking data privacy and security into the equation, the flow combines Mkt + Dev + Ops + Sec (which is a little more extensive than the currently popular DevOps view on things).

Being a data scientist makes you standing at the center of that flow and being a crucial point of contact and interest. Better be aware of all the nice attention. And, better ramp up your communication and persuasion skills – not least for turning down some less productive requests.

In order to be a true team player, the role requires you to understand how all the different departments work together. Plus, you should know how these are organized and what drives their successes. During some coffee break or at an introduction meeting, ask your colleagues what they do – like what exactly they produce – and what a good or a bad days looks and feels like for them.

## Next up

So far, so good. What is next for me? Besides some career aspirations, I wanted to start a blog to digest my experience thoroughly and contribute to the community of young talents that want to make a difference. I thought about titles, themes and anchor points. Here it is. 

machinemind.io is for those who want to inspire others to innovative and create bold solution statements. It is for the ones who regard data and algorithms as the core machinery of their tool kits. And is for those who make data products actually work to capture the full promise of analytical value delivery.
