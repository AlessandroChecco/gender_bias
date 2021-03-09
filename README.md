# User Bias in Image Search
Dataset used in  the paper

Otterbacher, J., Checco, A., Demartini, G., & Clough, P. (2018, June). Investigating user perception of gender bias in image search: the role of sexism. In The 41st International ACM SIGIR Conference on Research & Development in Information Retrieval (pp. 933-936).

It contains 2,811 query-description comparisons for 281 different users.

# Dataset description
We release two datasets:

1. final_anonymised.csv contains the results of the experiment, where each record represents a different users.
2. pivoted_anonymised.csv is the pivot of final_anonymised.csv so that each query shown is a different record.

# Structure of the experiment
1. Repeat the following ten times (counter i): 
   - A grid with 9 images (the top 9 in the list in i_imageurl) is shown. This images are obtained  using the query *i_query* (this query is not shown to the participant.
   - Ask the participant: "What are the keywords that better represent the images?". The answer is stored in *guess_i*
   - The participant is not allowed to go back, if they try to click 1 is added to *remorse_i*
2. The following questions about search engines are asked:
   - How objective do you think search engines are in general?" stored in *objective*.
   -  "What search did you last perform using an image search engine? [Optional]" stored in *last_search*
   -  "Can you recall an image search performed recently where you felt the results did not provide an objective view? [Optional]" stored in *biased_search*
   -  "How skilled  do you consider yourself at using search engines?" stored in *proficiency*
   -  Approximately, how many image searches you make per week? (insert a whole number) stored in *experience*
3. Now this is repeated again ten times (counter i):
   - A grid with 9 images (the top 9 in the list in i_imageurl) is shown (the same grid as before). 
   - "How objective do you think the results of the search engine are for the query *i_query*?" stored in *specific_bias_i*
   -  "Can you explain why in your words?" stored in *explanation_bias_i*
   -  "We obtained these images from a search engine by using the query: *i_query*, while you described the images with the keywords: *guess_i*. Please answer to some questions about the difference between the two keywords
      - "How similar are the keywords?" stored in *similarity_i*
      - In which characteristic(s) the two keywords *i_query* and *guess_i* differ? (please only focus on the difference between the two texts, don't consider the images here) stored in *semantic_i*
      - "Which keywords better describe the above search engine results?" (it's a two options choices, either the search engine or the participant choice) stored in *better_i*
      - "Can you explain why in your words?" stored in *explanation_i*
4. "We will now ask you a series of 22 questions about relationships between women and men. Please indicate, for each statement, the degree to which you agree or disagree." HERE THE ASI questionnaire is administered. stored in *asii*
5. "We will now ask you some demographic questions that will help us to better understand how to improve search engines." stored in *age*, *gender*
6. "Thank you! Do you have any feedback regarding this task?" stored in *feedback*


## Columns Description
We use x$y to represent a range of columns. For example asi1$22 represents the columns asi1, asi2, ..., asi22.
We put the domain in square brakets, where appropriate.

- *_unit_id*: main id
- *id*: this is allows to compare experiments between different countries.
- *_channel*: Crowdflower channel used
- *_trust*: the worker trust, given by CrowdFlower
- *_worker_id*: worker id (anonymised)
- *_country*: country
- *_region*: region
- *_city*: city
- *_ip*: IP address (anonymised)
- *age*: age range [0-18,19-25,26-35,36-50,50-80,>80"]
- *asi1$22*: answer to the ASI [1-7], already corrected according the indicated reversals: items 2, 3, and 7 are con-trait items, phrased in the reverse. HSS items 3, 6, and 9 are also con-trait items.
- *better_0$9*: "Which keywords better describe the above search engine results?" [Your answer - Search engine query]
- *biased_search*: Can you recall an image search performed recently where you felt the results did not provide an objective view? [Free text - Optional]
- *experience*: Approximately, how many image searches you make per week? (insert a whole number) [integer]
explanation_0$9: refering to better$, explanation of whether the search engine or the guess is better: "Can you explain why in your words?"
- *feedback*: [free text] worker final feedback
- *gender*: worker gender [Male, Female, Other]
- *guess_0$9*: worker image grid description, answering the question "What are the keywords that better represent the images?"
- *last_search*:  What search did you last perform using an image search engine? [Free text - Optional]
- *objective*: How objective do you think search engines are in general? [from 1 (very subjective) to 7 (very objective)]
- *proficiency*: How skilled  do you consider yourself at using search engines? [from 1 (non skilled) to 7 (very skilled)]
- *remorse_0$9*: it's an [integer] that shows how many times the worker clicked back to signal they changed their mind about the query they just guessed
- *worker_user_agent*: worker user agent (anonymised)
- *semantic_0$9*: In which characteristic(s) the two textual descriptions differ?
- *similarity_0$9*: How similar are the two queries? [from 1 (very different) to 7(very similar)]
- *specific_bias_0$9*: How objective do you think the results of the search engine are for the query '{{query}}' [from 1 (very subjective) to 7 (very objective)]
- *tentative_0$9*: it's an [integer] that shows how many times the worker failed to guess because they put a very small word (less than three letters) and clicked next
- *0$9_imageurl_google*: image url (list of urls) from google
- *0$9_imageurl*: image url (list of urls) downloaded (see zip file attached)
- *0$9_query*: query we used to obtain image grid.
- *total_time*: time spent on the task (in nanoseconds)
- *asi_score*: ASI score
- *asi_benevolent_score*: ASI score (benevolent part)
- *asi_hostile_score*: ASI score (hostile part)
- *global_rmse*: mean squared error of perceived bias
- *male_rmse*: mean squared error of perceived bias for male images
- *female_rmse*: mean squared error of perceived bias for female images 
- *neutral_rmse*: mean squared error of perceived bias for neutral images 
- *global_offset*: mean of errors where positive error means tendency to perceive a bias for neutral images and negative error is the opposite. Zero can mean no bias or balanced errors in the two directions!


# Citing the dataset
Otterbacher, J., Checco, A., Demartini, G., & Clough, P. (2018, June). Investigating user perception of gender bias in image search: the role of sexism. In The 41st International ACM SIGIR Conference on Research & Development in Information Retrieval (pp. 933-936).

```
@inproceedings{otterbacher2018investigating,
  title={Investigating user perception of gender bias in image search: the role of sexism},
  author={Otterbacher, Jahna and Checco, Alessandro and Demartini, Gianluca and Clough, Paul},
  booktitle={The 41st International ACM SIGIR Conference on Research \& Development in Information Retrieval},
  pages={933--936},
  year={2018}
}
```
