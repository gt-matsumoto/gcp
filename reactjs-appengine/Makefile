prj:=gae-go-devm-297203
version-number:=$(shell date "+%Y%m%d%H%M")
version:=v$(version-number)

default:
	@echo "select one of following targets: install build deploy"

install:
	yarn install

build: install
	yarn run build

deploy: build
	gcloud -q app deploy --project $(prj) --version $(version) app.yaml

local: build
	yarn start
