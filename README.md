# Video-Induced Multi-modal Sentiment Analysis: Inferring Comment Opinion and Emotion Toward Micro Video

 This repository aims to share and provide public CAMV datasets which is a Dataset of Inferring the Comment Sentiment and Emotion with Micro Videos, offering free, open, and accessible data resources for scientists, researchers, and developers.

# Overview
The prosperity of micro video platforms has brought new topics to multimodal affective computation. The comments of a micro video convey different sentiments and emotions. Therefore, we propose a task to infer comment sentiment and emotion by understanding the context of the micro video. In light of this, we create a new dataset called CAMV (Comment Analysis with MicroVideo) to study this task, which includes more than 100k manually annotated comments. The key to the task is to construct the deep semantic correlation between video and comment. 
## Task
Existing multi-modal benchmarks on video include MOSI, CMU-MOSEI, and MELD. The video form in these benchmarks is monologue or dialogue. They take temporal images (e.g., facial expression, smile, and gaze), audio(e.g., tones, pauses, and voice pitch), and textual data transcribed from spoken words as a clue to infer the sentiment and emotion of the speaker.

With the development of the Internet we-media, micro video social platforms bring a new issue for multi-modal sentiment analysis and emotion recognition. People create micro videos to showcase their individuality and express their feeling about them with comments. Unlike current benchmarks, the comment texts convey different sentiments and emotions for the same micro-videos, and the semantics are not aligned between the video and comments. That makes the issue unique because we not only need to concern about the comment text but also consider the semantic information conveyed in micro videos.

The CAMV dataset is collected from the most popular micro video social media platform, TikTok, which includes both the micro videos and corresponding comments.
Similar to the existing benchmark, we provide two types of annotations: sentiment and emotion. The sentiment labels consist of Positive, Negative, and Neutral, respectively. It indicates the comment holds agreement, disagreement, or indifferent sentiment toward the content of the videos. As for the emotion labels, we adopt the widely-used Plutchik’s wheel of emotions strategy, which includes eight labels: Trust, Joy, Surprise, Anticipation, Disgust, Sadness, Anger, and Fear.


## Video Features
### Description

For the visual feature which extracted from video frames, we present them as tensor representations which saved as npy files for each micro video. First of all, we uniform all the micro videos at same frame rate of 25fps. Afterwards, we used FFmpeg to extract all video frames. Then, we utilize the I3D model to generate the temporal features of the micro videos with a window size of 16 frames and a step size of 8. We slide the window on the temporal axis and limit the max tensor length as 180. The feature dimension is 1024.

### Download

You can download Video Features from the following location:

- Google Drive:[Video Features Download Link](https://drive.google.com/file/d/1kZUSbQsCjnx1Q4OzDiX5JAH5OExG0HxF/view?usp=sharing)
- Baidu NetDisk:[Video Features Download Link](https://pan.baidu.com/s/19K-7D4cFrY0lkhuwEVU1pg?pwd=sykw) Extract code: sykw

## Comment Annotations

### Description

For the comment data, we organize them as JSON files. We save all comments data as a json file and assign unique keys as data pointer. And each comment records text, annotated label, related micro video and hashtag. We use three json file to split train, dev and test set.

### Download

You can download Comment Annotations from the following location:

- Google Drive:[Comment Annotations Download Link](https://drive.google.com/drive/folders/1H1qUc6UCYWdg6NK9n4BwqM5aCCVM5dcF?usp=sharing)
- Baidu NetDisk:[Comment Annotations Download Link](https://pan.baidu.com/s/19K-7D4cFrY0lkhuwEVU1pg?pwd=sykw) Extract code: sykw



## License

 Our code is open sourced under the MIT license. Our annotations are available under a CC BY-SA 4.0 license.

If you have any questions about this repository or the datasets, please contact us.

Thank you!
