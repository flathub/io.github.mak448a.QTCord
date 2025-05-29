# Build instructions

Download flatpak-pip-generator
`curl -o flatpak-pip-generator https://raw.githubusercontent.com/flatpak/flatpak-builder-tools/master/pip/flatpak-pip-generator`

Do a `python3 flatpak-pip-generator --checker-data requests platformdirs, etc.` to generate a json file (keep this separate!).

`flatpak-builder build-dir io.github.mak448a.QTCord.yml`
`flatpak-builder --user --install --force-clean build-dir io.github.mak448a.QTCord.yml`

## Resources
https://docs.flatpak.org/en/latest/first-build.html
https://docs.flatpak.org/en/latest/sandbox-permissions.html
