# User Bias in Image Search
Dataset used in  the paper
Otterbacher, J., Checco, A., Demartini, G., & Clough, P. (2018, June). Investigating user perception of gender bias in image search: the role of sexism. In The 41st International ACM SIGIR Conference on Research & Development in Information Retrieval (pp. 933-936).

It contains 2,811 query-description comparisons for 281 different users.

# Dataset description
We release two datasets:

1. final_anonymised.csv contains the results of the experiment, where each record represents a different users.
2. pivoted_anonymised.csv is the pivot of final_anonymised.csv so that each query shown is a different record.

## Columns Description
We use x$y to represent a range of columns. For example asi1$22 represents the columns asi1, asi2, ..., asi22.
We put the domain in square brakets, where appropriate.

- *_unit_id*: main id
- *id*: this is allows to compare experiments between different countries.
- *_channel*: Wrowdflower channel used
- *_trust*: the worker trust, given by CrowdFlower
- *_worker_id*: worker id (anonymised)
- *_country*: country
- *_region*: region
- *_city*: city
- *_ip*: IP address (anonymised)
- *age*: age range []
- *asi1$22*: answer to the ASI [1-7] (corrected according the the indicated reversals)
- *better_0$9*: Which description do you think better represent the images? [Your answer - Search engine query]
- *biased_search*: Can you recall an image search performed recently where you felt the results did not provide an objective view? [Free text - Optional]
- *experience*: Approximately, how many image searches you make per week? (insert a whole number) [integer]
explanation_0$9: refering to better$, explanation of whether the search engine or the guess is better: "Can you explain why in your words?"
- *feedback*: [free text] worker final feedback
- *gender*: worker gender [Male, Female, Other]
- *guess_0$9*: worker image grid description
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
- *0$9_query*: query we used to obtain image grid $.
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
