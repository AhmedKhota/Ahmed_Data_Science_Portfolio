This portfolio includes brief summaries of the work done in various projects for my PhD, with major methods and results highlighted. For further detail, please click on the titles of each project to see the full GitHub page of each which includes code. My PhD research involves the study of Non-linguistic utterances for social robots. These are non-speech sounds that are used in social robots to convey mood, and emotion and to communicate basic information. The most popular example of such a case is the fictional robot R2D2 from Star Wars. Since then, similar sounds have been implemented in real social robots with varying degrees of success. As social robots and devices in general become more prevalent in society, the need for non-speech, basic, quick, and distinguishable communication channels is highlighted. Non-linguistic utterances can go some way to addressing this need.

# [Creation of Non-Linguistic Utterances using Genetic Algorithm and Validation using Previously Trained Random Forest Model](https://github.com/AhmedKhota/GA-sound-generation)

Summary:

* Previously, a random forest model was trained to infer the valence and arousal of 560 Non-Linguistic Utterances (NLUs) sourced from popular movies, TV shows, and video games.
* The sounds were extracted from movies, TV shows, and video games manually.
* A Genetic Algorithm (GA) was used together with the Mido and MidiUTIL PyPI libraries to generate NLUs.
* A Neural Network (Multi-layer Perceptron) was trained using 3000 randomly synthesized sounds to infer the fitness of a genotype.
* Two layers of Batch Normalization and Dropout were implemented and reduced overfitting during the training process of the Neural Network.
* Using 10-fold cross-validation, the Neural Network was trained to evaluate the fitness of the genotypes and achieved an average Mean Absolute Error (MAE) of 0.136 on the normalized rating scale, and a correlation between actual and predicted values of 0.725. The results of the Neural Network training can be seen in the graph below. 
* The GA ran for thousands of generations and used the trained Neural Network to infer the fitness of the genotypes.
* The GA-generated sounds were tested and evaluated by human subjects, as well as the random forest model.
* Comparing the Valence and Arousal ratings from the human subjects and the inferences from the random forest model, the Mean Absolute Error was found to be 0.117 for Valence and 0.067 for Arousal. Correlation coefficients between experiment ratings and inferences were 0.22 for Valence and 0.63 for Arousal.
* The fittest sounds generated by the GA can be refined and implemented in a social robot for use in a commercial setting.

![](/images/NN2.png)

* The hexagon scatter plot below shows the GA-generated sounds inferred valence and arousal after 48000 'fit' individuals were generated over 2000 generations. It shows the regions of the Valence Arousal space explored by the algorithm.

![](/images/snapshot_4.png)

# [Valence Arousal Inference Model using Random Forest](https://github.com/AhmedKhota/Valence_Arousal_Inference)

Summary:

* Extracted 560 Non-Linguistic Utterances (sounds) from popular movies, TV shows, and video games. The sounds were extracted manually using Adobe Premiere Pro.
* Extracted audio features from the sounds. The audio features used were the openSMILE Lower-Level Descriptors, which when testing against other feature sets including PyAudioAnalysis and openSMILE Functionals, resulted in the best model performance.
* Carried out an experiment where human subjects rated the emotional valence and arousal of the sounds.
* Used the audio features and experiment ratings to train a random forest model to infer the valence and arousal of a Non-Linguistic Utterance sound.
* The model was able to infer the valence with a Mean Absolute Error (MAE) of 0.107 and arousal with an MAE of 0.097, which were both less than the difference between two adjacent points on the rating scale used in the original experiment.
* The correlation of predicted vs. actual ratings for valence was 0.63 and for arousal 0.75.

![](/images/pvsascatters.png)

# [Clustering and ANOVA for 2-dimensional data with sample weights](https://github.com/AhmedKhota/Clustering_and_ANOVA)

Summary:

* Using the previously trained random forest model, the valence and arousal of a set of sounds were inferred.
* The sounds were rated by subjects in an experiment for their suitability to four emotions: excited, tense, sad, and neutral.
* A clustering analysis was performed, using both Density-Based clustering and Kmeans clustering, to determine if meaningful clusters and differences naturally exist in the data, considering the subject ratings.
* Both DBSCAN and Kmeans found multiple clusters in the data, and using ANOVA, when considering the subject ratings, the differences between the clusters were meaningful at a significance level of p < 0.05.
* The clustering and ANOVA results showed that sounds with different valence and arousal corresponding to different emotions were interpreted differently from each other. This suggests that the system was able to present sounds to subjects that were suitable for a given emotion. The model will be used to develop an audio sample curation system to support the sound design process.

![](/images/clusterafsall.png)

# [A Transfer Learning Neural Network Model using InceptionV3 to infer (regression) the Valence or Arousal using Mel Spectrograms of sounds](https://github.com/AhmedKhota/Transfer_Learning_NN_MelSPecSounds)

Summary:

* A Transfer Learning Neural Network model to infer the Valence or Arousal of a sound based on its Mel Spectrogram. Using an existing neural network, the Inception V3 model, trained on image data.
* Keras was used to implement the transfer learning model.
* The Training results are shown in the graph below (for Valence):

![MelSPecLossGraph](/images/MelSPecLossGraph.png)

* The final loss value of 0.276 is within two adjacent rating points in the original experiment's seven-point rating scale.
* The transfer learning model was able to identify the valence and arousal of NLU sounds.
* This model could be used to infer the valence and arousal of untested NLU sounds, or possibly other non-speech sounds.
