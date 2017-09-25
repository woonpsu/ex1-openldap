# ex1-openldap
ex1-openldap is a docker-compose file with 2 folders to build an example docker service to run openldap.

To run this project.
1. Start/Install ubuntu server 16.04 64 bit and docker 17.06.2-ce
2. Use docker-compose 1.8.0-2, you can install it by "sudo apt install docker-compose"
3. Clone this project,<br>
   git clone https://github.com/woonpsu/ex1-openldap.git
4. Run command<br>
   cd ex1-openldap<br>
   docker-compose up -d<br>
Note: <br>
  This project is based on docker image ubuntu:16.04 so that it will take more time if this image is   not existed.
5. Use this commands to verify,<br>
  docker images<br>
  docker ps<br>
  docker volume ls<br>
6. Add some example users,<br>
   sudo apt install ldap-utils<br>
   ldapadd -H ldap://ldap.example.com -f ./openldap/src/create-users.ldif -x -D "cn=admin,dc=example,dc=com" -w 123456
