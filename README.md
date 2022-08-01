1. Configure hosts file

2. Install kubernetes

  `ansible-playbook -i hosts kube-dependencies.yml`

3. Configuration

  `ansible-playbook -i hosts control-plane.yml`


4. SSH into the node

  (`ssh test@<ip>`)

5. Remove control node taint

  `kubectl taint nodes --all node-role.kubernetes.io/master-`
  
Miscellaneous:
- Easy way to list node information: `virsh net-dhcp-leases --network default`

Credit: Based on playbooks from
https://www.digitalocean.com/community/tutorials/how-to-create-a-kubernetes-cluster-using-kubeadm-on-ubuntu-18-04
