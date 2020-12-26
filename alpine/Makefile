NAME   := ${DOCKER_REPO_NAME}
TAG    := $$(git log -1 --pretty=%!H(MISSING))
IMG    := ${NAME}:alpine-${TAG}
LATEST := ${NAME}:v21-alpine
 
build:
  @docker build -t ${IMG} .
  @docker tag ${IMG} ${LATEST}
 
push:
  @docker push ${NAME}
 
login:
  @docker log -u ${DOCKER_USER} -p ${DOCKER_PASS}
