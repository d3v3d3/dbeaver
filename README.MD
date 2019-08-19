
# DBeaver

Insall XQuartz (using brew)
```BASH
brew cask install xquartz
```

Run XQuartz
```BASH
open -a XQuartz
```

Assure "Allow connections from network clients" is checked under XQuartz -> Preferences -> Security

Run DBeaver container:

```BASH
export DISPLAY=:0.0
xhost + 127.0.0.1
docker run --rm -d -e DISPLAY=host.docker.internal:0 -v /tmp/.X11-unix:/tmp/.X11-unix -v ${PWD}/.local:/root/.local d3v3d3/dbeaver
```