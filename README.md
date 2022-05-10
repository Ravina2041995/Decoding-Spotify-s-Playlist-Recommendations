# Decoding-Spotify-s-Playlist-Recommendations
Online music streaming becomes the dominant medium for people to listen to their favorite songs, Spotify API allows users to pull-out the different songs attributes (spotipy python library).
Here, objective is to use machine learning algorithm to understand the working of Spotify's recommendation engine.

**Dataset**
The dataset has 13 features and 195 records
Independent Variables: loudness, duration, energy, mode, liveliness, speechiness, tempo, time_signature, valence, instrumentalness, key, danceability, acousticness
Target Variable: liked

**Exploratory Data Analysis**

-Songs in dataset has following attributes: 
-high dancebaility (how suitable the track is for dancing)
-highly energtic
-not acoustic
-mix of happy and sad songs
-has vocal content (not instrumental) 
-track is not live recorded.
-Users liked songs score high on danceability and energy
-Almost all the liked songs are not instrumental and hence is positively correlated with speechiness
-Most of the liked songs are loud
-User liked mix of happy and sad songs hence is not strongly correlated with Valence

**Approach**
Cross-validation Is Used To Evaluate Model Performance Since Dataset Is Small
Model Is Further Refined Using Grid Search CV!
Parameter Grid->Cross Validation->Best Parameter -> Data set (Pre processing) -> Training data -> Retained Model -> Test Data -> Final Evaluation

**5 Fold Cross-validationRandom Forest And Decision Tree Have Similar AUC Score**
KNN Output = 0.94
Logistic Regression Output = 0.97
Decision Tree Output = 0.82
Random Forest Output = 0.97

**Hyper-Parameter Tuning**
Random Forest Has Slight Improvement In Prediction Accuracy!

**Conclusion**

-The caveat of fewer records was overcome by using cross validation in determining the ML model giving better prediction
-Random Forest gives better prediction followed by Logistic Regression with f1 score of 93% and 92% respectively
-Random Forest and Logistic Regression were both refined using Grid search cross validation to improve prediction ability
-Instrumentalness followed by speechiness, danceabilty and duration were treated as high priority features while building classifier

**Appendix**
-Acousticness : A confidence measure from 0.0 to 1.0 of whether the track is acoustic. 1.0 represents high confidence the track is acoustic.
-Danceability : Danceability describes how suitable a track is for dancing based on a combination of musical elements including tempo, rhythm stability, beat strength, and overall regularity. A value of 0.0 is least danceable and 1.0 is most danceable.
-Duration_ms : The duration of the track in milliseconds.
-Energy : Energy is a measure from 0.0 to 1.0 and represents a perceptual measure of intensity and activity. 
-Instrumentalness : Predicts whether a track contains no vocals. The closer the instrumentalness value is to 1.0, the greater likelihood the track contains no vocal content.
-Key : The key the track is in. Integers map to pitches using standard Pitch Class notation . E.g. 0 = C, 1 = C♯/D♭, 2 = D, and so on.
-Liveness : Detects the presence of an audience in the recording. A value above 0.8 provides strong likelihood that the track is live
-Loudness : The overall loudness of a track in decibels (dB). Values typical range between -60 and 0 db.
-Mode : Mode indicates the modality (major or minor) of a track. Major is represented by 1 and minor is 0.
-Speechiness : Speechiness detects the presence of spoken words in a track. The more exclusively speech-like the recording (e.g. talk show, audio book, poetry), the closer to 1.0 the attribute value.
-Tempo : The overall estimated tempo of a track in beats per minute (BPM)
-Time_signature : An estimated overall time signature of a track (specifies how many beats are in each bar)
-Valence : A measure from 0.0 to 1.0 describing the musical positiveness conveyed by a track
-Liked : 1 for liked songs , 0 for disliked songs




