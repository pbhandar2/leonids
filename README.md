# Update 22/10/2019

My personal website. 

Theme: https://github.com/renyuanz/leonids


## Quick setup

```
git clone https://github.com/renyuanz/leonids
cd leonids
jekyll server
```

Check out your awesome blog at `http://localhost:4000` and Cheers!

## Running with Docker

```
docker run --rm -it --volume=$PWD:/srv/jekyll -p 4000:4000 jekyll/jekyll:pages jekyll serve --watch --force_polling
