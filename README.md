# HabitusDocker

This repository contains docker files needed for hosting Habitus Shiny app and
its dependencies.

1. Build app: `sudo docker build -t habitus-app .`

2. Run app and expose it to data volume on the host:

`sudo docker run --rm -v /home/vincent/projects/fontys:/srv/shiny-server/data -p 3838:3838 habitus-app`

(If you do `sudo docker run --rm -p 3838:3838 habitus-app` you would not expose the data to the app)

3. Open app in browser: `http://localhost:3838/`

4. Remove image: `sudo docker rmi habitus-app`

