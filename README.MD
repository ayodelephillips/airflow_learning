A. SetUp
https://medium.com/international-school-of-ai-data-science/setting-up-apache-airflow-in-ubuntu-324cfcee1427
1. **set up virtualenv**
2. in the activated virtualenv, install airflow via 
**"pip3 install apache-airflow[gcp,sentry,statsd]"**
3. install sklearn if needed via "pip3 install pyspark"
4. Set **AIRFLOW_HOME** environment variable to the current working directory via ' export AIRFLOW_HOME="$(pwd)" '
DB: sqlite:////home/samuel/airflow/airflow.db
5. navigate to airflow_learning/airflow. Then run the command "**airflow db init**".
This creates the logs folder, a config file(airflow.cfg) and airflow.db
6. If running for the first time, create a user.
**airflow users create --username admin --password root --firstname your_first_name --lastname your_last_name --role Admin --email your_email@domain.com**
7. verify username via **"airflow users list"**
8. start airflow scheduler -- **"airflow scheduler"**
9. open a new terminal, activate the virtualenv, navigate to **airflow folder** and start the webserver
**"airflow webserver"**
10. navigate to **"localhost:8080"**