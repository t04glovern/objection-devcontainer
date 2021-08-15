# Objection Exploration

## Objection DevContainer

```bash
docker build -t objection_docker .
docker run --privileged -it -v /dev/bus/usb:/dev/bus/usb objection_docker bash
```

## Decompile APK

```bash
mkdir decompiled && cd decompiled
jadx com.domain.app.apk -d ../decompiled/
```
