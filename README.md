Project3 - Supervised Integrated Video Streaming Application.

This school project involves the initialization of a VLC video stream from a bash script.
The stream shall be live via http protocol, and the quality must meet requirements for
regular HD with standard framerate(720p, 30 fps). This requires a minimum bitrate of 2500
kbps.

Along side the stream a TCPDUMP must be initiated for network observation.

The video stream script is now complete. The format is as the following:

<vlc> <input_stream> <--sout> <'#trancode{videocodec,audiocodec,vb,hq,ab}:standard{access,mux,dst}'>

vlc                   Triggers the VLC app.'

input_stream          The full path of video(s) to be streamed.

sout                  VLC Stream mode.

transcode             Transcodes the video and audio on the fly to best fit the stream and desired quality.

vcodec                vcodec: the new video codec. It can be one of mp4v (MPEG4), mpgv (MPEG1), DIV1, DIV2, DIV3 (DivX 1,2,3),      H263 (H263), I263 (H263I), WMV1 or WMV2 (Windows Media Video 1 or 2), MJPG (MJPEG), MJPB (MJPEGB).

acodec                acodec: the new audio codec. It can be one of mpga (MPEG audio layer 2), a52 or ac3 (AC3 sound) or vorb (Vorbis)

vb                    video bitrate in kbps(2500 minimum for 720p).

ab                    audio bitrate in Kbps(128 is standard).

hq                    high quality transcoding.

access                How the video shall be sent/streamed(in this case http).

mux                   Which format shall be used for video and audio.

dst                   Destination for stream(IP address:PORT).
