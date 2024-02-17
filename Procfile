web_init: sh -c 'psql -U postgres -h roundhouse.proxy.rlwy.net -p 39182 -d railway -c "CREATE SCHEMA IF NOT EXISTS mlflow;"'
web_set_search_path: sh -c 'psql -U postgres -h roundhouse.proxy.rlwy.net -p 39182 -d railway -c "ALTER DATABASE railway SET search_path TO mlflow;"'
web_mlflow: mlflow server --host 0.0.0.0 --port $PORT --backend-store-uri postgresql://postgres:$DB_PASSWORD@roundhouse.proxy.rlwy.net:39182/railway
