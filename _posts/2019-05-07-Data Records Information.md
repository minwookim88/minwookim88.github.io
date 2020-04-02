---
layout: posts
title:  "Data Records Information"
date:   2019-05-07 20:00:00 -0700
categories:
  - data_science
  - topsy-turvy
tags:
  - data
  - information
  - truth
  - observation
---

In order to understand the nature of data, we first need to understand [the concept of information and its relation with data]({% post_url 2019-04-03-Information Abstracts Truth %}). In short, information is subjective description that attempts to summarize contextual truth given the limited description capacity. That is, information is truth conditional upon context, if we are allowed to use probabilistic terminology. In a general sense, information is (mostly) intangible, so it inherits two major problems: One, it is easily likely to deviate from the original meaning as it passes down to others because people tend to reinterpret the meaning (either intentionally or unintentionally) as they deliver the information; Two, there is no viable way to propagate information directly on a large scale - you can never deliver your original knowledge directly to millions of people in your lifetime because of physical limitation in time and space.

<figure>
  <img src="/assets/images/3layer_pyramid.png">
  <figcaption>Truth, Information, and Data</figcaption>
</figure>

Data, on the other hand, is recorded information in a written form using numbers and letters. The key characteristics that differentiates data from information is sustainability. Once you record it, data exists and lasts forever unless otherwise destroyed. So, unlike information, data is more robust to deformation and is most suitable for massive propagation. However, this doesn't mean that data is always reliable and objective. It's not, even though they are represented as numbers and letters which are seemingly objective.

<figure>
  <img src="/assets/images/data_table2.png">
  <figcaption>Data Table</figcaption>
</figure>

Because data is recorded information, it requires someone (say, source of the data) who first observes evidence of truth and translates it into information through abstraction. Then, the source records the resulting abstracted information into formatted data.
<!---That means, data goes through additional step of abstraction.--->
The following example explains the detailed process of data recording, which will helpful in understanding why data is also subjective and where the subjectivity comes from.

<hr style="height:3px;border:none;color:#808080;background-color:#808080;" />

Suppose a researcher <font color="blue"><b>A</b></font> wants to study the relationship between length of middle finger and stature of people. In order to expedite the study, he decides to use finger data collected by someone else instead of collecting himself. Then, he comes to know that one of his colleagues, researcher <font color="red"><b>B</b></font>, has recently done a research using the same kind of data he collected himself. <font color="blue"><b>A</b></font> asks <font color="red"><b>B</b></font> for the data access, and he finally gets the data. <font color="blue"><b>A</b></font> is so excited by the fact that he can immediately start the research without having to collect data on his own. He moves on to the next step immediately and finishes the work in no time.

Few days later, <font color="blue"><b>A</b></font> decides to treat <font color="red"><b>B</b></font> in order to thank for providing dataset because he knows how it is painful to collect data. They gather in a restaurant, and start talking about their recent research while having dinner. Then, <font color="red"><b>B</b></font> begins to explain his long, heroic journey about collecting the dataset he has provided.

(<font color="red"><b>B</b></font>): 
<!---I first started to collect data myself. I first decided to fly--->
"I first flew to Switzerland. There, I started wandering the streets to recruit some European participants. Original plan was to travel several countries in Europe and collect data myself and head back to home, though things didn't go as planned."
  
(<font color="blue"><b>A</b></font>): "Wait, What? Did you just study European people?"

(<font color="red"><b>B</b></font>): "Yes. I didn't really take into account either Asian or African people or anyone else, because I didn't want to introduce unnecessary cultural bias to my study. So, that's not in there. Anyway, I started picking random people on the streets and asked them for the participation to study. For those who accepted, I spent few seconds to measure the index finger length, but damn, I was..."

(<font color="blue"><b>A</b></font>): "Wait, did you measure index finger length? Not middle finger?"

(<font color="red"><b>B</b></font>): "Yeah, why? Just because I thought that index finger would be the best representative out of 5 fingers that represents some sort of average finger length of hand. Is there something wrong?... Anyway, where was I? Hmm.. I got it. So, I was just about to measure the very first participant's finger, but holy crap, I wasn't sure where finger actually starts! Is it the small knuckle bone that connects finger and back of hand? Or is it the palm-side fingerprint that bends and connects between finger and palm? I hadn't really thought about it seriously, my bad, so I had to pay for it. I was so embarrassed that I couldn’t make a decision right away. Sometimes I measured from the bone, sometimes I measured from the print... My mind was full of the thoughts that I screwed up my own research; I just couldn't get away with it. After wasting precious hours, I finally managed to get a grip, and decided to stick with the knuckle bone."

