# k8s-aninaka-user-auth-api-manifests

# secret 作成

`kubectl create secret generic my-secret --dry-run=client --from-env-file=./aninaka-credentials/envs/production/db/.env --output=yaml > secret.yml`

# データベースへのアクセス

kubectl exec -it psql-pod -n aninaka -- psql -h mypostgres -U postgres
