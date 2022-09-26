# Vital Flatpak

Run Vital Synth with Flatpak.

**Note**: I haven't done a whole lot of testing. The synth creates sound; that was the goal for now.
I haven't checked stuff like persistent data and permissions.

## Building and running

Grab the Debian installer from https://vital.audio/ and place it in the root of the repository.
The file should be named `VitalInstaller.deb`, rename if necessary.

Build the flatpak:
```console
flatpak-builder --force-clean build-dir audio.vital.Vital.yml
```

Now you can either run Vital directly...
```console
flatpak-builder --run build-dir audio.vital.Vital.yml /app/usr/bin/Vital
```

... or install the flatpak:
```console
flatpak-builder --force-clean --install audio.vital.Vital.yml
```
