# Model Card - Toxicity in Text

## Model Details
- The TOXICITY classifier provided by Perspective API [32], trained to predict the likelihood that a comment will be perceived as toxic.
- Convolutional Neural Network.
- Developed by Jigsaw in 2017.

## Intended Use
- Intended to be used for a wide range of use cases such as supporting human moderation and providing feedback to comment authors.
- Not intended for fully automated moderation.
- Not intended to make judgments about specific individuals.

## Factors
- Identity terms referencing frequently attacked groups, fo- cusing on sexual orientation, gender identity, and race.

## Metrics
- Pinned AUC, as presented in here [11], which measures threshold-agnostic separability of toxic and non-toxic com- ments for each group, within the context of a background distribution of other groups.

## Ethical Considerations
- Following [31], the Perspective API uses a set of values to guide their work. These values are Community, Trans- parency, Inclusivity, Privacy, and Topic-neutrality. Because of privacy considerations, the model does not take into ac- count user history when making judgments about toxicity.
 
## Training Data
- Proprietary from Perspective API. Following details in [11] and this includes comments from a online forums such as Wikipedia and New York Times, with crowdsourced labels of whether the comment is “toxic”.
- “Toxic” is defined as “a rude, disrespectful, or unreasonable comment that is likely to make you leave a discussion.”

## Evaluation Data
- A synthetic test set generated using a template based approach, as suggested in [11], where identity terms are swapped into a variety of template sentences.
- Synthetic data is valuable here because [11] shows that real data often has disproportionate amounts of toxicity directed at specific groups. Synthetic data ensures that we evaluate on data that represents both toxic and non-toxic statements referencing a variety of groups.

## Caveats and Recommendations
- Synthetic test data covers only a small set of very specific comments. While these are designed to be representative of common use cases and concerns, it is not comprehensive.

## Quantitative Analyses
<img width="100%" alt="Quantitative Analyses" src="https://user-images.githubusercontent.com/1875500/226171968-57eb1d5f-426a-4fd5-9ed2-62fcae319a99.png">