# NGram_Language_Model

	N-Gram model is widely used in search engine and spell correction. The search engine will collect typing words history and achieve text auto completion by predicting next words whenever the user types a new word. 
	The datasets is some chapters from three different books. Since a n-gram is a contiguous sequence of n items from a given sequence of text or speech. So firstly, I import this document collection by Hadoop HDFS. I read each document line by line and remove all non-alphabetical symbols. 
	I choose n as 5 so I split each sentence to 1-gram, 2-gram, 3-gram, 4-gram and 5gram. N-gram is based on 1-gram. Here I use Map Reduce method in Java divide sentence and merge into N-gram. 
	The next step is to build language model. I calculate the probability to predict the following word. Here in order to reduce unnecessary computation, I remove some words whose show-up probability is less than a specific threshold. Also to save storage, I only store top 5 words with the highest probabilities. If two words have the same probability, I choose the one which is lexicographically higher. 
	After I complete these methods, I use MySQL to store outputs. Then I use Hadoop to run the code and connect with MySQL by MAMP. I created a simple user web interface for test. Then I randomly test some words, and the results shows it can accomplish text auto completion. 
