# importing packages
from pytube import YouTube
import os

# url input from user
yt = YouTube(
	str(input("Please enter the YouTube link you want to download to MP3: \n>> ")))

# extract only audio
video = yt.streams.filter(only_audio=True).first()

# check for destination to save file
print("Please enter the destination or leave blank for current directory")
destination = str(input(">> ")) or '.'

# download the file
outFile = video.download(output_path=destination)

# save the file
base, ext = os.path.splitext(outFile)
newFile = base + '.mp3'
os.rename(outFile, newFile)

# result of success
print(yt.title + " has been successfully downloaded.")
