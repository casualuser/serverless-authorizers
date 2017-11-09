# Serverless Authorizer
Example of a service that uses API Gateway custom authorizer feature to authorize your endpoints with TOKEN type

## Usage

```
cd serverless-authorizer/token_type
serverless deploy

# Notice the displayed endpoint after deployment
url=<endpoint>
curl --header "Authorization: allow" ${url} # Should work! Authorized!
curl --header "Authorization: deny" ${url} # Should not work
curl --header "Authorization: unauthorized" ${url} # Should not work
curl --header "Authorization: blabla" ${url} # Should not work
curl ${url} # Should not work
```