# Ahmed_Data_Science_Portfolio
A place to showcase my data science projects. These are made up of work done during my PhD studies where I needed to use machine learning methods to model the emotional meaning of non-linguistic sounds.

# [Creation of Non-Linguistic Utterances using Genetic Algorithm and Validation using Previously Trained Random Forest Model](https://github.com/AhmedKhota/GA-sound-generation)

Summary:

* Previously, a random forest model was trained to infer the valence and arousal of 560 Non-Linguistic Utterances (NLUs) sourced from popular movies, TV shows, and video games.
* A Genetic Algorithm was used together with the mido and midiUTIL PyPI libraries to generate NLUs.
* The generated sounds were tested and evaluated by human subjects, as well as the random forest model.
* Comparing the Valence and Arousal ratings from the human subjects and the inferences from the random forest model, the Mean Absolute Error was found to be 0.117 for Valence and 0.067 for Arousal. Correlation coefficients between experiment ratings and inferences were 0.22 for Valence and 0.63 for Arousal.

# [Valence Arousal Inference Model using Random Forest](https://github.com/AhmedKhota/Valence_Arousal_Inference)

Summary:

* Extracted 560 Non-Linguistic Utterances from popular movies, TV shows, and video games.
* Extracted audio features from the sounds.
* Carried out an experiment where human subjects rated the emotional valence and arousal of the sounds.
* Used the audio features and experiment ratings to train a random forest model to infer the valence and arousal of a Non-Linguistic Utterance sound.
* The model was able to infer the valence with a Mean Absolute Error (MAE) of 0.107 and arousal with an MAE of 0.097, which were both less than the difference between two adjacent points on the rating scale used in the original experiment.
* The correlation of predicted vs. actual ratings for valence was 0.63 and for arousal 0.75. 

