# CS5760 Natural Language Processing — Homework 2

## Student Information

Name: Madhu Karishma Gurram 
Course: CS5760 Natural Language Processing  
Semester: Fall 2026


Assignment Overview

This homework covers Naive Bayes classification, classification harms, bigram language models, zero-probability problems, smoothing, backoff models, and evaluation metrics.

The programming portion implements a bigram language model in Python using Maximum Likelihood Estimation (MLE).

Part I — Written Questions

The written portion of the assignment includes:

Naive Bayes document classification using Add-1 smoothing

Harms of classification

Bigram probability calculations

The zero-probability problem

Add-1/Laplace smoothing

Backoff models

Precision and recall

Macro and micro averaging

Naive Bayes Classification

For the document:

predictable no fun

the Naive Bayes scores are:

Negative score ≈ 6.11 × 10^-5
Positive score ≈ 3.28 × 10^-5

Since the negative score is higher, the document is classified as:

Negative

Bigram Language Model

The bigram calculations demonstrate how sentence probabilities are calculated by multiplying the conditional probabilities of consecutive words.

Add-1 smoothing is used to avoid zero probabilities for unseen words or bigrams.

Backoff

The backoff model uses a shorter context when a longer n-gram, such as a trigram, has not been observed in the training data.

Evaluation Metrics

The assignment also calculates precision, recall, macro averages, and micro averages using a multi-class confusion matrix.

Part II — Programming

Bigram Language Model

The Python program is contained in:

homework2.py

The program implements a simple bigram language model.

Training Corpus

The program uses the following training sentences:

<s> I love NLP </s>
<s> I love deep learning </s>
<s> deep learning is fun </s>

What the Program Does

The program:

Creates the training corpus.

Calculates unigram counts.

Calculates bigram counts.

Calculates Maximum Likelihood Estimation (MLE) bigram probabilities.

Calculates the probability of a complete sentence.

Tests the two required sentences.

Compares their probabilities.

Prints which sentence the model prefers.

MLE Bigram Formula

The bigram probability is calculated using:

P(w2 | w1) = Count(w1, w2) / Count(w1)

Test Sentences

The program evaluates:

S1 = <s> I love NLP </s>

S2 = <s> I love deep learning </s>

Results

The program produced:

P(S1) = 0.3333333333333333
P(S2) = 0.16666666666666666

Therefore, the model prefers:

S1 = <s> I love NLP </s>

because S1 has the higher probability.

Files in This Repository

CS5760-Homework2/
│
├── homework2.py
├── README.md
└── CS5760_Homework2.ipynb

homework2.py

Contains the Python source code for the bigram language model.

README.md

Contains information about the assignment, implementation, and results.

CS5760_Homework2.ipynb

Contains the Google Colab notebook used to run and test the Python program.

How to Run the Program

The program requires Python 3.

Run the following command from the directory containing homework2.py:

python homework2.py

The program will calculate the unigram and bigram counts, calculate the sentence probabilities, and display which sentence has the higher probability.

Conclusion

This assignment provided practice with Naive Bayes classification, Add-1 smoothing, bigram language models, zero-probability problems, backoff models, and classification evaluation metrics.

The programming portion demonstrates how a bigram language model can calculate sentence probabilities and compare two sentences based on their probabilities.
