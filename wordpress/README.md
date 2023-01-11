How to install Wordpress on Openshift

1) Download all files in this directory.

2) Create Namespance.
>oc create ns wordpress

3) Set following policy for the namespace.
>oc adm policy add-scc-to-user anyuid -z default -n wordpress1

4) Apply donwloaded yamls.
>oc apply -k ./ -n wordpress
