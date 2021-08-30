# -*- mode: ruby -*-
# vi: set ft=ruby :
docker_compose = %q(
version: '3.1'
services:
  db:
    image: mariadb:10.3
    restart: always
    environment:
      MYSQL_ROOT_PASSWORD: notSecureChangeMe

  phpmyadmin:
    image: phpmyadmin
    restart: always
    ports:
      - 8080:80
    environment:
      - PMA_ARBITRARY=1
)
Vagrant.configure("2") do |config|
  config.vm.define  "rdbms"
  config.vm.box = "debian/buster64"
  config.vm.box_check_update = false
  config.vm.synced_folder ".", "/vagrant", disabled: true
  # this is only required for the deployment using Docker
  config.vm.provision "shell" do |s|
    s.privileged = true,
    s.inline = %Q(
      apt-get update -q
      apt-get install -q -y docker docker-compose
      echo "#{docker_compose}" > docker-compose.yml 
      docker-compose up --detach
    )
  end
end
