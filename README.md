# engine-on-container-socket-lost-test

Simple repo to reproduce https://github.com/balena-os/balena-engine/issues/282 :

* Deploy this to a Pi 3
* Start a console in the container
* See how, e.g., `balena ps` works normally.
* `SIGKILL` the Engine on the HostOS
* Engine (`balena ps` et alis) will no longer work on the container. (Even after
  the Engine automatically restarts on the HostOS).
