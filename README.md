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

# general idea
1. This is a reference example of summarizing an hour-long conversation (state of the union) with paragraphs.  You can summarize at 22.5 times cheaper than GPT4, if you use GPT3.  TL;DR the code is you can get better summarization than GPT4 if you think in logical paragraphs and detect subject changes ie topic changes… so… if you:
Create sentence fragments by breaking on ‘.’ ‘,’ ‘?’ etc.. (so you break on ideas as opposed to character count)

2. Then, break things into paragraphs. so you don’t cut off a chunk on a logical idea boundary, and have a ‘logical’ idea overlap (as opposed to a fixed character amount like everyone is doing)

3. Then, summarize each paragraph and create a title for it.

4. Then use gpt-3.5-16k to summarize the summaries.

5. You can also do a comparison of the paragraphs to determine cosine similarity so you can actually get a better notion of when the topic changes on top of these paragraphs.  U could use images to see an idea change..  jpg, gif
The tradeoff (there’s always a tradeoff) is that this doesn’t do parralization and serializes it so it of course is going to be slower…whudua expect at 22.5 times cheaper?

6. So if someone sends a 1K prompt and gets a 1K response, aka completion, their cost for GPT-3.5-turbo is 2 x $0.002 = $0.004. Whereas the same token count for GPT4 8K model would be. 1K prompt + 1K completion = $0.03 + $0.06 = $0.09.

7. Some people said it has high RPM, which is true, but you should be using an account with more RPM non-throttle.
