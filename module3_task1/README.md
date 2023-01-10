## Building a website with Go-Hugo

## Prerequisites

- Install Hugo (the extended edition)
- Install Git
- install go

## Lifecycle
- build: Generate the website from the markdown and configuration files in the directory dist/.
- clean: Cleanup the content of the directory dist/
- post: Create a new blog post whose filename and title come from the environment variables POST_TITLE and POST_NAME.
- help: prints out the list of commands in makefile and their usage.
