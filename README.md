# bugs_daily
2/3/2019
1. Helm
helm upgrade stuck - https://github.com/helm/helm/issues/5595
  
Workaround:
  Edit helm scerets, set release status from "pending/failed" to "deployed"
  kubectl get secrets --show-labels | grep sh.helm.release.v1
  Then update/rollback
    
2. Airflow Maintenance
Scheduler with Error : No more disk space at /usr/airflow/logs

Workaround:
  Make a dag to delete outdated logs
  https://github.com/teamclairvoyant/airflow-maintenance-dags/blob/master/log-cleanup/airflow-log-cleanup.py


    
    
