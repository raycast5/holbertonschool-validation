build:	## builds the hugo website and the awesome binary
	hugo
	go build -o awesome-api

run: ##  runs the application in background by executing the binary awesome-api
	./awesome-api >./awesome.log 2>&1 &

clean:	## cleans the directory where website source code is located
	rm -rf ./dist/*
	rm  -f ./awesome-api ./awesome.log

post:	## adds posts to website according to env variables
	hugo new posts/$(POST_NAME).md
	sed -i '2s/.*/title: "$(POST_TITLE)"/' content/posts/$(POST_NAME).md

stop:	## stops the application
	pkill awesome-api

test: ## test it to ensure that app behaves as expected
	curl http://localhost:9999
	curl http://localhost:9999/health

.SILENT:
help:	## provides help about the commands.
	cat Makefile | grep '##' | tr -d '##'
