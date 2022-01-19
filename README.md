Run the initial playbook

`ansible-playbook -i hosts ~/kube-cluster/initial.yml`

Install kubernetes

`ansible-playbook -i hosts ~/kube-cluster/kube-dependencies.yml`

Configuration
`ansible-playbook -i hosts ~/kube-cluster/control-plane.yml`


SSH into the node 
(`ssh test@<ip>`)
Remove control node taint

`kubectl taint nodes --all node-role.kubernetes.io/master-`
  
Miscellaneous:
- Easy way to list node information: `virsh net-dhcp-leases --network default`
