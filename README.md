# android_build_gradle2.2
This is a Dockerfile for Android build projects.

## Included
* OpenJDK 8
* Gradle 2.2
* platform-tools，build-tools
* Android SDK (android-19、21、22、23、24)
* Android Support Libraries

## How to use
Build docker image
```
docker build -t jmcn/android_build_gradle2.2 .
```

Run docker image
```
docker run --rm \
	-v ~/project:/project \
    -v ~/.gradle:/root/.gradle \
    jmcn/android_build_gradle2.2:latest /bin/bash -c "cd /project;gradle assembleRelease";
```

> use `-v` to mount your `android project directory` and `gradle cache`
