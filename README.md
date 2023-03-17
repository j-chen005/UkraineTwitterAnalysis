# Topic Modelling and Emotion Analysis of the Tweets of British and American Politicians on the Topic of War in Ukraine
This project focuses on the content and emotive features of four British and American politicians’ posts that were published on their official Twitter accounts during the first three months of the Russian invasion of Ukraine. The politicians studied were Boris Johnson, Yvette Cooper, Joe Biden, and Marco Rubio.

## Requirements
- Jupyter Notebook or Jupyter Lab
- Python 3.10 
- NLTK (Natural Language Tool Kit)
- Demoji 1.1.0
- NRC Lexicon 4.0
- [GSDMM](https://github.com/rwalk/gsdmm) (Gibbs sampling algorithm for a Dirichlet Mixture Model)

## Paper
[The paper](https://eejpl.vnu.edu.ua/index.php/eejpl/article/view/658) for this research was published in the East European Journal of Psycholinguistics (Vol. 9 No. 2).

## Methods
This project was conducted in 4 phases:
### Phase 1: Dataset Construction
Tweets about the war in Ukraine were manually chosen by examining the Twitter accounts of the four politicians. Since the Ukraine war was impacted by both the U.S. and U.K. without them fighting in it directly, two British politicians and two American politicians were selected. Boris Johnson, Prime Minister of the UK, and Yvette Cooper, the Labour MP and Shadow Home Secretary of the State for the Home Department, were chosen due to their important roles in the government and their membership in opposing political parties (Conservative Party and Labour Party, respectively). By examining two politicians from different political parties, it was believed that two different opinions on the war would be obtained, and a more accurate understanding of the opinion of the country as a whole would be gained. The U.S. President Joe Biden, a Democrat, and Senator Marco Rubio, a Republican, were chosen for the same reasons.
### Phase 2: Term Frequency and Distribution
Voyant Tools was used to calculate the raw frequency -- the actual number of occurrences of a term in a politician’s set of tweets -- and relative frequency -- the ratio of the frequency of a specific term to the total amount of words in the set of tweets -- of each politician's set of tweets. These frequencies were then plotted over time based on the time each tweet was made. 
### Phase 3: Topic Modelling
I implemented the Gibbs Sampling algorithm for the Dirichlet Multinomial Mixture model (GSDMM) on each politician’s dataset of tweets. The GSDMM algorithm is an unsupervised machine learning method that groups the tweets of each politician into unnamed “clusters,” or topics, based on text similarity. Using the results of the unsupervised clustering, I examined the five most common tokens of each cluster to manually assign each cluster a topic. 
### Phase 4: Emotion Analysis
After converting the tweets into lists of tokens, I evaluated the emotions of the tweets using the NRC Lexicon. Each word in the lexicon has certain emotional scores assigned to it, and so the scores for each word add up to a final emotion score for each emotion in that tweet. The total emotion scores of all the tweets in a topic can be used to determine the emotions the politician felt towards that topic.

## Conclusions
The frequency of terms, collocations, topic modelling, and emotion analysis performed in this research revealed the attitudes of politicians regarding  different aspects of the war in Ukraine. Topic modelling indicated that when the politicians tweeted about the war, their tweets tended to fall under one of two topics: putin’s actions or Ukrainian support. One exception to this trend was Yvette Cooper, who focused mostly on her own department within the UK government, the Home Office. Additionally, Joe Biden and Marco Rubio showed interest in the topics of russian sanctions and Ukrainian nuclear plants, respectively. Emotion analysis demonstrated that Joe Biden and Boris Johnson, the leaders and figureheads of their respective nations, often expressed positive emotions such as trust and positivity in their tweets, especially the ones supporting Ukraine, in order to shed their actions regarding the war in the best possible light. Even their tweets regarding vladimir putin contained high amounts of positive emotion. Meanwhile, Yvette Cooper and Marco Rubio, two politicians of lower rank than Johnson and Biden, tweeted much more critically about their country’s actions in the war, expressing negative emotions such as fear and negativity. Furthermore, Cooper and Rubio are members of the political parties that are opposite to those of Johnson and Biden, and so their different political views likely resulted in more critical opinions of their country’s response. 

## Acknowledgements
This project was conducted in partnership with Professor Olena Karpina of Lesya Ukrainka Volyn National University.

## References
- Bird, S. (2006, July). NLTK: the natural language toolkit. In Proceedings of the COLING/ACL 2006 Interactive Presentation Sessions, 69-72.
- Crystal, D. (2011). A Microexample: Twitter. Internet Linguistics: A Student Guide. London and New York : Routledge. Taylor & Francis Group, 36-56.
- Mohammad, S. M., & Turney, P. D. (2013). NRC Emotion Lexicon. National Research Council, Canada, 2, 234.
- Weisser, C., Gerloff, C., Thielmann, A., Python, A., Reuter, A., Kneib, T., & Säfken, B. (2022). Pseudo-document simulation for comparing LDA, GSDMM and GPM topic models on short and sparse text using Twitter data. Computational Statistics, 1-28.
- Yin, J., & Wang, J. (2014, August). A dirichlet multinomial mixture model-based approach for short text clustering. In Proceedings of the 20th ACM SIGKDD international conference on Knowledge discovery and data mining, 233-242.
- Nerian, S. O. (2018). Dopys u sotsmerezhi yak movlennievyi zhanr internet-komunikatsii. [A post in a social network as a speech genre of Internet communication]. Naukovyy visnyk Khersonskoho derzhavnoho universytetu. Ser. Linhvistyka, 33 (1), 66-70. Retrieved from https://journals.indexcopernicus.com/api/file/viewByFileId/708692.pdf
- Shvelidze, L. D. (2021) Movni zasoby realizatsii komunikatyvnykh stratehii u dyskursi sotsialnykh merezh (na materiali ukrainskoi ta anhliyskoi mov) [Linguistic Means of Implementation of Communicative Strategies in the Social Media Discourse (Based on the Ukrainian and English Languages)]. (Unpublished doctoral dissertation). Vasyl' Stus Donetsk National University, Vinnytsya. Retrieved from https://abstracts.donnu.edu.ua/article/view/9878
- Horoshko E. I., Poliakova T. L. (2011). Lingvisticheskiie osobennosti angloiazychnogo tvittera. [Linguistic features of English-language Twitter]. Ucheni zapysky Tavriiskoho natsionalnoho universytetu imeni Vernadskoho. Ser. Filolohiia. Sotsialni komunikatsii, 24 (63), No 2–1. S. 53–58. Retrieved from http://repository.kpi.kharkov.ua/handle/KhPI-Press/49133
- Poliakova T. L. (2021). Leksychni zasoby v zhanri tvitynh v anhlomovnii politychnii internet-komunikatsii [Lexical means in the genre Tweeting in English political Internet communication]. Zakarpatski Filolohichni Studii, 14 (1), 177-181. https://doi.org/10.32782/tps2663-4880/2020.14-1.32
- Crystal, D. (2011). A Microexample: Twitter. Internet Linguistics: A Student Guide. London and New York : Routledge. Taylor & Francis Group, 36-56.
- Nikolaieva, T. M. (2019) Leksyko-semantychni aspekty movy sotsialnykh merezh [Lexico-semantic aspects of the social networks language]. Zakarpatski Filolohichni Studii, 9 (2), 96-101. Retrieved from https://dspace.uzhnu.edu.ua/jspui/handle/lib/33170