<figure>
  <img src="/assets/images/hand.png">
  <figcaption>How will you measure?</figcaption>
</figure>

(<font color="blue"><b>A</b></font>): "Okay, that's new to me. So what did you do with those early data?"

(<font color="red"><b>B</b></font>): "They are also included in the dataset as well. Oh, I forgot to mention it though. I had to tell you that you better remove the first 38 rows, but you looked in such a hurry that I forgot to tell you."

(<font color="blue"><b>A</b></font>): "What? I..."

(<font color="red"><b>B</b></font>): "Sorry my friend. But you know, it's okay. Look, there is no perfect data anywhere. Anyway, this is not the end of the story. I wanted to cover as much diverse race as possible, so I was planning to travel 10 different countries myself. Unfortunately, I got a serious flu on the second day, so I couldn't continue the job as planned. So I had to ask to some of my friends in those countries and asked them to collect data on behalf of me - not for free, of course. I am not a jerk. I am telling you that the dataset is quite an expensive one. But don't worry about it, I gave it to you for free, because you had once helped me big time. So, let's call it even."

(<font color="blue"><b>A</b></font>): "So, did you make sure your friends stick with knuckle bone when measuring the finger length?"

(<font color="red"><b>B</b></font>): "Uh...um... that's good point... I think so? You know, honestly, I don't know... I was damn sick that I wasn't in the status of giving detailed instructions."

<hr style="height:3px;border:none;color:#808080;background-color:#808080;" />

Apparently, there was a big gap between what <font color="blue"><b>A</b></font> expected from the data and what <font color="blue"><b>B</b></font> actually collected. When (<font color="red"><b>B</b></font>) was collecting data, he first observed the actual finger lengths (<b>evidence of truth</b>) of some of European people. However, this is not identical to the truth (which he might have pursued if it is ever possible) about actual finger lengths of all European people, because he only measured a portion of people. Also, when he was transforming his observation into <b>information</b>, he arbitrarily abstracted his observation by only caring about index finger length. No one can guarantee whether index finger is indeed the best representative, so it is this abstraction that introduced subjectivity to his dataset. It would have been much better if he could have somehow measured all finger lengths of all European people, but as is discussed [here]({% post_url 2019-04-03-Information Abstracts Truth %}), it is impossible due to physical limitations.

After he observed and formed his own version of information, he recorded his information as a form of <b>data</b> in order to preserve information. The way he recorded, however, was somewhat inconsistent. Sometimes he used knucklebone as starting point, and sometimes he used fingerprint. His mental information of "this long index finger" is inconsistently translated and recorded due to the lack of firm standard. Furthermore, although it is not explicitly stated in this example, he still could not been able to record correct information even with consistent standard, due to what is called <b>measurement error</b>. Whatever measurement device he might have used, there is inherent limitation that we can never read guage perfectly with naked eyes. Even if he might have used some sort of automatic measurement device, the maximum resolution of the device and discretization trait introduced by binary-oriented system does not allow you to record perfect truth.

<figure>
  <img src="/assets/images/ruler.png">
  <figcaption>We cannot tell the exact length</figcaption>
</figure>

Now we understand why data is also subjective and thus is not always reliable. In this example, we can see that there are three layers of abstraction that contributed to subjectivity. First layer is the step where he abstracted, justified and identified the <b>sample</b> of observation with the ground truth. 
Second layer is the step where he formed his own mental model that abstracts and maps hand observation into index finger length. Final layer is the step where he attempted to quantitatively measure his intangible idea of "long" and "short" and convert the idea to some numbers through measurement device and, record them.

This suggests the reason why we need to be always cautious about dealing with data. Data is summarized record based on some individual's (or group of individaul's) own observation of portion of truth as per his/her own interesets and capability. Thus, we always need to be keen to understand the nature and source of subjectivity in data so that we do not misunderstand, overtrust, and overgeneralize the meaning behind it.