#Disproportionately Common Crimes By Location in South Australia

##Purpose:

There are many reasons why a South Australian may want to know the most important crimes in their local area. These include, safety, confidence and house prices among others.  Similarly, South Australians may want to compare the important crimes between different locations in the state if they are relocating or deciding where to open a business. It may also be beneficial for police training and resource allocation to know this historical information about criminal activity. 

Lots of crimes are committed, but not all of them are important to know about nor do they impact how you view an area. There are some crime types that happen a lot in every location, so they are not useful for comparing regions in South Australia. For example property related crimes are the most common in almost every single location in this dataset. With this project we aim to provide users with an interactive graphic of the most important crimes by location. For the purposes of this study we define important crimes as the ones that are disproportionately common in a specific local. Therefore our intent is to remove the noise in South Australian crime data to provide the public with useful data to make them feel more comfortable in their community. 

##Method:

To rank the crimes based on their importance to a specific location, we used the term frequency inverse document frequency algorithm (TF-IDF). This algorithm was originally developed to determine which words are important in different documents. TF-IDF involves calculating the frequency of a word of interest in a text and then comparing that to how many of the texts in the corpus contain that word. By using this method, you can calculate which words are important based on their frequency without the very common words drowning out the most unique words. Therefore in most cases joining words do not rank very highly (like and), whilst for a sports text the word football may rank very highly. Similarly, we can use this technique to find out which crimes are disproportionately common in specific locations. 

To perform this analysis we used the crime mapper dataset and focused on the 2006 data because it was the most recent year that we could find the raw counts with which to calculate the term frequencies of each crime type in each location. Following this, we calculated the document frequencies by looking at how many locations contain at least one instance of each crime type. 

The crime mapper dataset maps crimes to local government areas (LGA), so we used some additional datasets in order to connect these LGAs to their corresponding Australian zip codes. By doing this, we were able to map our resulting dataset in an interactive dashboard where the TF-IDF disproportionately common crimes could be compared to the most frequent crimes by location. 

Furthermore, if you are interested in a specific crime type, you are able to filter the third map in our dashboard to show the frequency of your crime of interest by location in South Australia. This may be important if you are interested in finding out where the most motor vehicle related crimes or violent crimes occur. 

##Limitations:

This dataset only contains crimes that have been reported to or come to the attention of the police, so this does not mean that every crime that gets committed in a location is recorded. Additionally, some zips map to more than one local government area, so there are some locations that get more than one crime type assigned to them. With more time and work to deduplicate these mappings, this limitation could be improved. Further, there are some sub categories of crimes that could be grouped at different levels if more time was spent on this project. 

##Conclusion: 

The most disproportionately common types of crimes are different to the most frequent crimes in this dataset. By far, the most common crime by frequency is property related crime, whereas using TF-IDF a much more diverse range of important crimes are identified across different South Australian locations.

##Future Directions:

If more time was available we would have liked to include a temporal component in the dashboard and perhaps create an animated map showing the change in the most disproportionately common crimes by location over time, since there are several other years of data available. In addition, with more time multiple maps could be made to display greater detail about each sub-category of crime. This approach could be extended to work with more datasets, for example health, service utilisation, occupations etc.
