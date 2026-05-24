# Indentificação
        INTEGRANTES	

        Gabriel Barros Albertini - 10419482
        Rafael de Menezes Ros - 10417954
        Vinicius Alves Marques - 10417880
        Felipe do Nascimento Fonseca - 10409389
# Síntese do conteúdo do arquivo
        Conversão do arquivo .avi para .mp4.
# Código
        # Instalar ffmpeg para conversão de vídeo
        import os

        input_video_path = "/content/runs/detect/predict/https___www.youtube.avi"
        output_video_path = "/content/runs/detect/predict/https___www.youtube.mp4"

        # Verificar se o arquivo de entrada existe
        if os.path.exists(input_video_path):
        print(f"Convertendo '{input_video_path}' para '{output_video_path}'...")
        # Usar ffmpeg para converter AVI para MP4
        !ffmpeg -i {input_video_path} -c:v libx264 -preset medium -crf 23 -c:a aac -b:a 128k {output_video_path}
        print("Conversão concluída.")
        if os.path.exists(output_video_path):
                print(f"Vídeo MP4 salvo em: {output_video_path}")
        else:
                print("Erro: O arquivo MP4 não foi criado.")
        else:
        print(f"Erro: Arquivo de vídeo de entrada não encontrado em '{input_video_path}'.")

