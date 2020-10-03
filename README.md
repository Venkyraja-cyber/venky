import pafy 

print("---------------------YouTube Downloader--------------------")

# url of video 

url = input()

  

video = pafy.new(url) 

print("Available Resolutions...")

print()

streams = video.streams 

for i in streams: 

	print(i) 

print()

# get best resolution regardless of format 

best = video.getbest() 

  

print("Resolution: " + best.resolution, best.extension) 

print()

print("Downloading....")

print()

# Download the video 

best.download() 

print("Download completed...!!!")

print("-----------------------------------------------------------")
