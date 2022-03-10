# OpenScan-ML
As with all the other topics, I do not really know, what I do. But I have been following the development in ML for quite some time and I see a lot of potential. Using the OpenScanCloud creates quite a huge pile of data and I see several ways of (semi-) automatically labeling the photos.
Including my own image sets, I have more then 5000 sets containing a total of more then 500k photos. Most of the sets have been created with one of the OpenScan devices, but there are other images sets too (manually or by drone). Some of the sets are very suitable for photogrammetry, some are totally unusable.

## First idea (taken from [reddit](https://www.reddit.com/r/OpenScan/comments/sjdq58/is_there_someone_with_experience_in_machine/):

![Image](https://i.redd.it/30dq9e3kskf81.jpg)

When it comes to photogrammetry, the quality of the output highly depends on the surface features of the object. You usually want a feature-rich surface on the object and a feature-less background. It would be amazing to have a tool to classify different areas of a photo as "good" and "bad"

My 'idea': Is it possible to train a ML algorithm on lets say 30x30 squares to detect whether the given area is feature-rich or feature-less?

The training data could be derived from existing failed and successful image sets. One image set typically contains 100+ photos, where each could be split into "good" and "bad" squares. On a successful reconstructed image set, the center area normally contains "good" squares. Whereas the corners contain only background and thus "bad" squares. On a failed image set, the center squares would also be considered "bad".

So, starting from the huge pile of images on my hard drives, there should be more than enough training data. But is this approach viable or totally stupid due to my lack of understanding of the underlying mathematics. If it somehow sounds promising, I might start categorizing the existing data at some point soon.
