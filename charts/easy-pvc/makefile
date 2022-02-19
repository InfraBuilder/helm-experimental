RELEASENAME=testrelease

TARGET=fulltest

fulltest: render kubelint autoclean install

render:
	helm template $(RELEASENAME) -f values.override-test.yaml .
kubelint:
	helm template $(RELEASENAME) -f values.override-test.yaml  .|kubectl apply -f - --dry-run=client
install:
	helm install $(RELEASENAME) -f values.override-test.yaml  .
autoclean:
	helm list  -q| grep "$(RELEASENAME)" && helm delete $(RELEASENAME); echo autoclean done
clean:
	helm delete $(RELEASENAME)