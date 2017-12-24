deploy:
	docker run -it --rm -v ~/.ssh:/root/.ssh -v `pwd`:/conf williamyeh/ansible:alpine3 ansible-playbook -i /conf/inventory.yml /conf/deploy.yml
