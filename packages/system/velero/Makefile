export NAME=velero
export NAMESPACE=cozy-$(NAME)

include ../../../scripts/package-system.mk

update:
	rm -rf charts
	helm repo add vmware-tanzu https://vmware-tanzu.github.io/helm-charts
	helm repo update vmware-tanzu
	helm pull vmware-tanzu/velero --untar --untardir charts