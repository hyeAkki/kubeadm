#Deploy Kubernetes Infra in one click.

1. Launches Ubuntu instances, 1 Master node (t2.medium) and 2 Worker Nodes (t2.micro)
2. Installs Docker, kubeadm and their dependancies in all nodes.
3. Installs kubectl in Master node.
4. Generates a Token in Master Node.
5. Manually copy pastewhen asked to join workers.



Usage:

1. Launches instances only
ansible-playbook -i ec2.py -u ubuntu launch_instances.yml

2. Installs all required packages and their dependancy
ansible-playbook -i ec2.py -u ubuntu deploy_k8s.yml
