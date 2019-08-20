# simplem3u8
This is a simple m3u8 parser for Python &lt; v2.6

It returns a dictionary with all the available streams, with the available info about the resolution etc.

Currently supports only the following metatags:
* #EXT-X-MEDIA
* #EXT-X-STREAM-INF

It is easy to use it, like below.

```python
import sys
import simpleM3U8 as sm3u8

def main(argv):
    sm3u8Parser = sm3u8.parseHandler()

    f = open("filename.m3u8", "r")
    playlists = sm3u8Parser.parse(f.read())
    f.close()
    print playlists

if __name__ == "__main__":
	main(sys.argv[1:])
```

