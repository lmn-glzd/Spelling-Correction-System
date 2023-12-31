# Development-of-Spelling-Correction-for-Azerbaijani-Language
The most fundamental tools for word processing and document preparation are spelling correction systems. A spelling correction system is defined as detecting and substituting wrongly spelled words with the correct ones. In other words, it is a tool that parses the spellings of words in a text, validates them, and suggests reasonable alternatives if the spell checker has doubts about the word's spelling.
This project aims to create a spell correcting system based on algorithms adapted to our national language - Azerbaijani. This paper represents conducted research, data collection, and development process of a spell checker system. Since Azerbaijani has an agglutinative function, implementing the problem requires a more complex solution than in other languages. Because of its morphological structure, various words may be generated by adding suffixes and affixes to the words. It implies that there are many different morphological forms to spell the same word, making it difficult to find a comprehensive library that has all of them.

To take the first step in the project, we conducted an in-depth study of the methods used for spelling correction. One of the approaches we examined was Norvig's method proposed by Peter Norvig, an American computer scientist. To perform spelling correction, Norvig's technique uses the minimum edit distance algorithm and a probability-based on word frequency. The other approach we found is an N-gram model, a probabilistic language model for estimating a most likely word to follow a sequence of words in such a series of (N-1) words. Different N-grams types are commonly mentioned, such as Unigram, Bigram, and Trigram. Even though Norvig's method uses only unigram, we also applied bigram for our project. Inside the project, we also attempted to apply the Deep Learning method, a machine learning and artificial intelligence methodology that replicates how humans acquire knowledge. In order to train data, two approaches were used. Firstly labeling of misspelled data was done manually. The other approach was taking clean data samples from books and news websites to add synthetic typos and misspellings in random places.
As our spelling checker system utilizes two methods: Norvig's spell correction method and the bigram method, we used three accuracy measurement rates to evaluate and compare the performance of these methods. As the result of applying accuracy functions on both methods with 100 sentences, we obtained the fix rate of 20% and 33% for Norvig's and bigram methods, respectively. Additionally, we have calculated accuracy for 34000 sentences and obtained the 48% fix rate. A website for the system has also been developed where users can enter  sentences to be corrected by our spell checker.
In the future, we are planning to utilize the Deep Learning method to improve the accuracy of our spell checker system. As the deep learning models require large amounts of data to learn from, we plan to scrap web and social media platforms on a larger scale to acquire more Azerbaijani data.

#Application

This model works with Python 3. and above. For usage simply import norvig file and run duzelt() function. This function has two modes: most probable and most frequent.
example:

from norvig import *
duzelt('muellim qiymeti artir')
output:'müəllim qiyməti artır'

duzelt('bugn hava cox gozaldi')
output:'bugün hava cox gözəldi'

Note:
For running model you need to download pregenerated pickle files from the following link. These pickle files are generated from files from same directory.
Link: https://drive.google.com/drive/folders/1kmtUgDO05VXsG-CTGnbGex9STyA59RmR