# Resultado

                Convertendo '/content/runs/detect/predict/https___www.youtube.avi' para '/content/runs/detect/predict/https___www.youtube.mp4'...
        ffmpeg version 4.4.2-0ubuntu0.22.04.1 Copyright (c) 2000-2021 the FFmpeg developers
        built with gcc 11 (Ubuntu 11.2.0-19ubuntu1)
        configuration: --prefix=/usr --extra-version=0ubuntu0.22.04.1 --toolchain=hardened --libdir=/usr/lib/x86_64-linux-gnu --incdir=/usr/include/x86_64-linux-gnu --arch=amd64 --enable-gpl --disable-stripping --enable-gnutls --enable-ladspa --enable-libaom --enable-libass --enable-libbluray --enable-libbs2b --enable-libcaca --enable-libcdio --enable-libcodec2 --enable-libdav1d --enable-libflite --enable-libfontconfig --enable-libfreetype --enable-libfribidi --enable-libgme --enable-libgsm --enable-libjack --enable-libmp3lame --enable-libmysofa --enable-libopenjpeg --enable-libopenmpt --enable-libopus --enable-libpulse --enable-librabbitmq --enable-librubberband --enable-libshine --enable-libsnappy --enable-libsoxr --enable-libspeex --enable-libsrt --enable-libssh --enable-libtheora --enable-libtwolame --enable-libvidstab --enable-libvorbis --enable-libvpx --enable-libwebp --enable-libx265 --enable-libxml2 --enable-libxvid --enable-libzimg --enable-libzmq --enable-libzvbi --enable-lv2 --enable-omx --enable-openal --enable-opencl --enable-opengl --enable-sdl2 --enable-pocketsphinx --enable-librsvg --enable-libmfx --enable-libdc1394 --enable-libdrm --enable-libiec61883 --enable-chromaprint --enable-frei0r --enable-libx264 --enable-shared
        libavutil      56. 70.100 / 56. 70.100
        libavcodec     58.134.100 / 58.134.100
        libavformat    58. 76.100 / 58. 76.100
        libavdevice    58. 13.100 / 58. 13.100
        libavfilter     7.110.100 /  7.110.100
        libswscale      5.  9.100 /  5.  9.100
        libswresample   3.  9.100 /  3.  9.100
        libpostproc    55.  9.100 / 55.  9.100
        Input #0, avi, from '/content/runs/detect/predict/https___www.youtube.avi':
        Metadata:
        software        : Lavf59.27.100
        Duration: 00:00:11.83, start: 0.000000, bitrate: 36745 kb/s
        Stream #0:0: Video: mjpeg (Baseline) (MJPG / 0x47504A4D), yuvj420p(pc, bt470bg/unknown/unknown), 1920x1080, 36823 kb/s, 30 fps, 30 tbr, 30 tbn, 30 tbc
        Codec AVOption b (set bitrate (in bits/s)) specified for output file #0 (/content/runs/detect/predict/https___www.youtube.mp4) has not been used for any stream. The most likely reason is either wrong type (e.g. a video option with no video streams) or that it is a private option of some encoder which was not actually used for any stream.
        Stream mapping:
        Stream #0:0 -> #0:0 (mjpeg (native) -> h264 (libx264))
        Press [q] to stop, [?] for help
        [libx264 @ 0x59b2de2535c0] using cpu capabilities: MMX2 SSE2Fast SSSE3 SSE4.2 AVX FMA3 BMI2 AVX2 AVX512
        [libx264 @ 0x59b2de2535c0] profile High, level 4.0, 4:2:0, 8-bit
        [libx264 @ 0x59b2de2535c0] 264 - core 163 r3060 5db6aa6 - H.264/MPEG-4 AVC codec - Copyleft 2003-2021 - http://www.videolan.org/x264.html - options: cabac=1 ref=3 deblock=1:0:0 analyse=0x3:0x113 me=hex subme=7 psy=1 psy_rd=1.00:0.00 mixed_ref=1 me_range=16 chroma_me=1 trellis=1 8x8dct=1 cqm=0 deadzone=21,11 fast_pskip=1 chroma_qp_offset=-2 threads=3 lookahead_threads=1 sliced_threads=0 nr=0 decimate=1 interlaced=0 bluray_compat=0 constrained_intra=0 bframes=3 b_pyramid=2 b_adapt=1 b_bias=0 direct=1 weightb=1 open_gop=0 weightp=2 keyint=250 keyint_min=25 scenecut=40 intra_refresh=0 rc_lookahead=40 rc=crf mbtree=1 crf=23.0 qcomp=0.60 qpmin=0 qpmax=69 qpstep=4 ip_ratio=1.40 aq=1:1.00
        Output #0, mp4, to '/content/runs/detect/predict/https___www.youtube.mp4':
        Metadata:
        software        : Lavf59.27.100
        encoder         : Lavf58.76.100
        Stream #0:0: Video: h264 (avc1 / 0x31637661), yuvj420p(pc, bt470bg/unknown/unknown, progressive), 1920x1080, q=2-31, 30 fps, 15360 tbn
        Metadata:
        encoder         : Lavc58.134.100 libx264
        Side data:
        cpb: bitrate max/min/avg: 0/0/0 buffer size: 0 vbv_delay: N/A
        frame=  355 fps=4.2 q=-1.0 Lsize=   15478kB time=00:00:11.73 bitrate=10806.6kbits/s speed=0.14x    
        video:15474kB audio:0kB subtitle:0kB other streams:0kB global headers:0kB muxing overhead: 0.029410%
        [libx264 @ 0x59b2de2535c0] frame I:10    Avg QP:23.00  size: 56653
        [libx264 @ 0x59b2de2535c0] frame P:179   Avg QP:26.52  size: 51335
        [libx264 @ 0x59b2de2535c0] frame B:166   Avg QP:27.75  size: 36681
        [libx264 @ 0x59b2de2535c0] consecutive B-frames: 27.0% 25.4% 19.4% 28.2%
        [libx264 @ 0x59b2de2535c0] mb I  I16..4: 22.9% 74.0%  3.1%
        [libx264 @ 0x59b2de2535c0] mb P  I16..4: 14.3% 53.1%  2.6%  P16..4: 15.4%  6.7%  1.7%  0.0%  0.0%    skip: 6.3%
        [libx264 @ 0x59b2de2535c0] mb B  I16..4:  7.2% 21.1%  0.9%  B16..8: 29.9% 12.3%  2.2%  direct: 4.8%  skip:21.6%  L0:49.4% L1:40.6% BI: 9.9%
        [libx264 @ 0x59b2de2535c0] 8x8 transform intra:74.8% inter:82.6%
        [libx264 @ 0x59b2de2535c0] coded y,uvDC,uvAC intra: 51.6% 44.7% 2.7% inter: 31.8% 22.3% 0.5%
        [libx264 @ 0x59b2de2535c0] i16 v,h,dc,p: 25% 51%  7% 17%
        [libx264 @ 0x59b2de2535c0] i8 v,h,dc,ddl,ddr,vr,hd,vl,hu: 27% 34% 18%  3%  3%  4%  3%  4%  4%
        [libx264 @ 0x59b2de2535c0] i4 v,h,dc,ddl,ddr,vr,hd,vl,hu: 28% 33%  9%  4%  5%  7%  5%  5%  4%
        [libx264 @ 0x59b2de2535c0] i8c dc,h,v,p: 53% 27% 16%  3%
        [libx264 @ 0x59b2de2535c0] Weighted P-Frames: Y:11.7% UV:7.3%
        [libx264 @ 0x59b2de2535c0] ref P L0: 69.9% 18.7%  8.3%  2.8%  0.3%
        [libx264 @ 0x59b2de2535c0] ref B L0: 93.9%  5.3%  0.8%
        [libx264 @ 0x59b2de2535c0] ref B L1: 99.0%  1.0%
        [libx264 @ 0x59b2de2535c0] kb/s:10711.73
        Conversão concluída.
        Vídeo MP4 salvo em: /content/runs/detect/predict/https___www.youtube.mp4
