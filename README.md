# User Bias in Image Search
Dataset used in  "Investigating User Bias in Image Search: A Cross-Regional Study". It contains 2,811 query-description comparisons for \num{281} different users is available at \emph{redacted for anonymous review}.
# Dataset description
We release two datasets:

1. final_anonymised.csv contains the results of the experiment, where each record represents a different users.
2. pivoted_anonymised.csv is the pivot of final_anonymised.csv so that each query shown is a different record.

## Columns Description
We use x$y to represent a range of columns. For example asi1$22 represents the columns asi1, asi2, ..., asi22.
We put the domain in square brakets, where appropriate.

- *_unit_id*: main id
- *_id*: not sure but it can be ignored
- *_channel*: Wrowdflower channel used
- *_trust*: the worker trust, given by CrowdFlower
- *_worker_id*: worker id (anonymised)
- *_country*: country
- *_region*: region
- *_city*: city
- *_ip*: IP address (anonymised)
- *age*: age range []
- *asi1$22*: answer to the ASI [1-7]
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
semantic_0$9: In which characteristic(s) the two textual descriptions differ?
similarity_0$9: How similar are the two queries? [1(very different) - 7(very similar)]
specific_bias_0$9: How objective do you think the results of the search engine are for the query '{{query}}' [1(very subjective)-7(very objective)]
tentative_0$9: it's an integer that shows how many times the worker failed to guess because they put a very small word (less than three letters) and clicked next
worker_user_agent: worker user agent
0$9_imageurl: image url (list) backup in my server
0$9_imageurl_google: image url (list) from google
0$9_query: query we used for image $
