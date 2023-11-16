The purpose here is to show that you can get better summarization than GPT 4 at 22.5 times cheaper the cost.
You can accomplish this assuming that you dont need to parallize (ie do the summary super quickly).

You could probably index things at night, and vectorize it then for later.  

This will break a document down into "sentances"
Then it will create a paragraph of 5 sentances.
Then it will create a summary & a title of that paragraph.
Then it will summarize the summaries.



# llm_gpt3.5-vs-gpt4-comparison
1.run llm_setup.sh
This will install necessary packages.

2.Export your OPENAI_API_KEY
"export OPENAI_API_KEY=yourkeyhere"

3.Hit return each time to get through the prompts.

4. View on your browser heatmap.png , heatmap_chunk_topics.png 

5. stage 2 uses the larger gpt-3.5 16k as opposed to 4k.


