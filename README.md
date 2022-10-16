# V2ray deployment via Ansible on Docker

## Quick start

1. Make changes in the [`vars.yml`](./vars.yml) (_just edit two following variables_):
   * `external_node_domain`: Enter yout hostname or public IP address.
   * `port`: sets on 443 (recommended, because of _https_) but you could modify that.

2. Ensure that you have Ansible and `docker` by issuing the following command:
   ```bash
   sudo pip install ansible
   # or sudo apt install ansible
   sudo pip install docker
   ```

3. Make changes in the [`hosts`](./hosts) inventory list, You should have private key, if you have not any private key and login via password, uncomment the 7rd and 15rd `ansible_password` vars.

4. Deploying v2ray:
   ```
   ansible-playbook -i hosts.ini playbook.yml
   ```