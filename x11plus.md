# X11server additions ("x11plus")

   - descended from **suchja/x11server**
   - `docker build -t x11plus -f Dockerfile_x11plus .`
   - look at docker inspect
   - `docker run -d --name display -e VNC_PASSWORD=newPW -e XFB_SCREEN=1280x800x24 -e XFB_SCREEN_DPI=150 -p 5500:5900 x11plus`
   - look at output of `docker network inspect` to get docker machine IP. eg: 172.17.0.2
      * (need Docker CE >= 17.06 for this)
   - connect with eg.: `vncviewer 172.17.0.2:5900`
