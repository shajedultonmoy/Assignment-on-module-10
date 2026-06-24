#Commands:

ubuntu@ip-10-0-3-165:~$ sudo apt install -y docker.io
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
The following additional packages will be installed:
  bridge-utils containerd dns-root-data dnsmasq-base pigz runc ubuntu-fan
Suggested packages:
  ifupdown aufs-tools cgroupfs-mount | cgroup-lite debootstrap docker-buildx docker-compose-v2 docker-doc rinse zfs-fuse | zfsutils
The following NEW packages will be installed:
  bridge-utils containerd dns-root-data dnsmasq-base docker.io pigz runc ubuntu-fan
0 upgraded, 8 newly installed, 0 to remove and 12 not upgraded.
Need to get 73.8 MB of archives.
After this operation, 279 MB of additional disk space will be used.
Get:1 http://us-east-1.ec2.archive.ubuntu.com/ubuntu noble/universe amd64 pigz amd64 2.8-1 [65.6 kB]
Get:2 http://us-east-1.ec2.archive.ubuntu.com/ubuntu noble/main amd64 bridge-utils amd64 1.7.1-1ubuntu2 [33.9 kB]
Get:3 http://us-east-1.ec2.archive.ubuntu.com/ubuntu noble-updates/main amd64 runc amd64 1.3.4-0ubuntu1~24.04.1 [9574 kB]
Get:4 http://us-east-1.ec2.archive.ubuntu.com/ubuntu noble-updates/main amd64 containerd amd64 2.2.1-0ubuntu1~24.04.2 [28.1 MB]
Get:5 http://us-east-1.ec2.archive.ubuntu.com/ubuntu noble-updates/main amd64 dns-root-data all 2024071801~ubuntu0.24.04.1 [5918 B]
Get:6 http://us-east-1.ec2.archive.ubuntu.com/ubuntu noble-updates/main amd64 dnsmasq-base amd64 2.90-2ubuntu0.3 [376 kB]
Get:7 http://us-east-1.ec2.archive.ubuntu.com/ubuntu noble-updates/universe amd64 docker.io amd64 29.1.3-0ubuntu3~24.04.2 [35.6 MB]
Get:8 http://us-east-1.ec2.archive.ubuntu.com/ubuntu noble-updates/universe amd64 ubuntu-fan all 0.12.16+24.04.1 [34.2 kB]
Fetched 73.8 MB in 1s (84.5 MB/s)     
Preconfiguring packages ...
Selecting previously unselected package pigz.
(Reading database ... 72608 files and directories currently installed.)
Preparing to unpack .../0-pigz_2.8-1_amd64.deb ...
Unpacking pigz (2.8-1) ...
Selecting previously unselected package bridge-utils.
Preparing to unpack .../1-bridge-utils_1.7.1-1ubuntu2_amd64.deb ...
Unpacking bridge-utils (1.7.1-1ubuntu2) ...
Selecting previously unselected package runc.
Preparing to unpack .../2-runc_1.3.4-0ubuntu1~24.04.1_amd64.deb ...
Unpacking runc (1.3.4-0ubuntu1~24.04.1) ...
Selecting previously unselected package containerd.
Preparing to unpack .../3-containerd_2.2.1-0ubuntu1~24.04.2_amd64.deb ...
Unpacking containerd (2.2.1-0ubuntu1~24.04.2) ...
Selecting previously unselected package dns-root-data.
Preparing to unpack .../4-dns-root-data_2024071801~ubuntu0.24.04.1_all.deb ...
Unpacking dns-root-data (2024071801~ubuntu0.24.04.1) ...
Selecting previously unselected package dnsmasq-base.
Preparing to unpack .../5-dnsmasq-base_2.90-2ubuntu0.3_amd64.deb ...
Unpacking dnsmasq-base (2.90-2ubuntu0.3) ...
Selecting previously unselected package docker.io.
Preparing to unpack .../6-docker.io_29.1.3-0ubuntu3~24.04.2_amd64.deb ...
Unpacking docker.io (29.1.3-0ubuntu3~24.04.2) ...
Selecting previously unselected package ubuntu-fan.
Preparing to unpack .../7-ubuntu-fan_0.12.16+24.04.1_all.deb ...
Unpacking ubuntu-fan (0.12.16+24.04.1) ...
Setting up dnsmasq-base (2.90-2ubuntu0.3) ...
Setting up runc (1.3.4-0ubuntu1~24.04.1) ...
Setting up dns-root-data (2024071801~ubuntu0.24.04.1) ...
Setting up bridge-utils (1.7.1-1ubuntu2) ...
Setting up pigz (2.8-1) ...
Setting up containerd (2.2.1-0ubuntu1~24.04.2) ...
Created symlink /etc/systemd/system/multi-user.target.wants/containerd.service → /usr/lib/systemd/system/containerd.service.
Setting up ubuntu-fan (0.12.16+24.04.1) ...
Created symlink /etc/systemd/system/multi-user.target.wants/ubuntu-fan.service → /usr/lib/systemd/system/ubuntu-fan.service.
Setting up docker.io (29.1.3-0ubuntu3~24.04.2) ...
info: Selecting GID from range 100 to 999 ...
info: Adding group `docker' (GID 113) ...
Created symlink /etc/systemd/system/multi-user.target.wants/docker.service → /usr/lib/systemd/system/docker.service.
Created symlink /etc/systemd/system/sockets.target.wants/docker.socket → /usr/lib/systemd/system/docker.socket.
Processing triggers for dbus (1.14.10-4ubuntu4.1) ...
Processing triggers for man-db (2.12.0-4build2) ...
Scanning processes...                                                                                                                                              
Scanning linux images...                                                                                                                                           

Running kernel seems to be up-to-date.

No services need to be restarted.

No containers need to be restarted.

No user sessions are running outdated binaries.

No VM guests are running outdated hypervisor (qemu) binaries on this host.
ubuntu@ip-10-0-3-165:~$ sudo systemctl enable docker
ubuntu@ip-10-0-3-165:~$ sudo systemctl start docker
ubuntu@ip-10-0-3-165:~$ docker --version
Docker version 29.1.3, build 29.1.3-0ubuntu3~24.04.2
ubuntu@ip-10-0-3-165:~$ 

ubuntu@ip-10-0-3-165:~$ sudo apt install docker-compose-plugin -y
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
E: Unable to locate package docker-compose-plugin
ubuntu@ip-10-0-3-165:~$ docker compose version
docker: unknown command: docker compose

Run 'docker --help' for more information
ubuntu@ip-10-0-3-165:~$ sudo apt install docker-compose -y
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
The following additional packages will be installed:
  python3-compose python3-docker python3-dockerpty python3-docopt python3-dotenv python3-texttable python3-websocket
The following NEW packages will be installed:
  docker-compose python3-compose python3-docker python3-dockerpty python3-docopt python3-dotenv python3-texttable python3-websocket
0 upgraded, 8 newly installed, 0 to remove and 12 not upgraded.
Need to get 297 kB of archives.
After this operation, 1589 kB of additional disk space will be used.
Get:1 http://us-east-1.ec2.archive.ubuntu.com/ubuntu noble/universe amd64 python3-websocket all 1.7.0-1 [38.1 kB]
Get:2 http://us-east-1.ec2.archive.ubuntu.com/ubuntu noble-updates/universe amd64 python3-docker all 5.0.3-1ubuntu1.1 [89.1 kB]
Get:3 http://us-east-1.ec2.archive.ubuntu.com/ubuntu noble/universe amd64 python3-dockerpty all 0.4.1-5 [11.4 kB]
Get:4 http://us-east-1.ec2.archive.ubuntu.com/ubuntu noble/universe amd64 python3-docopt all 0.6.2-6 [26.1 kB]
Get:5 http://us-east-1.ec2.archive.ubuntu.com/ubuntu noble/universe amd64 python3-dotenv all 1.0.1-1 [22.3 kB]
Get:6 http://us-east-1.ec2.archive.ubuntu.com/ubuntu noble/universe amd64 python3-texttable all 1.6.7-1 [11.0 kB]
Get:7 http://us-east-1.ec2.archive.ubuntu.com/ubuntu noble/universe amd64 python3-compose all 1.29.2-6ubuntu1 [84.6 kB]
Get:8 http://us-east-1.ec2.archive.ubuntu.com/ubuntu noble/universe amd64 docker-compose all 1.29.2-6ubuntu1 [14.0 kB]
Fetched 297 kB in 0s (9881 kB/s)         
Selecting previously unselected package python3-websocket.
(Reading database ... 72980 files and directories currently installed.)
Preparing to unpack .../0-python3-websocket_1.7.0-1_all.deb ...
Unpacking python3-websocket (1.7.0-1) ...
Selecting previously unselected package python3-docker.
Preparing to unpack .../1-python3-docker_5.0.3-1ubuntu1.1_all.deb ...
Unpacking python3-docker (5.0.3-1ubuntu1.1) ...
Selecting previously unselected package python3-dockerpty.
Preparing to unpack .../2-python3-dockerpty_0.4.1-5_all.deb ...
Unpacking python3-dockerpty (0.4.1-5) ...
Selecting previously unselected package python3-docopt.
Preparing to unpack .../3-python3-docopt_0.6.2-6_all.deb ...
Unpacking python3-docopt (0.6.2-6) ...
Selecting previously unselected package python3-dotenv.
Preparing to unpack .../4-python3-dotenv_1.0.1-1_all.deb ...
Unpacking python3-dotenv (1.0.1-1) ...
Selecting previously unselected package python3-texttable.
Preparing to unpack .../5-python3-texttable_1.6.7-1_all.deb ...
Unpacking python3-texttable (1.6.7-1) ...
Selecting previously unselected package python3-compose.
Preparing to unpack .../6-python3-compose_1.29.2-6ubuntu1_all.deb ...
Unpacking python3-compose (1.29.2-6ubuntu1) ...
Selecting previously unselected package docker-compose.
Preparing to unpack .../7-docker-compose_1.29.2-6ubuntu1_all.deb ...
Unpacking docker-compose (1.29.2-6ubuntu1) ...
Setting up python3-dotenv (1.0.1-1) ...
Setting up python3-texttable (1.6.7-1) ...
Setting up python3-docopt (0.6.2-6) ...
Setting up python3-websocket (1.7.0-1) ...
Setting up python3-dockerpty (0.4.1-5) ...
Setting up python3-docker (5.0.3-1ubuntu1.1) ...
Setting up python3-compose (1.29.2-6ubuntu1) ...
Setting up docker-compose (1.29.2-6ubuntu1) ...
Processing triggers for man-db (2.12.0-4build2) ...
Scanning processes...                                                                                                                                              
Scanning linux images...                                                                                                                                           

Running kernel seems to be up-to-date.

No services need to be restarted.

No containers need to be restarted.

No user sessions are running outdated binaries.

No VM guests are running outdated hypervisor (qemu) binaries on this host.
ubuntu@ip-10-0-3-165:~$ docker compose version
docker: unknown command: docker compose

Run 'docker --help' for more information
ubuntu@ip-10-0-3-165:~$ docker-compose --version
docker-compose version 1.29.2, build unknown
ubuntu@ip-10-0-3-165:~$ 

ubuntu@ip-10-0-3-165:~$ git clone https://github.com/roy35-909/Module-3-deployment.git
Cloning into 'Module-3-deployment'...
remote: Enumerating objects: 211, done.
remote: Counting objects: 100% (211/211), done.
remote: Compressing objects: 100% (99/99), done.
remote: Total 211 (delta 79), reused 195 (delta 63), pack-reused 0 (from 0)
Receiving objects: 100% (211/211), 53.12 KiB | 1.83 MiB/s, done.
Resolving deltas: 100% (79/79), done.
ubuntu@ip-10-0-3-165:~$ cd Module-3-deployment
ubuntu@ip-10-0-3-165:~/Module-3-deployment$ ls -la
total 160
drwxrwxr-x 6 ubuntu ubuntu  4096 Jun 24 08:01 .
drwxr-x--- 5 ubuntu ubuntu  4096 Jun 24 08:01 ..
drwxrwxr-x 8 ubuntu ubuntu  4096 Jun 24 08:01 .git
drwxrwxr-x 3 ubuntu ubuntu  4096 Jun 24 08:01 .github
-rw-rw-r-- 1 ubuntu ubuntu   289 Jun 24 08:01 .gitignore
-rw-rw-r-- 1 ubuntu ubuntu   162 Jun 24 08:01 Dockerfile
-rw-rw-r-- 1 ubuntu ubuntu  1822 Jun 24 08:01 Jenkinsfile
-rw-rw-r-- 1 ubuntu ubuntu   834 Jun 24 08:01 README.md
-rw-rw-r-- 1 ubuntu ubuntu   767 Jun 24 08:01 eslint.config.js
-rw-rw-r-- 1 ubuntu ubuntu   380 Jun 24 08:01 index.html
-rw-rw-r-- 1 ubuntu ubuntu 78617 Jun 24 08:01 package-lock.json
-rw-rw-r-- 1 ubuntu ubuntu   377 Jun 24 08:01 package.json
-rw-rw-r-- 1 ubuntu ubuntu    87 Jun 24 08:01 postcss.config.js
drwxrwxr-x 3 ubuntu ubuntu  4096 Jun 24 08:01 src
-rw-rw-r-- 1 ubuntu ubuntu  5562 Jun 24 08:01 tailwind.config.js
drwxrwxr-x 2 ubuntu ubuntu  4096 Jun 24 08:01 test
-rw-rw-r-- 1 ubuntu ubuntu   576 Jun 24 08:01 tsconfig.app.json
-rw-rw-r-- 1 ubuntu ubuntu   126 Jun 24 08:01 tsconfig.json
-rw-rw-r-- 1 ubuntu ubuntu   501 Jun 24 08:01 tsconfig.node.json
-rw-rw-r-- 1 ubuntu ubuntu   230 Jun 24 08:01 vite.config.ts
ubuntu@ip-10-0-3-165:~/Module-3-deployment$ cat package.json
{
  "name": "node-express-app",
  "version": "1.0.0",

  "scripts": {
    "start": "node src/server.js",
    "check": "mocha test/**/*.test.js",
    "dev": "node src/server.js"
  },
  "dependencies": {
    "express": "^4.18.3"
  },
  "devDependencies": {
    "chai": "^4.5.0",
    "chai-http": "^4.4.0",
    "mocha": "^10.3.0",
    "supertest": "^6.3.4"
  }
}ubuntu@ip-10-0-3-165:~/Module-3-deployment$ nano Dockerfile
ubuntu@ip-10-0-3-165:~/Module-3-deployment$ 

ubuntu@ip-10-0-3-165:~/Module-3-deployment$ docker build -t express-app .
DEPRECATED: The legacy builder is deprecated and will be removed in a future release.
            Install the buildx component to build images with BuildKit:
            https://docs.docker.com/go/buildx/

permission denied while trying to connect to the docker API at unix:///var/run/docker.sock
ubuntu@ip-10-0-3-165:~/Module-3-deployment$ docker run -d -p 3000:3000 express-app
permission denied while trying to connect to the docker API at unix:///var/run/docker.sock
ubuntu@ip-10-0-3-165:~/Module-3-deployment$ newgrp docker
Password: 
Invalid password.
ubuntu@ip-10-0-3-165:~/Module-3-deployment$ docker build -t express-app .
DEPRECATED: The legacy builder is deprecated and will be removed in a future release.
            Install the buildx component to build images with BuildKit:
            https://docs.docker.com/go/buildx/

time="2026-06-24T08:06:27Z" level=error msg="Can't add file /home/ubuntu/Module-3-deployment/.git to tar: io: read/write on closed pipe"
time="2026-06-24T08:06:27Z" level=error msg="Can't close tar writer: io: read/write on closed pipe"
permission denied while trying to connect to the docker API at unix:///var/run/docker.sock
ubuntu@ip-10-0-3-165:~/Module-3-deployment$ sudo docker build -t express-app .
DEPRECATED: The legacy builder is deprecated and will be removed in a future release.
            Install the buildx component to build images with BuildKit:
            https://docs.docker.com/go/buildx/

Sending build context to Docker daemon  242.7kB
Step 1/7 : FROM node:20-alpine
20-alpine: Pulling from library/node
fff4e2c1b189: Pulling fs layer
4feea04c1543: Pulling fs layer
6a0ac1617861: Pulling fs layer
b2cbbfe903b0: Pulling fs layer
0f92261bcd1c: Download complete
fff4e2c1b189: Download complete
b2cbbfe903b0: Download complete
14f8540414db: Download complete
6a0ac1617861: Download complete
6a0ac1617861: Pull complete
4feea04c1543: Download complete
4feea04c1543: Pull complete
fff4e2c1b189: Pull complete
b2cbbfe903b0: Pull complete
Digest: sha256:fb4cd12c85ee03686f6af5362a0b0d56d50c58a04632e6c0fb8363f609372293
Status: Downloaded newer image for node:20-alpine
 ---> fb4cd12c85ee
Step 2/7 : WORKDIR /app
 ---> Running in ca16708d7fb8
 ---> Removed intermediate container ca16708d7fb8
 ---> aa275acc3618
Step 3/7 : COPY package*.json ./
 ---> e1bd3df0181b
Step 4/7 : RUN npm install
 ---> Running in 53851dff1814
npm warn deprecated inflight@1.0.6: This module is not supported, and leaks memory. Do not use it. Check out lru-cache if you want a good and tested way to coalesce async requests by a key value, which is much more comprehensive and powerful.
npm warn deprecated glob@8.1.0: Glob versions prior to v9 are no longer supported
npm warn deprecated superagent@8.1.2: Please upgrade to v9.0.0+ as we have fixed a public vulnerability with formidable dependency. Note that v9.0.0+ requires Node.js v14.18.0+. See https://github.com/ladjs/superagent/pull/1800 for insight. This project is supported and maintained by the team at Forward Email @ https://forwardemail.net

added 187 packages, and audited 188 packages in 4s

37 packages are looking for funding
  run `npm fund` for details

13 vulnerabilities (2 low, 5 moderate, 5 high, 1 critical)

To address issues that do not require attention, run:
  npm audit fix

To address all issues (including breaking changes), run:
  npm audit fix --force

Run `npm audit` for details.
npm notice
npm notice New major version of npm available! 10.8.2 -> 11.17.0
npm notice Changelog: https://github.com/npm/cli/releases/tag/v11.17.0
npm notice To update run: npm install -g npm@11.17.0
npm notice
 ---> Removed intermediate container 53851dff1814
 ---> f43578f0a189
Step 5/7 : COPY . .
 ---> 233c2794a1b7
Step 6/7 : EXPOSE 3000
 ---> Running in 52fcac733913
 ---> Removed intermediate container 52fcac733913
 ---> 65f03c87bc81
Step 7/7 : CMD ["npm","start"]
 ---> Running in c16b1823c158
 ---> Removed intermediate container c16b1823c158
 ---> 025ff131e7e3
Successfully built 025ff131e7e3
Successfully tagged express-app:latest
ubuntu@ip-10-0-3-165:~/Module-3-deployment$ sudo docker tag express-app yourdockerhubusername/express-app:latest
ubuntu@ip-10-0-3-165:~/Module-3-deployment$ sudo docker login

USING WEB-BASED LOGIN

i Info → To sign in with credentials on the command line, use 'docker login -u <username>'
         

Your one-time device confirmation code is: VTQP-WNSW
Press ENTER to open your browser or submit your device code here: https://login.docker.com/activate

Waiting for authentication in the browser…


WARNING! Your credentials are stored unencrypted in '/root/.docker/config.json'.
Configure a credential helper to remove this warning. See
https://docs.docker.com/go/credential-store/

Login Succeeded
ubuntu@ip-10-0-3-165:~/Module-3-deployment$


buntu@ip-10-0-3-165:~/Module-3-deployment$ docker run -d -p 3000:3000 express-app
permission denied while trying to connect to the docker API at unix:///var/run/docker.sock
ubuntu@ip-10-0-3-165:~/Module-3-deployment$ docker ps
permission denied while trying to connect to the docker API at unix:///var/run/docker.sock
ubuntu@ip-10-0-3-165:~/Module-3-deployment$ sudo docker tag express-app tonmoyshajedul@gmail.com/express-app:latest
error parsing reference: "tonmoyshajedul@gmail.com/express-app:latest" is not a valid repository/tag: invalid reference format
ubuntu@ip-10-0-3-165:~/Module-3-deployment$ sudo docker tag express-app shajedultonmoy/express-app:latest
ubuntu@ip-10-0-3-165:~/Module-3-deployment$ sudo docker push shajedultonmoy/express-app:latest
The push refers to repository [docker.io/shajedultonmoy/express-app]
c1ba30b6d762: Pushed 
2db173fc8ab9: Pushed 
d6a3a8481b91: Pushed 
b2cbbfe903b0: Mounted from library/node 
6a0ac1617861: Mounted from library/node 
4feea04c1543: Mounted from library/node 
fff4e2c1b189: Mounted from library/node 
b4a9d36bdb6a: Pushed 
latest: digest: sha256:025ff131e7e3c37c421d1c6016212ff419327906dba4d2cd01f38d263a6ae214 size: 2058
ubuntu@ip-10-0-3-165:~/Module-3-deployment$ 

buntu@ip-10-0-3-165:~/Module-3-deployment$ sudo nano docker-compose.yml
ubuntu@ip-10-0-3-165:~/Module-3-deployment$ sudo docker compose up -d
unknown shorthand flag: 'd' in -d

Usage:  docker [OPTIONS] COMMAND [ARG...]

Run 'docker --help' for more information
ubuntu@ip-10-0-3-165:~/Module-3-deployment$ sudo docker compose ps
docker: unknown command: docker compose

Run 'docker --help' for more information
ubuntu@ip-10-0-3-165:~/Module-3-deployment$ sudo docker-compose up -d
Creating network "module-3-deployment_default" with the default driver
Pulling nginx (nginx:alpine)...
alpine: Pulling from library/nginx
c75b9c33e8b0: Pull complete
c16defe09b2f: Pull complete
5b429a43b8df: Pull complete
967885d218c5: Pull complete
ce42635eeddd: Pull complete
01bf363d61e6: Pull complete
e6f31ffc071e: Pull complete
ab1fd9049751: Pull complete
9e6bf8ac91af: Download complete
84fd3fc5237f: Download complete
Digest: sha256:54f2a904c251d5a34adf545a72d32515a15e08418dae0266e23be2e18c66fefa
Status: Downloaded newer image for nginx:alpine
Building web
DEPRECATED: The legacy builder is deprecated and will be removed in a future release.
            Install the buildx component to build images with BuildKit:
            https://docs.docker.com/go/buildx/

Sending build context to Docker daemon  243.7kB
Step 1/7 : FROM node:20-alpine
 ---> fb4cd12c85ee
Step 2/7 : WORKDIR /app
 ---> Using cache
 ---> aa275acc3618
Step 3/7 : COPY package*.json ./
 ---> Using cache
 ---> e1bd3df0181b
Step 4/7 : RUN npm install
 ---> Using cache
 ---> f43578f0a189
Step 5/7 : COPY . .
 ---> 10f3fd4df384
Step 6/7 : EXPOSE 3000
 ---> Running in 1633717cd96d
 ---> Removed intermediate container 1633717cd96d
 ---> b9c28f11a49b
Step 7/7 : CMD ["npm","start"]
 ---> Running in 451bec8f5477
 ---> Removed intermediate container 451bec8f5477
 ---> fa7b62820496
Successfully built fa7b62820496
Successfully tagged module-3-deployment_web:latest
WARNING: Image for service web was built because it did not already exist. To rebuild this image you must use `docker-compose build` or `docker-compose up --build`.
Creating nginx_server ... done
Creating express_web_app ... done
ubuntu@ip-10-0-3-165:~/Module-3-deployment$ sudo docker-compose ps
     Name                    Command               State                  Ports                
-----------------------------------------------------------------------------------------------
express_web_app   docker-entrypoint.sh npm start   Up      3000/tcp                            
nginx_server      /docker-entrypoint.sh ngin ...   Up      0.0.0.0:8080->80/tcp,:::8080->80/tcp
ubuntu@ip-10-0-3-165:~/Module-3-deployment$ sudo docker-compose logs
Attaching to express_web_app, nginx_server
express_web_app | 
express_web_app | > node-express-app@1.0.0 start
express_web_app | > node src/server.js
express_web_app | 
express_web_app | Server running on port 5000
nginx_server | /docker-entrypoint.sh: /docker-entrypoint.d/ is not empty, will attempt to perform configuration
nginx_server | /docker-entrypoint.sh: Looking for shell scripts in /docker-entrypoint.d/
nginx_server | /docker-entrypoint.sh: Launching /docker-entrypoint.d/10-listen-on-ipv6-by-default.sh
nginx_server | 10-listen-on-ipv6-by-default.sh: info: Getting the checksum of /etc/nginx/conf.d/default.conf
nginx_server | 10-listen-on-ipv6-by-default.sh: info: Enabled listen on IPv6 in /etc/nginx/conf.d/default.conf
nginx_server | /docker-entrypoint.sh: Sourcing /docker-entrypoint.d/15-local-resolvers.envsh
nginx_server | /docker-entrypoint.sh: Launching /docker-entrypoint.d/20-envsubst-on-templates.sh
nginx_server | /docker-entrypoint.sh: Launching /docker-entrypoint.d/30-tune-worker-processes.sh
nginx_server | /docker-entrypoint.sh: Configuration complete; ready for start up
nginx_server | 2026/06/24 08:39:07 [notice] 1#1: using the "epoll" event method
nginx_server | 2026/06/24 08:39:07 [notice] 1#1: nginx/1.31.2
nginx_server | 2026/06/24 08:39:07 [notice] 1#1: built by gcc 15.2.0 (Alpine 15.2.0) 
nginx_server | 2026/06/24 08:39:07 [notice] 1#1: OS: Linux 6.17.0-1017-aws
nginx_server | 2026/06/24 08:39:07 [notice] 1#1: getrlimit(RLIMIT_NOFILE): 1024:524288
nginx_server | 2026/06/24 08:39:07 [notice] 1#1: start worker processes
nginx_server | 2026/06/24 08:39:07 [notice] 1#1: start worker process 30
nginx_server | 2026/06/24 08:39:07 [notice] 1#1: start worker process 31
ubuntu@ip-10-0-3-165:~/Module-3-deployment$ cd ~/Module-3-deployment
ubuntu@ip-10-0-3-165:~/Module-3-deployment$ sudo docker-compose up -d
nginx_server is up-to-date
express_web_app is up-to-date
ubuntu@ip-10-0-3-165:~/Module-3-deployment$ sudo docker-compose ps
     Name                    Command               State                  Ports                
-----------------------------------------------------------------------------------------------
express_web_app   docker-entrypoint.sh npm start   Up      3000/tcp                            
nginx_server      /docker-entrypoint.sh ngin ...   Up      0.0.0.0:8080->80/tcp,:::8080->80/tcp
ubuntu@ip-10-0-3-165:~/Module-3-deployment$ sudo docker-compose logs
Attaching to express_web_app, nginx_server
express_web_app | 
express_web_app | > node-express-app@1.0.0 start
express_web_app | > node src/server.js
express_web_app | 
express_web_app | Server running on port 5000
nginx_server | /docker-entrypoint.sh: /docker-entrypoint.d/ is not empty, will attempt to perform configuration
nginx_server | /docker-entrypoint.sh: Looking for shell scripts in /docker-entrypoint.d/
nginx_server | /docker-entrypoint.sh: Launching /docker-entrypoint.d/10-listen-on-ipv6-by-default.sh
nginx_server | 10-listen-on-ipv6-by-default.sh: info: Getting the checksum of /etc/nginx/conf.d/default.conf
nginx_server | 10-listen-on-ipv6-by-default.sh: info: Enabled listen on IPv6 in /etc/nginx/conf.d/default.conf
nginx_server | /docker-entrypoint.sh: Sourcing /docker-entrypoint.d/15-local-resolvers.envsh
nginx_server | /docker-entrypoint.sh: Launching /docker-entrypoint.d/20-envsubst-on-templates.sh
nginx_server | /docker-entrypoint.sh: Launching /docker-entrypoint.d/30-tune-worker-processes.sh
nginx_server | /docker-entrypoint.sh: Configuration complete; ready for start up
nginx_server | 2026/06/24 08:39:07 [notice] 1#1: using the "epoll" event method
nginx_server | 2026/06/24 08:39:07 [notice] 1#1: nginx/1.31.2
nginx_server | 2026/06/24 08:39:07 [notice] 1#1: built by gcc 15.2.0 (Alpine 15.2.0) 
nginx_server | 2026/06/24 08:39:07 [notice] 1#1: OS: Linux 6.17.0-1017-aws
nginx_server | 2026/06/24 08:39:07 [notice] 1#1: getrlimit(RLIMIT_NOFILE): 1024:524288
nginx_server | 2026/06/24 08:39:07 [notice] 1#1: start worker processes
nginx_server | 2026/06/24 08:39:07 [notice] 1#1: start worker process 30
nginx_server | 2026/06/24 08:39:07 [notice] 1#1: start worker process 31
ubuntu@ip-10-0-3-165:~/Module-3-deployment$ 

ubuntu@ip-10-0-3-165:~/Module-3-deployment$ docker ps
permission denied while trying to connect to the docker API at unix:///var/run/docker.sock
ubuntu@ip-10-0-3-165:~/Module-3-deployment$ sudo usermod -aG docker ubuntu
ubuntu@ip-10-0-3-165:~/Module-3-deployment$ exit
logout
Connection to 34.239.127.16 closed.
shajedul@Hydra:~/Documents/AWS$ ssh -i key.pem ubuntu@34.239.127.16
Warning: Identity file key.pem not accessible: No such file or directory.
ubuntu@34.239.127.16: Permission denied (publickey).
shajedul@Hydra:~/Documents/AWS$ ssh -i ST-Key-Dev002.pem ubuntu@34.239.127.16
Welcome to Ubuntu 24.04.4 LTS (GNU/Linux 6.17.0-1017-aws x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/pro

 System information as of Wed Jun 24 08:46:26 UTC 2026

  System load:  0.0               Temperature:           -273.1 C
  Usage of /:   29.6% of 8.65GB   Processes:             123
  Memory usage: 11%               Users logged in:       0
  Swap usage:   0%                IPv4 address for ens5: 10.0.3.165


Expanded Security Maintenance for Applications is not enabled.

10 updates can be applied immediately.
10 of these updates are standard security updates.
To see these additional updates run: apt list --upgradable

1 additional security update can be applied with ESM Apps.
Learn more about enabling ESM Apps service at https://ubuntu.com/esm


Last login: Wed Jun 24 07:35:51 2026 from 103.189.237.32
ubuntu@ip-10-0-3-165:~$ docker ps
CONTAINER ID   IMAGE                     COMMAND                  CREATED         STATUS         PORTS                                     NAMES
229ada8fdce9   module-3-deployment_web   "docker-entrypoint.s…"   7 minutes ago   Up 7 minutes   3000/tcp                                  express_web_app
15c4c7cde5f3   nginx:alpine              "/docker-entrypoint.…"   7 minutes ago   Up 7 minutes   0.0.0.0:8080->80/tcp, [::]:8080->80/tcp   nginx_server
ubuntu@ip-10-0-3-165:~$ 


ubuntu@ip-10-0-3-165:~$ docker ps
CONTAINER ID   IMAGE                     COMMAND                  CREATED         STATUS         PORTS                                     NAMES
229ada8fdce9   module-3-deployment_web   "docker-entrypoint.s…"   7 minutes ago   Up 7 minutes   3000/tcp                                  express_web_app
15c4c7cde5f3   nginx:alpine              "/docker-entrypoint.…"   7 minutes ago   Up 7 minutes   0.0.0.0:8080->80/tcp, [::]:8080->80/tcp   nginx_server
ubuntu@ip-10-0-3-165:~$ cat src/server.js
cat: src/server.js: No such file or directory
ubuntu@ip-10-0-3-165:~$ cat docker-compose.yml
cat: docker-compose.yml: No such file or directory
ubuntu@ip-10-0-3-165:~$ cd ~/Module-3-deployment
ubuntu@ip-10-0-3-165:~/Module-3-deployment$ cat src/server.js
const express = require('express');
const path = require('path');
const fileURLToPath = require('url');
// import path from 'path';
// import { fileURLToPath } from 'url';

// __filename = fileURLToPath(import.meta.url);
// const __dirname = path.dirname(__filename);

const app = express();
const port = process.env.PORT || 5000;

// Serve static files from the public directory
app.use(express.static(path.join(__dirname, 'public')));

app.get('/', (req, res) => {
  res.sendFile(path.join(__dirname, 'public', 'index.html'));
});

app.get('/api', (req, res) => {
  res.json({ message: 'Hello World changes'});
});

let server;

// if (import.meta.url === new URL(import.meta.resolve('./server.js')).href) {
//   server = app.listen(port, () => {
//     console.log(`Server is running on port ${port}`);
//   });
// }

if (require.main === module) {
  // If the file is run directly, start the server
  const PORT = process.env.PORT || 5000;
  server = app.listen(PORT, () => console.log(`Server running on port ${PORT}`));
}

module.exports = appubuntu@ip-10-0-3-165:~/Module-3-deployment$ cat docker-compose.yml
version: '3.8'

services:
  nginx:
    image: nginx:alpine
    container_name: nginx_server
    ports:
      - "8080:80" # Exposes the stack on port 8080 per assignment criteria

  web:
    build: .
    container_name: express_web_app
    depends_on:
      - nginx # Starts the Express app after Nginx
ubuntu@ip-10-0-3-165:~/Module-3-deployment$ cat nginx/default.conf
cat: nginx/default.conf: No such file or directory
ubuntu@ip-10-0-3-165:~/Module-3-deployment$ curl localhost:8080
<!DOCTYPE html>
<html>
<head>
<title>Welcome to nginx!</title>
<style>
html { color-scheme: light dark; }
body { width: 35em; margin: 0 auto;
font-family: Tahoma, Verdana, Arial, sans-serif; }
</style>
</head>
<body>
<h1>Welcome to nginx!</h1>
<p>If you see this page, nginx is successfully installed and working.
Further configuration is required for the web server, reverse proxy, 
API gateway, load balancer, content cache, or other features.</p>

<p>For online documentation and support please refer to
<a href="https://nginx.org/">nginx.org</a>.<br/>
To engage with the community please visit
<a href="https://community.nginx.org/">community.nginx.org</a>.<br/>
For enterprise grade support, professional services, additional 
security features and capabilities please refer to
<a href="https://f5.com/nginx">f5.com/nginx</a>.</p>

<p><em>Thank you for using nginx.</em></p>
</body>
</html>
ubuntu@ip-10-0-3-165:~/Module-3-deployment$ mkdir -p nginx
ubuntu@ip-10-0-3-165:~/Module-3-deployment$ nano nginx/default.conf
ubuntu@ip-10-0-3-165:~/Module-3-deployment$ sudo nano docker-compose.yml
ubuntu@ip-10-0-3-165:~/Module-3-deployment$ sudo docker-compose down
Stopping express_web_app ... done
Stopping nginx_server    ... done
Removing express_web_app ... done
Removing nginx_server    ... done
Removing network module-3-deployment_default
ubuntu@ip-10-0-3-165:~/Module-3-deployment$ sudo docker-compose up -d --build
Creating network "module-3-deployment_default" with the default driver
Building web
DEPRECATED: The legacy builder is deprecated and will be removed in a future release.
            Install the buildx component to build images with BuildKit:
            https://docs.docker.com/go/buildx/

Sending build context to Docker daemon  245.2kB
Step 1/7 : FROM node:20-alpine
 ---> fb4cd12c85ee
Step 2/7 : WORKDIR /app
 ---> Using cache
 ---> aa275acc3618
Step 3/7 : COPY package*.json ./
 ---> Using cache
 ---> e1bd3df0181b
Step 4/7 : RUN npm install
 ---> Using cache
 ---> f43578f0a189
Step 5/7 : COPY . .
 ---> 8b3b88ec7bd3
Step 6/7 : EXPOSE 3000
 ---> Running in 63fc2a9398ab
 ---> Removed intermediate container 63fc2a9398ab
 ---> 966c124a3849
Step 7/7 : CMD ["npm","start"]
 ---> Running in d1d29416bc2a
 ---> Removed intermediate container d1d29416bc2a
 ---> da23798eac17
Successfully built da23798eac17
Successfully tagged module-3-deployment_web:latest
Creating express_web_app ... done
Creating nginx_server    ... done
ubuntu@ip-10-0-3-165:~/Module-3-deployment$ sudo docker-compose ps
     Name                    Command               State                  Ports                
-----------------------------------------------------------------------------------------------
express_web_app   docker-entrypoint.sh npm start   Up      3000/tcp                            
nginx_server      /docker-entrypoint.sh ngin ...   Up      0.0.0.0:8080->80/tcp,:::8080->80/tcp
ubuntu@ip-10-0-3-165:~/Module-3-deployment$ curl localhost:8080
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hello World</title>
    <link rel="stylesheet" href="/styles.css">
</head>
<body class="container">
    <h1 class="hello-world">Roy</h1>
</body>
</html>ubuntu@ip-10-0-3-165:~/Module-3-deployment$ 
ubuntu@ip-10-0-3-165:~/Module-3-deployment$ sudo docker-compose logs
Attaching to nginx_server, express_web_app
nginx_server | /docker-entrypoint.sh: /docker-entrypoint.d/ is not empty, will attempt to perform configuration
nginx_server | /docker-entrypoint.sh: Looking for shell scripts in /docker-entrypoint.d/
nginx_server | /docker-entrypoint.sh: Launching /docker-entrypoint.d/10-listen-on-ipv6-by-default.sh
nginx_server | 10-listen-on-ipv6-by-default.sh: info: Getting the checksum of /etc/nginx/conf.d/default.conf
nginx_server | 10-listen-on-ipv6-by-default.sh: info: /etc/nginx/conf.d/default.conf differs from the packaged version
nginx_server | /docker-entrypoint.sh: Sourcing /docker-entrypoint.d/15-local-resolvers.envsh
nginx_server | /docker-entrypoint.sh: Launching /docker-entrypoint.d/20-envsubst-on-templates.sh
nginx_server | /docker-entrypoint.sh: Launching /docker-entrypoint.d/30-tune-worker-processes.sh
nginx_server | /docker-entrypoint.sh: Configuration complete; ready for start up
nginx_server | 2026/06/24 08:54:43 [notice] 1#1: using the "epoll" event method
nginx_server | 2026/06/24 08:54:43 [notice] 1#1: nginx/1.31.2
nginx_server | 2026/06/24 08:54:43 [notice] 1#1: built by gcc 15.2.0 (Alpine 15.2.0) 
nginx_server | 2026/06/24 08:54:43 [notice] 1#1: OS: Linux 6.17.0-1017-aws
nginx_server | 2026/06/24 08:54:43 [notice] 1#1: getrlimit(RLIMIT_NOFILE): 1024:524288
nginx_server | 2026/06/24 08:54:43 [notice] 1#1: start worker processes
nginx_server | 2026/06/24 08:54:43 [notice] 1#1: start worker process 29
nginx_server | 2026/06/24 08:54:43 [notice] 1#1: start worker process 30
nginx_server | 172.18.0.1 - - [24/Jun/2026:08:55:01 +0000] "GET / HTTP/1.1" 200 316 "-" "curl/8.5.0" "-"
nginx_server | 103.189.237.32 - - [24/Jun/2026:08:55:12 +0000] "GET / HTTP/1.1" 200 316 "-" "Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/149.0.0.0 Safari/537.36" "-"
nginx_server | 103.189.237.32 - - [24/Jun/2026:08:55:12 +0000] "GET /styles.css HTTP/1.1" 200 768 "http://34.239.127.16:8080/" "Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/149.0.0.0 Safari/537.36" "-"
nginx_server | 103.189.237.32 - - [24/Jun/2026:08:55:12 +0000] "GET /favicon.ico HTTP/1.1" 404 150 "http://34.239.127.16:8080/" "Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/149.0.0.0 Safari/537.36" "-"
nginx_server | 103.189.237.32 - - [24/Jun/2026:09:00:22 +0000] "GET / HTTP/1.1" 304 0 "-" "Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/149.0.0.0 Safari/537.36" "-"
nginx_server | 103.189.237.32 - - [24/Jun/2026:09:00:22 +0000] "GET /styles.css HTTP/1.1" 304 0 "http://34.239.127.16:8080/" "Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/149.0.0.0 Safari/537.36" "-"
express_web_app | 
express_web_app | > node-express-app@1.0.0 start
express_web_app | > node src/server.js
express_web_app | 
express_web_app | Server running on port 5000
ubuntu@ip-10-0-3-165:~/Module-3-deployment$ 

