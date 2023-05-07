# Zara Social Listening

Zara is one of the most decorated and celebrated clothing and accessories brand in the world with 1.3M followers on Twitter. 
With the huge social media presence, the brand does many campaigns and promotions on Twitter and Instagram. 
The goal was to: 
1. Identify what people talk about when they mention Zara in their tweets.
2. Identify potential influencers that could help the brand. 
3. Extraction of keywords & hashtags 

## Extracting Data from Twitter

- Since twitter was the only source of data collection snscrape library was used to extract two sets of data, one for the keywords and hashtags and, another for finding potential influencers and conversations surrounding the brand.
- Extracted more than 3000 tweets from Zara's handle for the past 10 years and saved the file as Zara_tweets.csv.
- The second dataset contained all the tweets that tagged Zara in the past one year. Was able to extract around 34,000 tweets and used this data to find out the influencers who play a significant role in the brand's promotions. The file is saved as zara_influencers.csv
- The tweets have various hashtags, special characters, website links, mentions and stop words. Later used a pre-processing function to eliminate unwanted characters and make the tweets consistent.
- Used this corpus to build our understanding of how Zara used their Twitter handle to promote their brand, make announcements, collaborations with creators etc. Using this data; we found the top keywords, bi-grams, tri-grams and vital hashtags.
- Set the date range for the second dataset from Jan 2022 to Jan 2023 and only english tweets were extracted. The code for the scraper used can be found [here](https://colab.research.google.com/drive/1cKnnkrn6zNQ0omUWXQgpesTrVrt4Zpcc?usp=sharing).

## Extracting Keywords and Hashtags

### Keywords
![Screenshot 2023-04-13 at 6 22 58 PM](https://user-images.githubusercontent.com/105431583/231764511-74e3a900-d9cb-46a3-aa18-346448ffeadf.png)

- To extract keywords, KeyBERT was used, a very smooth and efficient way of extracting keywords that use the BERT embeddings to create meaningful words and phrases relevant to the corpus.
- For some of the words which would not be relevant in understanding the effectiveness, were removed by marking them as stop words and then found the top 20 most appropriate ones.
- Here we see that the top 3 keyword is 'woman', 'editorial' and 'kid'. It makes sense as Zara's collection is inclined towards Women and Kids.
- Other primary keywords include 'summer', 'spring', 'winter', and 'season', which have been mentioned several times as the brand launches new collections before the start of these seasons. Editorial also shows up which is an online publication of Zara showcasing their best products with collaborations with models/celebrities.
- Keywords like 'online' and 'store' signify the brand's presence when new products are launched in both modes.
'srpls' and 'trf' have also made it to the top 20 keywords. trf is short for ‘Trafaluc’ and as per Zara : “Trf is our more trend-led collection with a more daring aesthetic, including statement pieces such as slogan T-shirts, oversized hoodies, printed dresses and co-ords, plus statement denim”, which is aimed at the younger generation.
- Lookbook is one of the popular hashtags and keywords where Zara posts pictures of their models mixing up their product line-ups to promote an entire outfit head to tow.
- On the other hand, 'srpls' is the Zara collection of streetwear clothing, which is a rage amongst its customers. It's also a premium priced lineup of clothing products compared to other listings sold by the brand.

### Hashtags
![Screenshot 2023-04-13 at 6 26 12 PM](https://user-images.githubusercontent.com/105431583/231765321-1ed0dea6-ead2-456d-ab82-047da9a7d6f6.png)

- Another important aspect of social listening is finding out the most relevant and frequent hashtags.
- Using the extracted data,the most tweeted hashtags was found, which would enable us in building a campaign around the brand Zara.
- #zaradaily bags the top spot with 218 mentions. Followed by #zaranewin and #woman in second position.
- While #woman, #zarawoman, #zarakids, #zaraeditorial #zaraman are more focused on associating the brand with the target audience, also find hashtags on the days of the week, like #monday, #tuesday, #thursday, which might have reference to launch of some new line of product, or any special campaign.
- There are also several hashtags which specify the collection type, like #aw14, #aw15, #trf, #fw11 and #ss14 which specify the collection season like Autumn/Winter, Fall/Winter and Spring/Summer.

## Finding Influencers

- To find out our influencers, the tweets and re-tweets by users who tagged Zara in their conversations was extracted. This way we were able to build a dataset for all conversations surrounding the brand and called it zara_influencers.
- Found out the users which most frequently tagged the brand, and who had the maximum engagement in terms of likes, re-tweets and replies.
- At a high level 3 step process was employed:
1. Setting conditions to extract top-profiles
2. Extracting and Ranking profiles
3. Selecting the most relevant after manually going through each user profile.
- The very first condition was to filter based on the number of times a user tweeted [tweet count] regarding Zara by tagging them. After going through the top 10 profiles we selected [@CocoandVera](https://twitter.com/CocoandVera) and [@GilmoreTee](https://twitter.com/GilmoreTee). The first profile is an active fashion blogger and the second is a Zimbabwean TV personality and Creative Director.
- In the next piece of extraction we were looking at the mean like count of tweets/accounts that tagged Zara. [@Lesdoggg](https://twitter.com/Lesdoggg) made top of the list. She is a female comedian who has actively tagged Zara in her posts due to her outfit showcase on Twitter. [@StudioMDHR](https://twitter.com/StudioMDHR) made our list as a children's show actively airing on Netflix, this was due to a collaboration with Zara to launch a kids line-up of clothing. We believe Zara needs more active collaborations with other companies that kid's can associate themselves with because this one was a successful campaign based on Twitter likes. [@AshikaRanganath](https://twitter.com/AshikaRanganath) is our third recommendation who is a South Indian actress who has used Zara's products in more than a couple of posts on Instagram/Twitter in 2022.
- Third measure was to use the reply count to assess user-profiles and found [@khloekardashian](https://twitter.com/khloekardashian) on the list of influencers. Her company, ["Good American"](https://www.goodamerican.com/) has actively collaborated with Zara to launch a new line-up. [@TheSocialCTV](https://twitter.com/TheSocialCTV) is a TV show that delves into pop-culture topics and lifestyle subjects. and is the second account we recommend, as multiple hosts of the TV show have tagged Zara to showcase their outfits for the episode.
- [@WomensRightsNet](https://twitter.com/WomensRightsNet) was an account from our retweet count measure that aim to protect women's rights. There were multiple complaints against a host of clothing brands that maintained unisex changing rooms, where a couple of Zara stores came under fire. This received fair attention to order for separate spaces for both genders especially for a brand who primarily sells to women.
