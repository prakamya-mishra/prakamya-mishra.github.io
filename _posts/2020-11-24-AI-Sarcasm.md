---
layout: post
comments: false
title: "AI & Sarcasm"
date: 2020-12-18 00:00:00
tags: review
---

> **Abstract:** In this post I comment on the capability of the present AI systems to comprehend sarcasm by investigating the present work. At the end I also reason out why the present state of AI is incapable for properly understanding sarcasm.   


<!--more-->

{: class="table-of-content"}
* TOC
{:toc}

## Introduction

Natural language processing, popularly known as NLP deals in making computers intelligent enough to meaningfully process human language. Some common applications are document topic classification and text summarization. Sentiment analysis is another application in which the goal is to extract a person’s opinion from a piece of text written by them. In recent times, social media has become pervasive in every walk of people’s life. About 4 petabytes of data is generated every day on Facebook. A little more insight into this figure would show that roughly 4 million likes are generated every minute and close to 350 million photos are uploaded onto Facebook daily. Also, close to 1.42 billion reddit comments are generated across Reddit every month. The sheer number of people involved and their collective activity leads to a vast amount of data being shared between them regarding a wide range of topics. A lot of this information can be of value to many different stakeholders. One example from the recent past is the US elections, wherein a particular political party could gauge people’s sentiment by analyzing online activity. This generation of large amounts of data in a short time becomes too much to handle manually. Hence, social media is the perfect platform to perform any kind of sentiment analysis using NLP.

The online Oxford dictionary defines sarcasm as “the use of irony to make or convey contempt”. Merriam-Webster defines it as “a sharp and often satirical or ironic utterance designed to cut or give pain”. Sarcasm is a form of figurative language whose utterance can alter its sentiment. It is used in daily life to make jokes or at times to criticize people, ideas, or events. 

Some examples of sarcasm are:
- Oh, how I love being ignored. #sarcasm.
- Absolutely love it when my lift is late #sarcasm
- Wow, that’s a huge discount, I am not buying anything!!

This ambiguous nature of sarcasm makes it difficult even for humans at times in deciding if the nature of the remark was sarcastic or not. Sarcastic sentences usually use words that can have different meanings based on the context in which it appears (polysemy), which can be misleading for machine learning models for detecting sarcasm. Given this uniquely confusing nature of sarcasm, it becomes really difficult for NLP based applications such as review summarization and dialogue systems to identify the user’s sentiment. Thus, it is important to have in place an AI model which is able to identify sarcasm in the reviews. 

Developing truly conversational speech agents that can understand all the unique intricacies of the human language - remains one of the most important pending NLP problems of this time. Humans regularly use sarcasm as a crucial part of the day-to-day conversation when venting, arguing, or maybe engaging in humorous banter with friends. For an agent to really be conversational, detection of sarcasm may be a must. 

Understanding sarcasm, which is usually a difficult task even for humans, maybe a challenging task for machines. Common approaches for sarcasm detection are supported by machine learning classifiers trained on simple lexical or dictionary-based features. To date, some research in sarcasm detection has been done on collections of tweets from Twitter, reviews on Amazon, and comments/replies on Reddit. Reddit is an online discussion platform, where the community members can post information regarding news, politics, hobbies, etc, and any other areas of interest. The areas of interest are categorized as subreddits (/news, /politics, etc).

## The present state of AI in sarcasm detection

The main aim of this sections is to describe different works that have already happened in the field of sarcasm detection and to also give an overview of the recent advances in natural language processing for sentiment analysis. I will first start by describing the previously done work chronologically to showcase different techniques that have already been used to tackle sarcasm detection problems.

