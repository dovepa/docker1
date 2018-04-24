FROM debian

LABEL dpalombo ex03 GitLab docker1

RUN apt-get update -y \
	&& apt-get upgrade -y \
	&& apt-get install -y curl openssh-server ca-certificates \
	&& apt-get install -y postfix \
	&& curl https://packages.gitlab.com/install/repositories/gitlab/gitlab-ee/script.deb.sh | bash \
	&& EXTERNAL_URL="http://gitlab.example.com" apt-get install gitlab-ee


# Expose web & ssh
EXPOSE 443 80 22

#docker run -p 443:443 -p 80:80 -p 22:22 test