# video-conv2
convert video sr
# Code for Video Converter using moviepy
from moviepy.editor import VideoFileClip

def convert_video_to_mp4(input_video_path, output_video_path):
    # Load the video clip
    video_clip = VideoFileClip(input_video_path)

    # Export as MP4
    video_clip.write_videofile(output_video_path, codec='libx264', audio_codec='aac')

    print(f"Conversion complete. MP4 file saved at {output_video_path}")

# Example usage
input_video_path = "input_video.avi"
output_video_path = "output_video.mp4"

convert_video_to_mp4(input_video_path, output_video_path)
