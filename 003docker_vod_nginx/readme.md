1. ubuntu
2. nginx
3. python3.x

`docker build -t vod-nginx .`

`docker run --rm -it -p 80:9999 -v g:/:/opt/drive-g vod-nginx /bin/bash`