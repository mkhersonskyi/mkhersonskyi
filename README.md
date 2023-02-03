UPDATE AWS ECS

aws ecs update-service --profile mwnonprod --cluster   dev-mw-octordle-cluster  --service stg-mw-octordle-service --force-new-deployment --enable-execute-command

aws ecs execute-command --profile mwnonprod --cluster dev-mw-octordle-cluster    --task c87144aa29194e78abf2233f93786901 --container stg-mw-octordle-nginx-container --interactive --command "bash"

