# Docker-in-Docker

For now, please ignore this.  I'm doing horrible things to the code so that I can stand up a simulated wifi environment, inside of a container, which includes containers as clients.  

We currently use a mix of OpenVSwitch, Docker, Guacamole, Apache2, and VMs to provide a hands-on environment for students.  Currently, this includes simulated wifi environments.  The drawback: it requires a dedicated VM for each environment (e.g., one for command-line wifi, one for WEP cracking, one for WPA cracking, and so on).  

This is my attempt at Docker-izing those environments so that multiple VMs are not required.  It relies heavily on the work of:

- Jérôme Petazzoni
- @jfrazelle
- @tianon

This project relies on actual Docker-in-Docker, not manage-Docker-containes-from-a-Docker-container.  The isolation from the host machine is actually a desired feature.

## Assumptions

- the host container will require the --privileged switch.

## Sources

- (forked from) https://github.com/jpetazzo/dind
- https://itnext.io/docker-in-docker-521958d34efd

