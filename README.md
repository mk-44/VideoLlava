#VideoLlava
VideoLlava is a model that allows the multi-modality between text, images and videos.
It allows us to ask questions from videos and text and provides great response.
The video-llava-implementation.ipynb file shows the entire archtitecture involved and loads weights from hugging-face.

Video-Llava performs well as the distribution space of image and video encoders are aligned, while training of video-encoder model.
This is done by using CLIP text encoder and aligning the video encoder output to it.
As the image encoder is already aligned to the text encoder, so as a result, both image and video encoder end up in same distribution space.
This alignment allows the Language Decoder model to learn only one distribution space [common for image and video embeddings] instead of learning 2 distributions.