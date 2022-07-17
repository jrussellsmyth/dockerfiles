# Various Dockerfiles
## Build
Using the included devcontainer, 

`docker login`

`docker buildx create --use`

navigate to the appropriate project folder and
docker buildx build --push --platform linux/amd64,linux/arm64 --tag jrussellsmyth/{project}:latest .

## Future Improvements
move docker install into Dockerfile, so we can docker buildex create in the dockerfile itself

currently uses vscode featur "docker"

https://github.com/microsoft/vscode-dev-containers/blob/main/script-library/docs/docker.md
