
# standard role execution for front server serving static files
```
ansible-playbook /etc/ansible/roles/torlowski.configurator_nginx/site.yml -u root -t "standard_front_static,reload_nginx" -e "domain=gistance-test.ngn-itsolutions.eu" -l rocky
```

# standard role execution for backedn server working as reverse proxy for tomcat
```
ansible-playbook /etc/ansible/roles/torlowski.configurator_nginx/site.yml -u root -t "standard_be_tomcat,reload_nginx" -e "domain=gistance-test-api.ngn-itsolutions.eu proxy_pass_port=8081" -l rocky
```
