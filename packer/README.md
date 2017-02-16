```
ansible-galaxy install -f -r roles.yml -p roles
export GOOGLE_APPLICATION_CREDENTIALS=~/.gcloud/account.json; \
  packer build -var "project_id=_gcloud_project_id_" docker-swarm-node.json
```
