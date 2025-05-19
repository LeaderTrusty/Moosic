# Moosic
Unsupervised ML - Clustering Songs
Welcome to Moosic!

Moosic is a little start-up that creates playlists curated by music experts and specialists in old and new trends. Users can subscribe to their website and listen to these playlists through their preferred Music App (be it Spotify, Apple Music, Youtube Music…). They love the fact that their playlists have a personal touch, and that each playlist encapsulates a certain “mood” or “style”.
Business is scaling up fast and the music experts are slow in creating new playlists. They have hired you with a clear mission: use Data Science to add a degree of automatisation to the creation of playlists.

They want you to use a dataset that has been collected from the Spotify API and contains the audio features (tempo, energy, danceability…) for a few thousand songs and use a basic clustering algorithm such as K-Means to divide the dataset into a few clusters (which will become playlists).


Either way, in this first iteration of the project they expect you to have an initial prototype. No pressure: the playlists don’t have to be perfect, and the company understands that they are at the beginning of a lengthy process. Between you and the musical experts, a couple of assessments will have to be made:

Are Spotify’s audio features able to identify “similar songs”, as defined by humanly detectable criteria? When you listen to two rock ballads, two operas or two drum & bass songs, you identify them as similar songs. Are these similarities detectable using the audio features from Spotify?
Is K-Means a good method to create playlists? Would you stick with this algorithm moving forward, or explore other methods to create playlists?
By the end of this project, you are expected to present your clusters to the team and discuss these questions with them.
For this project we’ll be using data from Spotify. Here’s the first dataset of 10 songs.

The data that you will use in order to group songs are Spotify’s audio features. Obviously, then, the playlists that will emerge from the clustering algorithm that you will apply are going to be completely determined by whatever information these audio features capture from a song.


Start by reading the descriptions that Spotify provides about its audio features. You will see how some of these measures are well-established musical properties (key, mode, tempo…) while others have been created by Spotify’s team of Data Science and Sound Engineering (danceability, energy, valence…).

**acousticness**
A confidence measure from 0.0 to 1.0 of whether the track is acoustic. 1.0 represents high confidence the track is acoustic.	Float

**danceability**

Danceability describes how suitable a track is for dancing based on a combination of musical elements including tempo, rhythm stability, beat strength, and overall regularity. A value of 0.0 is least danceable and 1.0 is most danceable.	Float

**duration_ms**

The duration of the track in milliseconds.	Integer

**energy**

Energy is a measure from 0.0 to 1.0 and represents a perceptual measure of intensity and activity. Typically, energetic tracks feel fast, loud, and noisy. For example, death metal has high energy, while a Bach prelude scores low on the scale. Perceptual features contributing to this attribute include dynamic range, perceived loudness, timbre, onset rate, and general entropy.	Float

**instrumentalness**

Predicts whether a track contains no vocals. “Ooh” and “aah” sounds are treated as instrumental in this context. Rap or spoken word tracks are clearly “vocal”. The closer the instrumentalness value is to 1.0, the greater likelihood the track contains no vocal content. Values above 0.5 are intended to represent instrumental tracks, but confidence is higher as the value approaches 1.0.	Float

**key**

The key the track is in. Integers map to pitches using standard Pitch Class notation . E.g. 0 = C, 1 = C♯/D♭, 2 = D, and so on.	Integer

**liveness**

Detects the presence of an audience in the recording. Higher liveness values represent an increased probability that the track was performed live. A value above 0.8 provides strong likelihood that the track is live.	Float

**loudness**

The overall loudness of a track in decibels (dB). Loudness values are averaged across the entire track and are useful for comparing relative loudness of tracks. Loudness is the quality of a sound that is the primary psychological correlate of physical strength (amplitude). Values typically range between -60 and 0 db.	Float

**mode**

Mode indicates the modality (major or minor) of a track, the type of scale from which its melodic content is derived. Major is represented by 1 and minor is 0.	Integer

**speechiness**

Speechiness detects the presence of spoken words in a track. The more exclusively speech-like the recording (e.g. talk show, audio book, poetry), the closer to 1.0 the attribute value. Values above 0.66 describe tracks that are probably made entirely of spoken words. Values between 0.33 and 0.66 describe tracks that may contain both music and speech, either in sections or layered, including such cases as rap music. Values below 0.33 most likely represent music and other non-speech-like tracks.	Float

**tempo**

The overall estimated tempo of a track in beats per minute (BPM). In musical terminology, tempo is the speed or pace of a given piece and derives directly from the average beat duration.	Float

**time_signature**

An estimated overall time signature of a track. The time signature (meter) is a notational convention to specify how many beats are in each bar (or measure).	Integer

**valence**

A measure from 0.0 to 1.0 describing the musical positiveness conveyed by a track. Tracks with high valence sound more positive (e.g. happy, cheerful, euphoric), while tracks with low valence sound more negative (e.g. sad, depressed, angry).	Float


