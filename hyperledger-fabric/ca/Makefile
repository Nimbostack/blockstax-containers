.PHONY: build
APP_VERSION := 1.5.12

build: package tag

image:
	apko build apko.yaml nimbostack/hyperledger-fabric-ca:$(APP_VERSION) \
        --repository-append ./packages hyperledger-fabric-ca.tar

publish:
	$(eval DIGEST:=$(shell apko publish apko.yaml \
        --keyring-append ../../melange.rsa.pub --arch x86_64,aarch64 \
        --sbom=false \
        --repository-append packages docker.io/nimbostack/hyperledger-fabric-ca:$(APP_VERSION)))
    @echo "Image digest: $(DIGEST)"

package:
	melange build melange.yaml --signing-key ../../signing-key.rsa

sign: publish
	COSIGN_PASSWORD="" cosign sign --key ../../cosign.key --yes $(DIGEST)

tag: sign
	crane copy $(DIGEST) docker.io/nimbostack/hyperledger-fabric-ca:$(APP_VERSION)
