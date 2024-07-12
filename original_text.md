# How to Make Sure No One Cares About Your Open Data
**June 28, 2024**  
 · 6 min · 1121 words · Philip Heltweg

## Table of Contents

Sharing data openly is a noble endeavor. It can drive research, innovation, and transparency. It is also really hard and annoying to do, plus you lose control - who knows what people will get up to. Sadly, publishing open data is often legally required. So your best bet is to technically publish open data, but make sure no one is interested in it. Based on my experience interviewing open data practitioners, working with various open data sources, and teaching students about data engineering, here’s a list of common strategies that will help you avoid any attention by users actually interested in working with your data.

1. **Use an Obscure License**
   The easiest way to scare off potential users is to make it hard to know if your data is even open data in the first place. Avoid common open data licenses that have human-readable summaries (such as the ones published by the OKFN). Make sure to make the actual license your data is under hard to find (avoid using a SPDX identifier in the metadata). If you can, do not use a license at all and refer only to terms of use or similar documents.

   If you can’t avoid a standard license, try to find a license in your local language, that will at least scare off international users.

   Bonus points for publishing on Kaggle with the license “Other (specified in description)” and not writing about the license in the description.

2. **Publish with Only Metadata**
   Look at this exploration map, done by the French national access point to transport data: [https://transport.data.gouv.fr/explore](https://transport.data.gouv.fr/explore).

   ![Explore page of the French national access point to transport data](link-to-image)

   Or the Datenwaben project by Thomas Tursics. Doesn’t that give you ideas for projects using the underlying data and make it sound interesting?

   Terrible. Try to only publish the minimal metadata required and write factual, boring descriptions. If you can, avoid presenting examples of the data or how to use it at all cost. There are so many generic data sets out there, you can hide in the crowd.

### 2.5 In a Similar Vein: Include As Little Information As Possible
Some platforms, such as Kaggle, automatically give users a preview of the data that is contained in your data set. See for example this data set on Credit Card Fraud Detection.

![Useful visualization of data on Kaggle. This is the enemy.](link-to-image)

With the embedded preview of data and summaries of distributions for values in each column, it is really easy to judge if the data is appropriate to use. Because this reduces friction for the user, it will make it more likely that they actually use it. So make sure to avoid generating previews or summaries of your data.

3. **Make It Hard To Find**
   On a basic level, choosing short and non-descriptive names as well as minimal descriptions already make it hard for search engines to index your data sets.

   Additionally, you can try to hide your data by just not distributing it widely. Open data portals such as govdata.de often have well-done search functions or even APIs that can be used programmatically. That is a disaster of course, so make sure to create yet another data portal that only you use and publish only there.

4. **Use Uncommon or Hard-to-Use Formats**
   If you publish your data in easily usable formats such as CSV or JSON you have to accept the danger that users can access your data freely. You can try publishing in a format that requires commercial tools like XSL, but even those can be converted by most people nowadays. Best case, find a file format that is not machine-readable. PDFs are a popular choice, especially if you include some filler text such as headers or footers in addition to the data itself.

   ![The Federal Statistical Office of Germany foolishly offering a choice of common data formats to download](link-to-image)

### 4.5 Export Formatted for Humans
When you export tabular data, consider keeping the structure in a way that was originally designed for human readers. Include merged cells, fancy headers, and footnotes. If you export to CSV, add some pure text metadata such as copyright disclaimers to the file to break automated imports. If your users have to go through extensive cleaning and manual work before they can use your data they might give up.

5. **Ensure URLs 404**
   If you absolutely have to share your datasets on open data portals, make use of the fact that they often only hold the metadata and a backlink to your original source. Frequently restructure your data portal without setting up proper redirects and make sure the first thing excited users see is a 404 page (or better yet, a page explaining that your portal has a new structure and all data is somewhere else now). There is nothing better to frustrate potential users than squashing their interest after it is piqued.

### 5.5 Change Data After Publishing
Even if you cannot move the data somewhere else, you can still change it at the same URL without any versioning or notification. That way, when users download and use the data, they might get really confused when they try to re-run their software. Remember, a user that learned they need to re-download and re-validate your data constantly is a user that probably is not coming back.

### 6. Break Up Connected Datasets
Have a dataset that spans several years? Perfect. Split it into many individual files and do not connect them in an obvious way. Finding all the datasets and linking them is additional work for every user that makes the mistake of trying to use your data. Lucky for you, data scientists hate additional work.

This has the added benefit to hide the value of your data better. A potential user that just finds one of your datasets might assume it is not recent or extensive enough and leave you alone. Consider this dataset with football data since 1960. Doesn’t that immediately make you want to find out how the data changes over time? Imagine how much worse it could be if you would just publish it as one file for each year. With any luck, anyone would just stumble on the data for 1960, assume it is too old and not updated, and bother someone else.

**Stretch goal**: Spread data automatically to data portals but leave description and important context only on your website to make the data harder to use and seemingly of lower quality.

## Conclusion
These are the top tips for making sure no one cares about your open data, guaranteed to frustrate any potential users. Have I missed some? Let me know of other methods you have found that take the fun out of using open data.
