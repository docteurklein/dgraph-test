## drop everything:

```
dcr alpha curl '0/admin/slash' \
    -H "X-Auth-Token: $AUTH_TOKEN" \
    -H 'Content-Type: application/graphql' \
    --data-binary 'mutation { dropData(allDataAndSchema: true) { response { code message } } }'
```

## import

```
dcr alpha dgraph live --alpha alpha:9080 --zero zero:5080 --schema $PWD/schema.txt -f $PWD/1million.rdf.gz
```
