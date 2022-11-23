# Akash Contributors

```
repo=akash
curl "https://api.github.com/repos/ovrclk/${repo}/contributors?&per_page=100&page=1" | jq -r '.[] | .login' > ${repo}.contrib

cat *.contrib | sort | uniq -u | wc -l
```
