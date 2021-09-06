# HabitusDocker

This repository contains docker files needed for hosting Habitus Shiny app and
its dependencies.

1. Build app: `sudo docker build -t habitus-app .`

2. Run app and expose it to data volume on the host:

`sudo docker run --rm -v /home/vincent/projects/fontys:/srv/shiny-server/data -p 3838:3838 habitus-app`

3. Run app without exposing data: `sudo docker run --rm -p 3838:3838 habitus-app`

4. Open app in browser: `http://localhost:3838/`

5. Remove image: `sudo docker rmi habitus-app`

