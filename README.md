# CNN-based Image Search
This project was inspired by pyimagesearch's [tutorial](https://www.pyimagesearch.com/2014/01/27/hobbits-and-histograms-a-how-to-guide-to-building-your-first-image-search-engine-in-python/) on building an image search engine by using the images' histogram as a feature vector and then measure the chi-squared distance between a given query image and the indexed database.

In the final project of Computer Vision Course, I reused CNN to creates a feature vector, which is then given to classification layers. After that, these features are used to compare and search.

## The algorithm
1) With `getFeatures.py`, use a ResNet50 model to extract a feature vector for each image and dump them to a file.
2) With `query.py`, extract the features of a given picture and send them to `tools/Search.py` to measure the euclidean distance between the query vector and the vectors on the dataset. Sort them and show the five closest results.

## How to use
To run this script first install the dependencies
```
pip install -r requirements.txt
```
Then drop your image database on an "images" folder and run `getFeatures.py` to index all the pictures.
