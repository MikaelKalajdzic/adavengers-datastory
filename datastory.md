---
layout: full
---

![blablabla](assets/img/beer-2.png)

# Pints & Politics: Sipping Through Red, Blue, and Brew US 🍺

*Friday night. Cozy bar in California, USA. At a table, Larry and Jim sit enjoying a beer together.*

**Larry:** (*takes a long sip of his lager*) You know Jim, there’s something poetic about beer. It’s not just a drink – it’s like a mirror for the country. You can tell a lot about people by what’s in their glass.

**Jim:** Yeah I would agree with that… for once. I see elegant people enjoying a nice fancy cocktail. Old folks a glass of whisky… And us, students, a simple, cheap beer.

**Larry:** Nah, that’s not the point I’m making. It’s bigger than just age or class. Think about it, beer is like an unspoken language, man. It reveals where you stand in America, my friend!

**Jim:** (*raises an eyebrow*) Oh, here we go again Larry. Let me guess – you’re about to tell me how beer preferences somehow connect to our political leaning, right?  

**Larry:** Exactly! Think about it… The beers we drink say more about us than we realize.

**Jim:** (*leans back in his chair*) Alright… but where’s your proof? You always come in here with these wild ideas after a few beers.

**Larry:** I’m not giving you a random fun fact. I did some research since the last time we met. And I can guarantee you I found interesting results!

**Jim:** Well, if it’s serious work, now you have my attention.

**Larry:** Oh it’s real work. I analyzed the different beer styles, sentiments, and review ratings across the U.S. I investigated how beer preferences vary by state and if they align with political leanings. Also for swing states, if they gravitate toward specific beer styles during election years. I did all these analyses to see how beer preference trends changed throughout the years of 2004–2016.

**Jim:** (intrigued) Wait, seriously? How did you do all of that? ChatGPT?

*Larry and Jim share a good laugh and take a sip of beer.*

**Larry:** So first, I dug into the BeerAdvocate dataset – over two million reviews from American beer drinkers.

**Jim:** Two million reviews? That’s a lot of data, man. Okay, but how does that connect to politics?

**Larry:** That's where the real fun begins. While BeerAdvocate provides all the beer reviews, I had to gather the political information separately. For that, I used different sources. Firstly, I pulled data on the winning parties in each U.S state, in the election years from 2004 to 2016, from the [U.S. President 1976–2020](https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/42MVDX) dataset. Also, I gathered data on age-specific voting preferences from exit polls. But here’s a catch – it wasn’t available for all states. You know, exit polls are of interest in states that change their political climate over the years, the so-called swing states. Also, conducting these surveys is quite costly, so for states that are consistently Democrat or Republican, they are usually omitted.

**Jim:** All that looks very nice, but wait – just to make sure I’m following, what exactly are you trying to answer with all that research?

**Larry:** Well, at first I wanted to figure out how beer preferences can be categorized and visualized across different dimensions (such as style, emotions, sentiments, and key attributes) to provide a comprehensive understanding of beer types based on the U.S. reviewers.

**Jim:** Alright, that makes sense. And then? I guess it's linked to politics…

**Larry:** Then, I’m diving deeper. I wanted to see how these beer preferences vary across different U.S. states, and can these preferences be linked to political ideologies. Are there specific beer preferences that correlate with Republican or Democratic voting patterns?

**Jim:** Hmmmmm interesting.

**Larry:** And finally, how do beer preferences change over time during election years, particularly in swing states?

**Jim:** You really look passionate about all that!

**Larry:** I mean yeah, I really love beer. This one is very good by the way.

**Jim:** You know I’m not a beer connoisseur, but I really enjoy that one. Actually, for me, all the beers are kinda the same.

**Larry:** (*laughing*) Well my friend, I think you really didn’t have enough beers in your life to say something like that! Cheers!

*Larry and Jim clink their pints*

**Jim:** Cheers to you!

**Larry:** You know, there are actually 8 main beer styles that people commonly talk about. They are: IPA (India Pale Ale), Pale Ale, Red/Amber Ale, Other Ales (covering remaining Ale subcategories), Lager, Stout, Porter, and Pilsner.

**Jim:** So these are the beer styles you focused on in your research?

