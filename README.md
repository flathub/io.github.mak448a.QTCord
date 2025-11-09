# Build instructions

Download flatpak-pip-generator
`curl -o flatpak-pip-generator https://raw.githubusercontent.com/flatpak/flatpak-builder-tools/master/pip/flatpak-pip-generator`

Do a `python3 flatpak-pip-generator --checker-data requests platformdirs, etc.` to generate a json file (keep this separate!).

<s>
Do a `python3 flatpak-pip-generator requests platformdirs, etc.` to generate a json file (keep this separate!).
Manually add the below to each package. If not a whl file, remove the packagetype key.
```json
"x-checker-data": {
    "type": "pypi",
    "name": "idna",
    "packagetype": "bdist_wheel"
}
```
</s>


`flatpak-builder build-dir io.github.mak448a.QTCord.yml`
`flatpak-builder --user --install --force-clean build-dir io.github.mak448a.QTCord.yml`

## Resources
https://docs.flatpak.org/en/latest/first-build.html
https://docs.flatpak.org/en/latest/sandbox-permissions.html
