build:	## builds the hugo website
	hugo

clean:	## cleans the directory where website source code is located
	rm -rf ./dist/*

post:	## adds posts to website according to env variables
	hugo new posts/$(POST_NAME).md
	sed -i '2s/.*/title: "$(POST_TITLE)"/' content/posts/$(POST_NAME).md

lint:	## lint
	shellcheck setup.sh

.SILENT:
help:	## provides help about the commands.
	cat Makefile | grep '##' | tr -d '##'
