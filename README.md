# PostgreSQL

kustomize build k8s/postgre/ -o postgre.yaml

kubectl --context <name_context> apply -f postgre.yaml

kubectl --context <name_context> -n postgre port-forward pod/postgr-<id_pod> 5432:5432

# Fake Shop

kustomize build k8s/fake_shop/ -o fake-shop.yaml

kubectl --context <name_context> apply -f fake-shop.yaml

kubectl --context <name_context> -n fakeshop port-forward service/fakeshop 5000:5000

## Variável de Ambiente
DB_HOST	=> Host do banco de dados PostgreSQL.

DB_USER => Nome do usuário do banco de dados PostgreSQL.

DB_PASSWORD	=> Senha do usuário do banco de dados PostgreSQL.

DB_NAME	=>	Nome do banco de dados PostgreSQL.

DB_PORT	=>	Porta de conexão com o banco de dados PostgreSQL.
