# batchglprocess
Use custom GLSL shaders to batch process a lot of images. It uses raylib to access openGL and render the screen, I might give it a GUI sometime with raygui too. It's intended for use on two video files, one representing the foreground and the other representing the background, with frames extracted as png format.
ideal command to convert a video to frames is:

 ffmpeg -i generic.mov -r [framerate] -f image2 [folder]%05d.png
where framerate is the framerate at which the frames will be generated, and folder is "in_fg" or "in_bg"

ideal command to convert frames to a video:
 ffmpeg -framerate 30 -i out/%05d.png video.MOV

I plan to make this more easy to use and powerful in the future, with more example shaders, and with a preprocessor to add the supporting GLSL functions to any input shader.
