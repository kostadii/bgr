# bgr - Boot-time Graphics Renderer for QNX SDP 8

Licensing:
Before all, you will need a valid QNX SW license to use this. Thankfully, SDP8 non-commercial licenses are available if you register. (Thanks Blacberry folk!)
This project is aimed mostly as an example under GNU 3.0. 

This project is aiming:
* Make a minimalistic frame-buffer renderer under QNX using the Screen driver interfaces.
* Minimal footprint in dependencies - fast start
* Can be used to display a basic "Loading ..." screen until a proper graphics engine using EGL/OpenGLES or similar has loaded enough resources to take over.

Dependencies:
* Screen driver already running. (you should make use of 'waitfor /dev/screen' before starting. Otherwise bad things happen)
* Screen and display configuration files properly defined.
* imglib library and imglib conf file present and properly defined.
* freetype library present
* A freetype supported freetype. The default is the DejaVuSans.ttf that comes
* The usual support libraries - check current makefile -l / -L section for exact list

Runs on:
* The official Raspberry Pi 4 SDP8 image (aarch64le / QNX8.0)
* Should run on armv7 and/or QNX7.x, but not tested (no non-commercial licenses are available)
* Planning to test eventually on x86_64 / QNX8.0
