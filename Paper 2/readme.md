# What is the vocabulary of flaky tests.

 ### Authors: 

 ###  
 Gustavo pinto
Marcelo d’Amorim
Breno Miranda
Supun Dissanayake
Christoph treude
Antonia Bertolino.

>Conference:
Tue 30 Jun 2020 14:36 - 14:48 at MSR:Zoom - ML4SE Chair(s): Kevin Moran
 
 [Paper link]( https://2020.msrconf.org/details/msr-2020-papers/43/What-is-the-Vocabulary-of-Flaky-Tests- "click here to view paper")

> Media link: https://youtu.be/NsHfSA_S7Yo

# **Introduction and motivation**: 

Regression testing is an important practice in software development. It is defined as the fully or partial selection of already executed tests cases which are reexecuted to ensure existing functionalities work fine. Most of all, the result should be deterministic but that is only in theoretical value. However in the practical approach, the results are nondeterministic. i.e. tests are flanky. These are tests that may unpredictably pass or fail when rerun, even will no changes to configuration under test.
Practiconers rescue a number of units a time every test to gain a required result. They are spending important resources & time in analyzing failures that are due to flank test not due to problem in production code. Thus frankly test are studied and evaluated for time being to welcome the causes underlying this flankiness & also what are stragedies to remove this cause.  So there are 2 aims in overcoming the flank test result. 
1. Timely & efficiently recognize the flank test result, even well before it is committed in the test repository.
2. Differentiate flank test from nonflank test result.
3. To guide the identification of flaky tests that are been introduced in test repository.
# **Methodology**: 

1. Compilation of vocabulary of flaky test:
+	All identifiers are extracted from test cases in data set. After obtaining identifiers, we used the identifiers in their original form or split these identifiers using camel case syntax & converted all resulting tokens to lower case. Determine the length of each test case in term of lines of codes as process of code’s complexity.
2. A set of automated classifiers for test cases as flaky or nonflaky.
+	Preprocessed flanky & non flanky tests cases are evaluated by algorithms. 
+	The algorithm include randoms forest, decision tree, naïve Bayes, supplest vector, machine & nearest neighbour.
+	The random forest & support vector machine were best performer with metric f score of 0.9 for values of 5 & 10. & identifies splitting has a positive impact on the classifiers performance.
3. Performances evaluation of state of the art classifiers over an existing data set of flaky tests.
+	The data were based on deflakes benchmark. This bench monitor was suggested due to over 50k flaky tests, conducted.
+	Deflexers mark the coverage of several java projects. For each one of them, deflaker observes the latest code changes & marks as flaky any newly failing test that did not execute changed code.
+	They used 24 out of 25 projects of deflexer. And about 64k test cases over all the studied projects.

# **Conclusion**:
•
+	55% of these flanky tests failed only once, 99 times passed thus 100 thresholds might have limited the observation of flanky test.
•
+	Five machine learning algorithm used had good performances in distguinshing flanky from nonflanky tests.
•
+	Vocabulary words such as job table and action are introduced which give information and tokenization which help in earlier identification of flankiness in test for research worker.
+	This all helps practiconer in earlier identification of flankiness and overcome through stragedies of changing vocabulary, fc values that help in increasing efficiency of the test. 








