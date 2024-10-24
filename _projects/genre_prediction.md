---
layout: page
title: Spotify Genre Prediction
description: Made with python, sklearn
img: assets/img/genre_cover.png
importance: 1
category: software
---

### Predicting song genre with Spotify Metadata

This project presents an AdaBoost model to predict the genre of music given Spotify song features. The model was able to achieve above .78 area under receiver-operating characteristic scores for all classes, and above .9 for more than half of the classes.

### Methodology

The data consists of 50000 data points, with 10 genres containing 5000 points each. A train-test split of 9:1, with the split calculated separately for each class.

The data was not fully numeric and had missing values, so data preparation was necessary. The artist name and track name features were converted into features that represented the length of the artist and track names. Additionally, a predictor was extracted from the track name that was 1 if the name included ‘feat.’ (meaning the song had a feature), and 0 if not. The key column was converted from strings of the root of the scale to a number (12 total, for the 12 tone scale system). The mode column was converted to two columns denoting major and minor, a 1-hot encoding of the original. The tempo column was missing several values, so these were set to 0 as this would allow these data points to be used. From my domain knowledge of music, tempo should be a good predictor of genre, so I set missing values to 0 so the model might learn that a 0-tempo has no correlation with genre, instead of an average tempo confusing the model.

Once numeric, all the data was normalized with 0-mean and unit variance. Dimensionality reduction using PCA was attempted, but showed poor separation of classes.

I used the SKlearn AdaBoost model, with decision tree classifiers, a max depth of 1, 2000 estimators. 2000 estimators might be excessive, though it proved to have good performance and computational resources were not a concern.

### Evaluation

The model performance is measured using AUROC as well as a confusion matrix.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/metrics.jpg" title="evaluation metrics" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

### Conclusions

AUROC was highest for Classical music. This correlates well with the instrumentation, as most other genres (besides anime) are either band music (Jazz, Alternative, Country, Blues, Rock) or electronic instrument music (Electronic, Rap, Hip-Hop). The confusion matrix illustrates how anime was mostly misclassified as Classical, though Classical had the highest true positive rate.

Additionally, with Rap and Hip-Hop having much overlap in terms of tradition, instrumentation, and artists, the model represented this closeness through their frequent confusion/misclassification.

Since the model generally represents confusion we might have on the human level of genre, it is a safe assessment that the model is an accurate predictor of genre, and it is probably near human-level performance.

The data did include features such as “key” which were represented in the western 12-tone system, which means the model is inherently western biased, and it should be explored how other tuning systems or diverse metrics might impact model performance. It is also worth scrutinizing how key was included but not time-signature.