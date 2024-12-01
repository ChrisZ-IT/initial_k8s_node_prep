# initial_k8s_node_prep
playbook for prepping linux nodes to setup a new k8s cluster or adding them to an existing cluster

## How to use:
  • Clone this repo down

  • cd into `initial_k8s_node_prep`

  • run `ansible-galaxy role install -r roles/requirements.yml`

  • update the inventory text file with your list of nodes (At this time I only have this ansible role working on Debian based linux is supported. I'll add RHEL based OSes in the future when I have time)

  • run `ansible-playbook main.yml -i inventory -K`

  • At this point you should be able to either run `sudo kubeadm init` on your control node to setup a new cluster or `kubeadm token create --print-join-command` to get the join commands to join your new nodes to an existing cluster
