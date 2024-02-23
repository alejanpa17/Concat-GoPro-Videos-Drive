# Concatenate GoPro Videos stored in your Google Drive
Tired of dealing with segmented videos from your action camera (GoPro) and spending too much time merging them, risking loss of quality? Concatenate your video files stored on Google Drive using a Colab Notebook script. Save time while maintaining video quality.
This script utilizes the FFmpeg concatenation script demuxer. For more information, refer to the [official documentation](https://ffmpeg.org/ffmpeg-formats.html#concat-1)

## Getting Started

### Prerequisites
- Google account
  
### Installation
1. Upload the file `join_videos.ipynb` to your Google Drive.
2. Open the file in Drive using Google Colab.
3. Configure the following lines of the Notebook:

- Change the path where your video files are stored:
```
%cd /content/gdrive/MyDrive/VIDEOS
```

- Add the name of the video files into mylist.txt:
```
!echo file "video_1.MOV" >  mylist.txt
!echo file "video_2.MOV" >> mylist.txt
...
!echo file "video_n.MOV" >> mylist.txt
```

- Modify the name of the output file:
```
!ffmpeg -f concat -i mylist.txt -c copy "output.mp4"
```


