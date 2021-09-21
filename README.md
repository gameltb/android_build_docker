First, build the image:
```sh
docker build  -t android-build .
```

Then you can start up new instances with:
```sh
$ docker run -it --rm  --network none  -v $ANDROID_BUILD_TOP:/src android-build
> cd /src; source build/envsetup.sh
> lunch aosp_arm-eng
> m -j50
```
