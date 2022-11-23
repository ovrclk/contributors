# Akash Contributors

Generated using:

```shell
for repo in akash awesome-akash docs net ecosystem disco cosmos-omnibus 
do 
  curl "https://api.github.com/repos/ovrclk/${repo}/contributors?&per_page=100&page=1" | jq -r '.[] | .login' > ${repo}.contrib
done

cat *.contrib | sort -u > CONTRIBUTORS
```
