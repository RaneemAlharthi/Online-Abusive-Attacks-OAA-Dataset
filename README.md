 **Online-Abusive-Attacks-OAA-Dataset Description:**
The Online Abusive Attacks (OAA) dataset, the first benchmark dataset providing a holistic view of online
abusive attacks, including social media profile data and metadata for both targets and perpetrators, in addition
to context. The dataset contains 2.3K Twitter accounts, 5M tweets, and 106.9K categorised conversations.
This is the aggregated form of the dataset. **Data Collection & Resources**
Three phases
1. Topic Selection, which involves identifying popular and contemporary topics combined with existing
hashtags;
2. Target Identification, where the topics from the first
step are used to retrieve a set of users likely to be the
targets of abuse; and
3. Target-centric data collection, where tweet timelines
for the selected targets were harvested. The extensive
data collection leads to a dataset that is less skewed
towards the selected hashtags, hence retrieving a more diverse dataset.
**Data Labelling Guidelines:**
we label tweets in our dataset using Google Jigsaw’s Perspective API Perspective API . The Perspective API defines toxicity for a given text as ‘‘a rude, disrespectful, or unreasonable
comment that is likely to make people leave a discussion’’,
and provides a toxicity score for eight different attributes.
These attributes are toxicity, severe toxicity, identity attack,
insult, profanity, and threat; see Table 1 for the definition.
Figure 3 provides a brief explanation of the Perspective
API system. We use a combination of perspective API’s six
attributes, marking a tweet as abusive if the tweet exceeds
a threshold for any of the API attributes. More specifically,
we label a tweet as abusive if it receives a score of 0.9 or
above for any attribute, which we chose as a high value so that
abusive content can be deemed as such with high confidence,
given our priority for precision rather than recall.
**MANUAL VALIDATION OF LABELLING**
To further verify the labels obtained through Perspective API,
we manually annotated a sample of the data by two annotators. These two

 annotators are experienced in hate speech
research, with a Ph.D. level background in computer science and psychology. To perform the manual annotation, first,
we trained the annotators and provided feedback using the exact definition from the Perspective API. After the training, both annotators annotated a randomly selected sample of 202 tweets. Next, we measure the Inter-Annotator Agreement
(IAA) using Cohen’s kappa score . both annotators have a moderate agreement with Perspective API’s labels, where the overlap of agreement is 84% (annotator 1 vs. Perspective) and
91% (annotator 2 vs. Perspective). Given the reasonably high scores in the agreements between annotators and Perspective API, we deem the latter a valid approach that enables us to scale the analysis with limited noise.
**Paper Citation**
@article{alharthi2023target,
title={Target-Oriented Investigation of Online Abusive Attacks: A Dataset and Analysis},
author={Alharthi, Raneem and Alharthi, Rajwa and Shekhar, Ravi and Zubiaga, Arkaitz},
journal={IEEE Access}, year={2023}, publisher={IEEE}
}
