To deploy dashboard

kubectl apply -f https://raw.githubusercontent.com/kubernetes/dashboard/v2.7.0/aio/deploy/recommended.yaml


kubectl proxy 


Kubectl will make Dashboard available at http://localhost:8001/api/v1/namespaces/kubernetes-dashboard/services/https:kubernetes-dashboard:/proxy/.


At this point you can not access yet. 

Apply the admin-user 

Apply the serviceaccount 


Create the admin user token:

kubectl -n kubernetes-dashboard create token admin-user


Resources: https://github.com/kubernetes/dashboard/blob/master/docs/user/access-control/creating-sample-user.md


