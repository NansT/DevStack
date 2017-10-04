Cloud Infratructures - Practical project
Setting up a devlopment stack

Nans TURBET - nans.turbet@etud.univ-pau.fr

1) The web files (.php, .html, etc) needs to be on the physical machine in /var/www/html.
The BDS website in the archive bds.tar.gz has been tested and should work.

2) Create the images and launch the test environment
    docker-compose-run
This may take a few minutes, because a lot of downloads have to be completed.

3) In another terminal, launch the development environment
    docker run -it -e DISPLAY=$DISPLAY -v /var/www/html:/var/www/html -v /tmp/.X11-unix:/tmp/.X11-unix project_dev /bin/bash

4) Once in the development container, the source files can be found in /var/www/html and edited with gedit.
They can be accessed from firefox at <serverip>/<pathtofile>.
They can also be accessed from the physical machine at the same address or localhost/<path_to_file>.
