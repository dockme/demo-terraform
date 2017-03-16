```
ansible-galaxy install -f -r roles.yml -p roles
vault server -dev &
export GOOGLE_APPLICATION_CREDENTIALS=~/.gcloud/account.json; \
  export VAULT_ADDR='http://127.0.0.1:8200' \
  packer build -var "project_id=_gcloud_project_id_" -var "hashi_vault_token=_hashicorp_vault_token_" docker-swarm-node.json
```
