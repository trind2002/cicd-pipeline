# cicd-pipeline
Creating a Simple Workflow


Using KVdb REST API
Create a bucket
# Syntax
curl -d 'email=your-email-ID@domain.com' https://kvdb.io
# Returns a bucket ID, such as, "XsgrYuyPESbxCcte4sLxEM"
Store the key-value pair
# Syntax
curl https://kvdb.io/[bucket-ID]/[key]  -d '[value]'
# Example
curl https://kvdb.io/XsgrYuyPESbxCcte4sLxEM/migration_$\{CIRCLE_WORKFLOW_ID:0:7\}  -d '1'
Access the value associated with a key

# Syntax
curl --insecure  https://kvdb.io/[bucket-ID]/[key]
# Example
curl --insecure  https://kvdb.io/XsgrYuyPESbxCcte4sLxEM/migration_$\{CIRCLE_WORKFLOW_ID:0:7\}