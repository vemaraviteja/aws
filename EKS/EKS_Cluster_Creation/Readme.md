
## Create an IAM role and Assign that Role to ec2 instance where kubectl got installed

## Create an EKS cluster with 2 nodes & instance type - t2.micro
    eksctl create cluster \
    --name my-cluster3 \
    --region us-east-1 \
    --nodegroup-name my-nodes \
    --node-type t2.micro \
    --nodes 2

## Check created nodes
    'kubectl get nodes' 
    
## Check Default pods
    'kubectl get pods -n kube-system' or 'kubectl get po'
    
## Run a httpd service in pod
     'kubectl run <name_for_pod> <image_name>
        'kubectl run httpd --image=httpd'

## Delete Cluster
    eksctl delete cluster --name <cluster_name> --region <cluster_region>
