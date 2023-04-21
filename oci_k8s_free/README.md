# oci_k8s
k8s on OCI free tier

Need an Oracle Cloud account
- Need a compartment you want the resources to provision in – it can be the root compartment  

- Optionally an SSH key for worker nodes 

- OCI CLI installed

- Terraform CLI installed

- kubectl installed



- $ export TF_VAR_compartment_id=<your compartment ocid>
- $ export TF_VAR_region=<your region>
- $ export TF_VAR_ssh_public_key=<your public key>
  
cd /oci-infrastructure

  terraform apply -var="compartment_id=ocid1.compartment.oc1.............." -var="region=us-ashburn-1" -var="ssh_public_key=ssh-rsa ............
  
create kubeconfig file:
$ oci ce cluster create-kubeconfig --cluster-id <cluster OCID> --file ~/.kube/ocs-k8s-config --region us-ashburn-1  --token-version 2.0.0 --kube-endpoint PUBLIC_ENDPOINT

$ export KUBECONFIG=~/.kube/ocs-k8s-config

$ kubectl get nodes  


terraform output

cd ./k8s_infrastructure
  
terraform init


terraform apply
![pluralith_layout](https://github.com/gilby125/oci_k8s/blob/main/oci_k8s_free/oci_infrastructure/project_pluralith-local-project%252Frun_2287541%252Frun_2287541_1682085300049.png)
