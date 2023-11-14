# Automaticaly dublicate video on another language

# Problematics

This solution is designed to duplicate videos from the Russian language. The interest lies in the fact that the same content can be viewed in different languages, which certainly expands the audience of the author.

# Algorithm

![](https://i.imgur.com/RbkfcuZ.png)

# RUN

## 1) install all packets and libraries
```
!pip install pydub
!pip install faster-whisper
!pip install translate
!pip install gTTS
!pip install TTS
!pip install -U TTS
!pip install transformers==4.33
!pip install --upgrade deepspeed
!pip install moviepy
!pip install -U deep-translator
!apt install ffmpeg
!pip install spleeter
!pip install pypinyin
```
## 2) upload <a href="https://huggingface.co/coqui/XTTS-v2/tree/main">model</a>
```python
config = XttsConfig()
config.load_json("your/path/to/config.json")
model = Xtts.init_from_config(config)
model.load_checkpoint(config, checkpoint_dir="path/to/chechpoint/dir", use_deepspeed=True)

model.cuda()
```
## 3) upload your video and put your path
```python
video_file = 'path/to/your/mp4/file'
```
## 4) choose your voice: original(better, than google, but slower) or google(faster)
## 5.1) If you choose original voice, run all cells in "Some speakers + Music" tab
## 5.2) If you choose google voice, run all cells in "Google Speech" tab
## 5.3) If you choose one voice, run all cells in "One voice" tab
## 6) Download output.mp4 file

Here you are, thanks for watching our project)
