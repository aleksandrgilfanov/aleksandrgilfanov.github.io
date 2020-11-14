# My personal site [aleksandrgilfanov.github.io](https://aleksandrgilfanov.github.io)

Site built with using [Jekyll](https://jekyllrb.com).

Use docker to start web site from this repo locally.

1. Build site and cache dependencies into local directory:
```
docker run --rm \
	--volume="$PWD:/srv/jekyll" \
	--volume="$PWD/vendor/bundle:/usr/local/bundle" \
	-it jekyll/jekyll:3.8 \
	jekyll build
```

2. Start site on port 4000:
```
docker run --rm \
	--volume="$PWD:/srv/jekyll" \
	--volume="$PWD/vendor/bundle:/usr/local/bundle" \
	-p 4000:4000 \
	-it jekyll/jekyll:3.8 \
	jekyll serve
```

3. Go to [http://your-ip-address:4000](http://your-ip-address:4000) in browser.
