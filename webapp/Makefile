.PHONY: up
up:
	docker compose up -d

.PHONY: down
down:
	docker compose down
	
.PHONY: restart
restart:
	docker compose down; docker compose up -d

.PHONY: logs
log:
	docker compose logs -f

.PHONY: reset-logs
reset-logs:
	mv ./logs/nginx/access.log ./logs/nginx/access.log.$(shell date +%Y%m%d-%H%M%S) | : 
	mv ./logs/mysql/mysql-slow.log ./logs/mysql/mysql-slow.log.$(shell date +%Y%m%d-%H%M%S) | : 
	@make restart