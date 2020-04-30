# machine-learning-challenge

  I used three different models for classification of an object as an exoplanet or not: a decision tree model, random forest model, and deep neural network model. The features I selected from the data set were:
  - koi_period: The time interval between planetary transits
  - koi_prad: The radius of the object
  - koi_fpflag_nt: A true/false flag for whether an object's light curve is consistent with a transiting planet
  - koi_steff: The temperature of the object's photosphere
  - koi_slogg: Acceleration due to gravity on the object's surface
  - koi_srad: The object's radius
 
 Out of the three machine learning models utilized, the random forrest classifier performed the best with an accuracy of 0.741 (the single decision tree classifier was close at 0.693) on testing data. The deep neural network did not perform as well (accuracy of 0.662) despite optimizing for batch size and epochs. The best model had an an accuracy higher than 2/3, which is substantially better than guessing between 4 potential classes. Given that some KOIs are designated as "candidates" (effectively uncategorized) and "not dispositioned" (tests results pending), it is possible that removal of these data points would create a more accurate model for classifying a KOI as an exoplanet or not. This is due to these classifications containing the "confirmed" and "false positive" classes as subclasses, which may confuse the model. While fitting the random forest model to a shortened dataset that precludes these data points does increase accuracy, it is hard to tell how much improvement is simply due to removing the number of potential classes. Improvements on this model could be made through searching through other exoplanet features in the dataset that have high importance, then remodeling the classifier using the features of highest importance. 
