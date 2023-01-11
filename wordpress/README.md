How to install Wordpress on Openshift

1)Download "wordpress".

2)Create Namespance.
oc create ns wordpress

3) set following policy for namespace.
oc adm policy add-scc-to-user anyuid -z default -n wordpress2

4) Apply yamls.
oc apply -k ./ -n wordpress
