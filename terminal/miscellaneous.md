# Terminal

## Save multiline into file

```yaml
cat <<EOF > myfile.yaml
apiVersion: v1
kind: Pod
metadata:
  name: nginx
spec:
  containers:
  - name: nginx
    image: nginx:1.14.2
    ports:
    - containerPort: 80
EOF
```

## Filter output with colums with condition

Example output:
```bash
apple banana strawberry
pear coconut blueberry 
```

Extract first column if third column contains blueberry:
```bash
awk '$3 == "blueberry" {print $1}' file
```
