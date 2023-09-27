# Flatpak for GStreamer Debug Viewer

Viewer for GStreamer debug log files. For more information, please [visit the project website](https://gstreamer.freedesktop.org) or [view the source code](https://gitlab.freedesktop.org/gstreamer/gstreamer/-/tree/main/subprojects/gst-devtools/debug-viewer)

## Usage notes
A log can be produced using the `GST_DEBUG_FILE` environment variable:
```
GST_DEBUG_FILE=test.log GST_DEBUG=DEBUG gst-play-1.0 https://archive.org/download/BigBuckBunny_124/Content/big_buck_bunny_720p_surround.ogv
```

The log file can be opened via the command line using the flatpak option [`--file-forwarding`](https://docs.flatpak.org/en/latest/flatpak-command-reference.html#idm45858572528784):
```
flatpak run --file-forwarding org.freedesktop.GstDebugViewer @@ ./test.log @@
```