**Larry:** Yes! Actually, among the reviewed beers in the dataset, there are 104 unique beer styles. I did matching by keywords into the 8 predefined categories. I was left with 56 unique styles. And to give you a clearer idea of their distribution, here’s a cloud of words.
<br/><br/>
<div style="text-align: center;">
  <img src="./assets/img/beer_types_word_cloud.png" alt="Beer Types Word Cloud" style="max-width: 100%; height: auto;">
  <p style="font-size: 14px; color: gray;">Figure 1: A word cloud showing beer styles encompassed by our general categories.</p>
</div>
<br/><br/>

**Jim:** Looks very nice. So you’ve categorized all these beer styles, but how do you know which ones are actually the most popular?

**Larry:** I see you’re starting to get interested now! I analyzed the number of reviews left by U.S. users for each beer style over the years. Check this out!

*Larry shows the interactive chart on his phone*

{% include count_total_reviews.html %}

**Larry:** What you’re looking at here is the count of reviews by beer style, year by year. You can see a clear increase in the overall number of reviews, especially in the late 2000s and early 2010s. Makes sense right? That’s when internet communities and rating websites started to grow in popularity.

**Jim:** That’s awesome! Yeah, I agree, and I see the top 3 beer styles are the same throughout the years: IPA, Other Ale, and Stout.

**Larry:** Absolutely! And also we can notice that after 2008, Stouts consistently ranked third, showing how stable their popularity is among beer enthusiasts.

**Jim:** What about IPAs? I keep hearing about them everywhere.

**Larry:** You’re right! There was a big rise in IPA reviews starting in the mid-2010s. That’s actually when IPAs became the best-selling style in the [craft beer segment](https://www.beervanablog.com/beervana/2019/12/16/the-2010s-in-review). It’s cool to see how the trends in reviews align with real-world sales data.

**Jim:** So basically, this chart doesn’t just show reviews, does it? It’s like a snapshot of how beer culture evolved.

**Larry:** You’ve got it! It’s fascinating to see how much you can learn from data.

**Jim:** Alright, so you know which beer style is the most reviewed, but does that mean they are also the most highly rated maybe?

**Larry:** Not exactly! That’s what I looked into next – figuring out which beer styles received the highest average ratings across the U.S. For this, I used the mean rating across five categories: aroma, palate, taste, appearance, and overall. Look at this, I’ve got a map that shows how beer style preference evolved over time.

{% include fav_beer_us.html %}

{% include count.html %}

The sentiment plot too...

{% include sentiment_states.html %}

comment on results,...

## Connection to politics

plot with winners over years  
what are the confounding factors that we considered and why we went for the ones that we did... 
deeper analysis into potential confounding factors - age, where we get the data from. Why do we interpolate (motivation behind all this)

{% include usmap_politics.html %}

{% include interpolated-vote-distribution.html %}

deeper analysis into potential confounding factors - age, where we get the data from. Why do we interpolate (motivation behind all this)

{% include clustering_states.html %}

## Some other plot for fun because that was lot of work

{% include correlation_matrix.html %}

{% include pairwise.html %}

| Column 1       | Column 2       | Column 3       |
|-----------------|---------------|----------------|
| Row 1, Item 1  | Row 1, Item 2  | Row 1, Item 3  |
| Row 2, Item 1  | Row 2, Item 2  | Row 2, Item 3  |
| Row 3, Item 1  | Row 3, Item 2  | Row 3, Item 3  |

{% include swing_pattern.html %}

{% include top3_styles.html %}

## Sources

Illustrations:  
ChatGPT / Dall-E, [chatgpt.com](https://chatgpt.com).

Datasets:  
MIT Election Data and Science Lab, 2017, "U.S. President 1976–2020", Harvard Dataverse, V8, doi:10.7910/DVN/42MVDX.  
Exit polls, NY Times, [2004](https://www.nytimes.com/elections/2012/results/president/exit-polls.html), [2008](https://archive.nytimes.com/www.nytimes.com/elections/2008/results/president/national-exit-polls.html?mod=article_inline), [2012](https://www.nytimes.com/elections/2012/results/president/exit-polls.html), [2016](https://edition.cnn.com/election/2016/results/exit-polls)
BeerAdvocate dataset, 2019, [drive.google.com/drive/folders/1Wz6D2FM25ydFw_-41I9uTwG9uNsN4TCF](https://drive.google.com/drive/folders/1Wz6D2FM25ydFw_-41I9uTwG9uNsN4TCF).




