# Data Analysis of App Profitability via Ad Revenue

In this project, data pertaining to apps downloaded on Google Play and App Store was dissected and analyzed to ascertain **what kind of free apps might be best to make for a company that generated the entirety of their revenue from in-app advertisements**.

## Datasets and Metrics of interest.

The datasets for the [Google Play Store](https://www.kaggle.com/lava18/google-play-store-apps/home) and [Apple Store](https://www.kaggle.com/ramamet4/app-store-apple-data-set-10k-apps/home) were publicly available on Kaggle.

Metrics such as the following were acquired from datasets containing info on Google store and the Apple store:
- Price
- Rating
- Category/Genre
- No. of installs
- No. of ratings.

## Data-Cleaning
- Because we were only interested in free apps, the dataframe had to be simplified to exclude apps with a cost.
- Data that was incorrect or duplicate also had to be pruned out of the tables.
- Removed apps in languages other than English. The numbers corresponding to the characters we commonly use in an English text are all in the range 0 to 127, according to the ASCII (American Standard Code for Information Interchange) system. Based on this number range, we built a function that detects whether a character belongs to the set of common English characters or not. If the number is equal to or less than 127, then the character belongs to the set of common English characters. We used this to identify non-English characters in App names.
- To avoid incorrectly excluding English apps that happened to use emojis or special characters (like ™ or 😜), we set a threshold allowance of 3 non-english characters.
- Visually previewed the removed apps to verify most of the removed ones were non-English.

## Data Analysis
Since our end goal is to have our apps up on both markets, we want to be looking at types of apps that are successful in these two markets.

- We observed that apps in google playstore related to entertainment genres, like gaming, were immensely popular. This was a bit less of true of the iOS store. 
- We also verified that this was the case by looking at apps in terms of ratings. 
- When looking at communication apps, social network apps, and navigation apps, we realized that the **average number of installs was being skewed immensely by very popular giants like WhatsApp, Google Maps, and Facebook.** This needed to be kept in mind to avoid mistakenly thinking a category was more popular than it really was.
- **Used lower quartile and median popularities to determine which markets might be harder or easier to break into** (also partly so we avoid competing against established giants like WhatsApp or Facebook).

## Conclusion

In the end, we arrived at the conclusion that due to fitness apps (especially relating to diet control, weight loss, and bodybuilding) being reasonably popular, and having a low barrier to entry (i.e. seeming not too difficult to break into).

Since weight loss (i.e. body fat reduction) is a very significant part of body-building, especially for someone who just casually trains, hoping to achieve abs and some more defined musculature, it might be an extremely good idea to market a way of losing weight through an avenue that people enjoy, i.e. sports. This kind of app would likely do well in both the Google Play and App Stores, which is exactly what our company intends to do.

Furthermore, **fitness and sports-related aps often feature advertisements that sell things like nutrition and weight loss supplements**. Because people interested in improving their health also tend to seek out these supplements to help them reach their goals quicker, **the advertisements we place in our ads would have a very high click rate, thus generating higher revenue**.

The app should be something that sells an approach to weight loss through very accessible and enjoyable means. An appropriately sensationalistic slogan like "lose weight doing what you love!" is also bound to grab attention very quickly might also be something that would go well with the app.
