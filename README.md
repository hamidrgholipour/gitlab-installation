# gitlab-installation
#get root pass
docker exec -it <gitlab-container-name> grep 'Password:' /etc/gitlab/initial_root_password
#register a runner
docker run --rm -it -v /srv/gitlab-runner/config:/etc/gitlab-runner gitlab/gitlab-runner register
#if get error host not resolve add below to config.tol
network_mode = "host"
