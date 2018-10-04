# Serving local files

imgproxy can process files from your local filesystem. To use this feature do the following:

1. Set `IMGPROXY_LOCAL_FILESYSTEM_ROOT` environment variable to your images directory path.
2. Use `local:///path/to/image.jpg` as the source image url.

### Example

Assume you want to process image that stored on your disc at `/path/to/project/images/logos/evil_martians.png`. Run imgproxy with `IMGPROXY_LOCAL_FILESYSTEM_ROOT` set to your images directory:

```bash
$ IMGPROXY_LOCAL_FILESYSTEM_ROOT=/path/to/project/images imgproxy
```

Then use path inside this directory as source url:

```
local:///logos/evil_martians.png
```

The URl for resizing this image to fit 300x200 will look like this:

```
http://imgproxy.example.com/insecure/fit/300/200/no/0/bG9jYWw6Ly8vbG9n/b3MvZXZpbF9tYXJ0/aWFucy5wbmc.jpg
```