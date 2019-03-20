Please note down the following information from the output:

To start using your cluster, you need to run the following as a regular user:

mkdir -p $HOME/.kube
sudo cp -i /etc/kubernetes/admin.conf $HOME/.kube/config
sudo chown $(id -u):$(id -g) $HOME/.kube/config
You can now join any number of machines by running the following on each node

as root:

kubeadm join 192.168.100.6:6443 --token 06tl4c.oqn35jzecidg0r0m --discovery-token-ca-cert-hash sha256:c40f5fa0aba6ba311efcdb0e8cb637ae0eb8ce27b7a03d47be6d966142f2204c
