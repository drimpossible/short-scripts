# Short Scripts

- Convert .m4a to .mp3 (adjust 256k to 320k or whatever bitrate)

```
find . -type f -name '*.m4a' -exec bash -c 'ffmpeg -i "$0" -ab 256k "${0/%m4a/mp3}"' '{}' \; 
find . -type f -name '*.m4a' -exec bash -c 'rm "$0"' '{}' \;
```
