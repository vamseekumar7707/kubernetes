# kubernetes

nginx directory --> FrontEnd Pod  
backend directory --> BackEnd Pod  
database directory --> MySQL:5.6 database Pod  

For the above directories go to next branch (Master)

REFERENCE:
----------
1) https://artifacthub.io/packages/helm/nginx/nginx-ingress
2) https://www.digitalocean.com/community/tutorials/how-to-set-up-an-nginx-ingress-on-digitalocean-kubernetes-using-helm



How To Set Up an Nginx Ingress on DigitalOcean Kubernetes Using Helm
--------------------------------------------------------------------
INSALL HELM
============
sudo snap install helm --classic

Installing via Helm Repository
==============================
helm install my-release nginx-stable/nginx-ingress

Installing Using Chart Sources
==============================
helm install my-release .

Upgrade via Helm Repository:
============================
helm upgrade my-release nginx-stable/nginx-ingress

un-tar the file:
===============
helm pull nginx-stable/nginx-ingress --untar=true

# Route 53 changes 
In Route 53 service kops.cf is Hosted Zones , so create a Record called ex.kops.cf and asign Ingress contoller load balancer in Record.
