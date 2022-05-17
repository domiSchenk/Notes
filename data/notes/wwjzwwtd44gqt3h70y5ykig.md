
# Index html generation failed

## Property Missing ':'
![](assets/images/index-html-gen-failed.png)

If this happens, somewhere in a CSS file, a non base64 svg is used!
Something like this:
> background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='540' height='450' viewBox='0 0 1080 900'%3E%3Cg6...");

### Solution
add this to `angular.json`
```json
"optimization": {
	"styles": {
		"inlineCritical": false
	}
 }
```

1
