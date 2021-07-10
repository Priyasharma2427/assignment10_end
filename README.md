<b> 1. Precision , Recall and F1 score </b>

To understand these metrics, we will take the heart disease dataset. Here we have to predict if the patient is suffering from heart ailment or not.

Confusion matrix helps us to gain an insight into how correct our predictions were and how they hold up against the actual values.

![image](https://github.com/Priyasharma2427/assignment10_end/blob/main/latest_cm.png)

1 : Patients having heart disease.
0 : Patients who don’t have heart disease.

Actual Values : 
1. The patients who actually don’t have heart disease : 40
2. The patients who actually have a heart disease : 51

Predicted Values :
1. The patients who were predicted as not having a heart disease : 41
2. The patients who were predicted having a heart disease : 50

True Positives : Patients who are having heart disease and model also predicted them having heart disease.
False Positives : Patients who are not having heart disease but model predicted them having heart disease.
False Negatives : Patients who are having heart disease but model predicted them not having heart disease.
True Negatives : Patients who are not having heart disease and model also predicted them not having heart disease.

Precision is the ratio between the true positives and all the predicted positives. 
Basically, it is tells you what proportion of positive identificiations were actually correct.

![image](https://github.com/Priyasharma2427/assignment10_end/blob/main/precision.png)

True positive (TP) = 43
False Positive  (FP) = 7
Predicted Positives = 50

Precision = True positive / True Positive + False positive
	    =  43 / 50 
	    = 0.86 

Recall is the ratio between the true positives and all the actual positives.
Basically, it tells you what proportion of actual positives were identified.

![image](https://github.com/Priyasharma2427/assignment10_end/blob/main/recall.png)

True Positives (TP) = 43
False Negatives (TN) = 8
Actual Positives = 51

Recall = True Positives / False Negative + True Positive
           = 43 / 51
           = 0.84

    
F1 score is a function of precision and recall.   F1 score is needed when you want to have balance between Recall and Precision.

There are lot of situations where both precision and recall are equally important, in such cases we uses f1- score.  F1-score is harmonic mean of recall and precision. 

![image](https://user-images.githubusercontent.com/36500978/125171659-f5506300-e1d2-11eb-84c5-eb02dbed55d0.png)

F1 score = 2 * ((0.86 * 0.84) / (0.86 + 0.84))
	   = 0.85

<b> 2. BLEU </b>

Bilingual evaluation understudy is an algorithm for evaluating the quality of text which has been machine translated from one natural language to another.

The closer a machine translation is to a professional human translation, the better it is : BLEU: a Method for Automatic Evaluation of Machine Translation by Kishore Papineni

To measure the machine translation effectiveness, we will evaluate the closeness of the machine translation to human reference translation using a metric known as BLEU-Bilingual Evaluation Understudy.

BLEU compares the n-gram of the candidate translation with n-gram of the reference translation to count the number of matches.
The more the number of matches between candidate and reference and translation, the better is machine translation.
BLEU can be computed as a ratio of covered candidate words out of total no of candidate words.
<b> BLEU = Covered / Total no of words in the candidate. </b> 

<b> 3. Perplexity </b>
It is a metric used essentially for language models. 
Assuming that a language model is a probability matrix between a word and the next word that occurs in the corpus of the training set, Perplexity, known as PP, is “the inverse probability of the test set, normalised by the number of words”. In the Perplexity equation below, there are N words in a sentence, and each word is represented as w, where P is the probability of each w after the previous one. Also, we can expand the probability of W using the chain rule as followed.

![image](https://user-images.githubusercontent.com/36500978/125171478-182e4780-e1d2-11eb-8c35-63ccaa3219dd.png)

Given the equation above, the more accurate the language model, the higher the probability of the word sequence, the lower the perplexity. In other words, we try to minimise the value of PP(W) to get a better model.

<b> 4. Bert Score </b>
It is a automatic evaluation metric for text generation. It computes similarity score. Instead of finding an exact match, the contextual embedding of each token in the candidate sentence is compared with the embeddings of all tokens in the reference sentence. The embeddings are compared based on cosine similarity.

![image](https://user-images.githubusercontent.com/36500978/125171472-0c428580-e1d2-11eb-8b6d-1a1226be5661.png)