![joshi-etal-2015-harnessing]({{ '/assets/Blog/Blog1/joshi-etal-2015-harnessing.png'| relative_url }})
{: style="width: 100%;" class="center"}
*Table. 1.  Features of our sarcasm detection system. [Joshi, et al., (2015)](https://www.aclweb.org/anthology/P15-2124.pdf)*


[Joshi, Aditya, Vinita Sharma, and Pushpak Bhattacharyya. (2015)](https://www.aclweb.org/anthology/P15-2124.pdf) presented a computational system that harnesses context incongruity as a basis for sarcasm detection. They used four kinds of features: (a) Lexical, (b) Pragmatic, (c) Implicit congruity, and (d) Explicit incongruity features. Their main contribution was to introduce inter-sentential incongruity for sarcasm detection, which expanded the context of a discussion forum post by including the previous post in the discussion thread.

[Rajadesingan, A., Zafarani, R., & Liu, H. (2015)](https://doi.org/10.1145/2684822.2685316) addressed sarcasm detection on Twitter by leveraging behavioral traits intrinsic to users expressing sarcasm. They identified such traits using the user’s past tweets. They employ theories from behavioral and psychological studies to construct a behavioral modeling framework tuned for detecting sarcasm. They also identified different sorts of sarcasm and demonstrated how these forms are manifested on Twitter. They introduced behavioral modeling as a replacement, effective approach for detecting sarcasm on Twitter.

![amir2016modelling]({{ '/assets/Blog/Blog1/amir2016modelling.png'| relative_url }})
{: style="width: 100%;" class="center"}
*Fig. 1.  Illustration of the CUE-CNN model for sarcasm detection. The model learns to represent and exploit embeddings of both content and users in social media. [Amir, Silvio, et al. (2016)](https://www.aclweb.org/anthology/K16-1017.pdf)*

[Amir, Silvio, et al. (2016)](https://www.aclweb.org/anthology/K16-1017.pdf) proposed a model to automatically learn and then exploit user embeddings (which captured contextual features of the speaker), to be used with lexical signals to recognize sarcasm. The user embeddings required only the text from the speaker's previous posts. Their model did not require extensive manual feature engineering.

![ghosh-etal-2017-role]({{ '/assets/Blog/Blog1/ghosh-etal-2017-role.png'| relative_url }})
{: style="width: 50%;" class="center"}
*Fig. 2.  Sentence-level Attention Network for Context and Reply. [Ghosh, D., Fabbri, A. R., & Muresan, S. (2017)](https://www.aclweb.org/anthology/W17-5523.pdf)*
{: style="width: 50%;" class="center"}

[Ghosh, D., Fabbri, A. R., & Muresan, S. (2017)](https://www.aclweb.org/anthology/W17-5523.pdf) mainly solved two specific problems: (1) can the conversation context be used for sarcasm detection? and (2) to realize what parts of the context were responsible for sarcasm. To deal with the primary issue, they investigate models with linguistically-motivated discrete features and several other sorts of recurrent networks (networks with sentence-level attention on context and reply) which will model both the context and therefore the sarcastic reply. To deal with the second issue, they presented an analysis of attention weights produced by the models attentively.

![ghosh-veale-2017-magnets]({{ '/assets/Blog/Blog1/ghosh-veale-2017-magnets.png'| relative_url }})
{: style="width: 100%;" class="center"}
*Fig. 3.   A Neural Architecture for Detecting Sarcasm in Contextualized Utterances. [Ghosh, Aniruddha, and Tony Veale. (2017)](https://www.aclweb.org/anthology/D17-1050.pdf)*

[Ghosh, Aniruddha, and Tony Veale. (2017)](https://www.aclweb.org/anthology/D17-1050.pdf) showed significant gains using neural architecture in sarcasm detection accuracy when knowledge of the speaker’s mood at the time of production could be inferred. They show that the mood exhibited by a speaker over tweets leading up to a new post is as useful a clue for sarcasm as the topical context of the post itself. They build a model by adding input features for the psychological profile of the author and the context of the tweet to those for the tweet itself.

[Prasad, Anukarsh G., et al. (2017)](https://ieeexplore.ieee.org/document/8169892) compare various classification algorithms such as Random Forest, Gradient Boosting, Decision Tree, Adaptive Boost, Logistic Regression, and Gaussian Naïve Bayes to detect sarcasm in tweets. The best classifier was paired with various pre-processing and filtering techniques using emoji and slang dictionary mapping to provide the best possible accuracy. Their main contribution was to use emoji and slang dictionaries for analyzing the true intentions/sentiments of the tweets.

![hazarika-etal-2018-cascade-1]({{ '/assets/Blog/Blog1/hazarika-etal-2018-cascade-1.png'| relative_url }})
{: style="width: 100%;" class="center"}
*Fig. 4.   The figure describes the process of user profiling. Stylometric and personality embeddings are generated and then fused in a multi-view setting using CCA to get the user embeddings. [Hazarika, Devamanyu, et al. (2018)](https://www.aclweb.org/anthology/C18-1156.pdf)*

![hazarika-etal-2018-cascade-2]({{ '/assets/Blog/Blog1/hazarika-etal-2018-cascade-2.png'| relative_url }})
{: style="width: 100%;" class="center"}
*Fig. 5.   Overall hybrid network of CASCADE. [Hazarika, Devamanyu, et al. (2018)](https://www.aclweb.org/anthology/C18-1156.pdf)*

[Hazarika, Devamanyu, et al. (2018)](https://www.aclweb.org/anthology/C18-1156.pdf) proposed CASCADE that utilizes a composite method of both content and context-based modeling for sarcasm detection in the online discussion forum Reddit. CASCADE uses user embeddings that encode the stylometric and character traits of the users. When used alongside content-based feature extractors like Convolutional Neural Networks (CNNs), they saw a big boost within the classification performance on an outsized Reddit corpus.

![pamungkas-patti-2018-nondicevosulserio]({{ '/assets/Blog/Blog1/pamungkas-patti-2018-nondicevosulserio.png'| relative_url }})
{: style="width: 100%;" class="center"}
*Table. 2.    Feature Selection on each System. [Pamungkas, Endang Wahyu, and Viviana Patti. (2020)](https://www.aclweb.org/anthology/S18-1106.pdf)*

[Pamungkas, Endang Wahyu, and Viviana Patti. (2020)](https://www.aclweb.org/anthology/S18-1106.pdf) proposed to use various stylistic characteristics and utilized different affective means to tackle these tasks. They concentrated on two main tasks, Task A: whether a tweet was sarcastic or not? and Task B: Classifying tweets into various kinds of sarcasm. They conducted experiments using a support vector machine classifier, with a radial basis function kernel. They used architectural features and affective based features. Architectural features consisted of lexical and syntactical features that characterize Twitter data.


## Why the present AI models are incapable of understanding sarcasm properly?

As mentioned above, sarcasm is complex in nature and usually it is implied and not explicit. That's why most of the present works use some kind of context to capture their implied meaning. Here is where the present AI models have reached a bottleneck because mostly all of them are focusing on local contextual features like immediate reply or comment. This narrows the vision of the present AI models. Most of the time the actual context required for detecting sarcasm in a sentence might come from recent events in the society or from some general knowledge, which might not be captured by focusing only on local immediate context.

To properly understand sarcasm, the AI models should first build a global context knowledge base. This type knowledge base can range from general information about different topics to recent events in the society, from information about the individuals involved to their inherent opinions. The problem with this is that not all of this information can be found easily and that's why this lack of information in return reduces the global context which in return reduces the ability of  present AI models to detect sarcasm. Context plays an important role for understanding sarcasm. The recent advances in natural language processing has led to introduction of new sophisticated language models. These language models have increased the ability of AI models to better understand the context by using self attention mechanisms. These language models can further increase the performance of the sarcasm detection task, but the problem with them is that they are huge in size (highly computational intensive). So at present it's impossible to increase the size of context while using these big language models, which also creates a bottleneck. Also, present attention mechanisms cannot capture contextual information properly without losing important information from longer context. These are just the problems that we face if we only use text for sarcasm detection, using higher dimensional information like images, speech and videos are beyond the scope of the present AI models. Use of these higher dimensional data leads to additional complexity of tone analysis, expression recognition, temporal change in facial features, etc. The future of sarcasm detection and modeling will depend on the ability of the AI models to capture a large quantity of high quality contextual information and better AI models and attention mechanisms that can capture long sequences of context without losing any important information.

---

Cited as:
```
@article{prakamya2020AIsarcasm,
  title   = "AI & Sarcasm"",
  author  = "Prakamya Mishra",
  journal = "prakamya-mishra.github.io/Blog",
  year    = "2020",
  url     = "https://prakamya-mishra.github.io/Blog/2020-11-24-AI-Sarcasm.html"
}
```

## References

[1] Joshi, Aditya, Vinita Sharma, and Pushpak Bhattacharyya ["Harnessing Context Incongruity for Sarcasm Detection"](https://www.aclweb.org/anthology/P15-2124.pdf) ACL-IJCNLP 2015.

[2] Rajadesingan, A., Zafarani, R., & Liu, H. (2015) ["Sarcasm Detection on Twitter: A Behavioral Modeling Approach"](https://doi.org/10.1145/2684822.2685316) WSDM 2015.

[3] Amir, Silvio, et al. (2016) ["Modelling Context with User Embeddings for Sarcasm Detection in Social Media"](https://www.aclweb.org/anthology/K16-1017.pdf) SIGNLL 2016.

[4] Ghosh, D., Fabbri, A. R., & Muresan, S. (2017) ["The Role of Conversation Context for Sarcasm Detection in Online Interactions"](https://www.aclweb.org/anthology/W17-5523.pdf) SIGNLL 2017.

[5] Ghosh, Aniruddha, and Tony Veale. (2017) ["Magnets for Sarcasm: Making Sarcasm Detection Timely, Contextual and Very Personal"](https://www.aclweb.org/anthology/D17-1050.pdf) SIGDAT 2017.

[6] Prasad, Anukarsh G., et al. (2017) ["Sentiment analysis for sarcasm detection on streaming short text data"](https://ieeexplore.ieee.org/document/8169892) ICKEA 2017.

[7] Hazarika, Devamanyu, et al. (2018) ["CASCADE: Contextual Sarcasm Detection in Online Discussion Forums"](https://www.aclweb.org/anthology/C18-1156.pdf) COLING 2018.

[8] Pamungkas, Endang Wahyu, and Viviana Patti. (2020) ["#NonDicevoSulSerio at SemEval-2018 Task 3: Exploiting Emojis and Affective Content for Irony Detection in English Tweets"](https://www.aclweb.org/anthology/S18-1106.pdf) SemEval 2018.


<!-- 
---
```
Post comming soon.
``` -->
