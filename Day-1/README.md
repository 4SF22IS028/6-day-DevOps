
-->What I Did
Installed and set up Docker on Windows.

Explored WSL integration and fixed errors related to Docker service not running.

Ran and troubleshooted the hello-world Docker container.

Installed Jenkins using jenkins.war.

Faced and resolved Java version conflicts (Java 8 vs Java 17).

Successfully ran Jenkins on a custom Java path without uninstalling Java 8.

Accessed Jenkins UI on http://localhost:8080 and confirmed installation.

-->Code & Commands Used for docker:

docker create ubuntu /bin/bash
docker p -a
docker start <containerid>
docker ps
docker ps -a
docker create -it --name webserver amazonlinux /bin/bash
docker ps -a
docker strat webserver
docker ps
docker exec -it webserver /bin/bash
ls
exit
docker run -it --name sample ubuntu /bin bash
docker ps
docker run -td --name web-app -p 3002

-->installed WSL versions
<pre><code> wsl -l -v </code></pre>
# Shutdown and unregister Docker WSL
<pre><code> wsl --shutdown wsl --unregister docker-desktop </code></pre>
# Run hello-world to test Docker
<pre><code> docker run hello-world </code></pre>
># Run Jenkins using specific Java version (without changing system Java) 
<pre><code"C:\Path\To\Java17\bin\java.exe" -jar jenkins.war </code></pre>

Key Learnings:

WSL plays a crucial role in Docker on Windows.

Multiple Java versions can coexist and be used selectively.

Jenkins requires Java 11+, but can be run without changing the default Java version.

How to verify installations using commands and browser access.
