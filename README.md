# Objection Exploration

## Objection DevContainer

```bash
docker build -t objection_docker .
docker run --privileged -it -v /dev/bus/usb:/dev/bus/usb objection_docker bash
```

## Decompile APK

Assumes the APK lives in the `apk` folder

```bash
mkdir decompiled && cd apk
jadx com.domain.app.apk -d ../decompiled/
```

## Notes

You might need to comment out the following in the `.devcontainer/devcontainer.json` if you are on a Mac

```json
	"mounts": [
		// Mount the host's device to this container's.
		"source=/dev/bus/usb,target=/dev/bus/usb,type=bind,consistency=consistent"
	]
```
