# nginx-map-tester

## Steps

1. Change nginx/nginx.conf test map

i.e.
```
map $request_method_and_uri $test_map {
    default "default";
    "~^GET /match1" "match1";
    "~^GET /match2" "match2";
}
```
2. Start nginx 
```
docker-compose up
```
3. Test with cURL

i.e
```
curl -i localhost:8080/match1
```
