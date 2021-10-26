This image now downloads phpBB 3.2 as part of the nginx build process and then copies the /var/www/forum directory into a volume called forum upon runtime. This volume persists between builds, so if your changes aren't being applied, this is probably why.

to run:

```bash
git clone https://github.com/ZHoob2004/rusefi-docker
cd ruesfi-docker
docker-compose build
docker-compose up
```

open a browser to http://localhost/forum