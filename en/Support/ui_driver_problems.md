# UI Rendering/Driver Problems

## Windows: UI Rendering/Video Driver Issues {#opengl_troubleshooting}

If you experience UI rendering issues or video driver crashes on Windows, this may be caused by "flaky" OpenGL drivers. *QGroundControl* provides 3 shortcuts that you can use to start *QGroundControl* in "safer" video modes (try these in order):

- **QGroundControl:** QGC uses OpenGL graphics drivers directly.
- **GPU Compatibility Mode:** QGC uses ANGLE drivers, which implement OpenGL on top of DirectX.
- **GPU Safe Mode:** QGC uses a software rasterizer for the UI (this is very slow).