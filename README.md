# Ansible-Airflow

worker-playbook.yaml contain code to setup Airflow worker node setup. 

Pre-quisite : 
   1) Create "files" directory and copy all below files in it.
            airflow   : this is copied from apache-airflow-1.10.9.tar.gz
            airflow.cfg : this will be your custom airflow configuration file 
            airflow.conf : this is copied from apache-airflow-1.10.9.tar.gz
            airflow-flower.service : this is copied from apache-airflow-1.10.9.tar.gz
            airflow-kerberos.service : this is copied from apache-airflow-1.10.9.tar.gz
            airflow-scheduler.service : this is copied from apache-airflow-1.10.9.tar.gz
            airflow-webserver.service : this is copied from apache-airflow-1.10.9.tar.gz
            airflow-worker.service : this is copied from apache-airflow-1.10.9.tar.gz
  2) It's expected that above files are updated as per your environment 
  3) "files" needs to be created in directory from where you will be executing "ansible-playbook" or you can update "worker-playbook.yaml" file with appropriate path. 
    
    
Download this file and Run below command from Ansible controller node : 
#ansible-playbook enableSystemDscript.yaml   --limit <NEW_AIRFLOW_NODE> --private-key <PEM_FILE_PATH> -vv

Replace 
<NEW_AIRFLOW_NODE> with actual hostname of airflow worker node which you are planning to add to airflow cluster. 
<PEM_FILE_PATH> : this is path to pem file which is used login to worker node 

