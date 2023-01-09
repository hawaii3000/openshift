# openshift
tools for openshift

How to install Wordpress

1) Download "wordpress".

2) Create Namespance :
> oc create ns wordpress2

3) set following policy for namespace.
> oc adm policy add-scc-to-user anyuid -z default -n wordpress2

4) Apply yamls.
> oc apply -k ./ -n wordpress2

