import streamlit as st
import pygame
import pygame.movie

# Define the dimensions of the screen
WIDTH = 800
HEIGHT = 600

# Initialize Pygame
pygame.init()

# Create a Pygame video object
video = pygame.movie.Movie("path_to_video_file.mp4")  # Replace "path_to_video_file.mp4" with the actual path to your video file

# Start playing the video
video.play()

# Game loop
running = True
while running:
    for event in pygame.event.get():
        if event.type == pygame.QUIT:
            running = False

    # Draw the current video frame on the screen
    if video.get_busy():
        frame = video.get_surface()
        frame = pygame.transform.scale(frame, (WIDTH, HEIGHT))
        surface = pygame.surfarray.make_surface(frame)
        image_data = pygame.surfarray.array3d(surface)
        st.image(image_data)

# Stop the video playback and quit the program
video.stop()
pygame.quit()
