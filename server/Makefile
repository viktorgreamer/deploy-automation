include .env
export
up:
	docker-compose up -d --build
start:
	docker-compose start
down:
	docker-compose down  --remove-orphans
ssh-remote-staging:
	ssh root@10.5.0.3
ssh-remote-prod:
	ssh root@10.5.0.4
ssh-copy-keys-staging:
	echo ${PASSWORD} | ssh-copy-id -i ~/.ssh/id_rsa.pub root@10.5.0.3
ssh-copy-keys-prod:
	echo ${PASSWORD} ssh-copy-id -i ~/.ssh/id_rsa.pub root@10.5.0.4

