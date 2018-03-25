What is Reddit?
Reddit is a social news aggregation site and discussion board that houses many interactive communities. These communities, termed "subreddits", each have a particular thematic focus that collectively spans many aspects of pop culture. We will study the nature of the discourses held within these many, perhaps culturally idiosyncratic, communities and attempt to visualize the diverse array of underlying sentiments that pervade the intra-communal interactions amongst their members.

Overview
In our endeavor to map the emotional contents of various subreddit communities, we will have to choose some form of sentiment analysis to conduct on each comment observation from our dataset. Sentiment analysis refers to the process of computationally extracting and quantifying the emotions, attitudes, and opinions expressed through textual data and is a specific subfield of the much broader discipline of natural language processing (NLP). Recent studies within this field into social media sentiments have successfully utilized a variety of noisy labels ranging from a handful of emoticons to assortments of hashtags as a form of distant supervision. Following this paradigmn, we will be incorporating a Deep Neural Network for sentiment classification that is detailed in a relatively recent paper published by Felbo et. al [1]. This work introduces an interesting approach to classifying textual data into sentimental categories of (64) relevant emojis. More specifically, the so-called "DeepMoji" model applies already established LSTM architectures to an extensive corpus of tweet-emoji labeled data to learn text-sentiment associations while also incorporating an original approach for transfer learning that the authors refer to as the "chain-thaw" method (which has been empirically shown by the authors to allow the model to generalize to more traditional sentiment analysis benchmarks). Taking inspiration from this work, we will apply the pretrained DeepMoji model towards the Reddit comments dataset in the hopes of being able to map subreddits into a low-dimensional embedding of sentiments. This clustering and visualization objective is similar to that of [2,3] in that we are trying to bring to light interesting relationships between various subreddit communities. In this case, however, we are less so interested about similarities in concrete subject matter and more so in the emotional connections/disparities between subreddits and of how these diverse communities encourage discussions that involve differential sentimental expressions.