# ansible-demo-lab

sudo tail -f /var/log/cloud-init-output.log

cd ~/ansible-demo-lab

ansible-inventory -i inventory/aws_ec2.yml --graph


ansible-playbook -i inventory/aws_ec2.yml playbooks/day1_provision.yml \
  --user ec2-user \
  --ssh-common-args='-o StrictHostKeyChecking=no'
