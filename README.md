This is a simple test of how a tool like Figma could improve the workflow that starts with design changes on existing screens and ends with the changes implemented on the multiple front end clients.

The first commit on this repo contains the JSON representation of a Figma file containing one app screen. The file was generated with the following command:

```shell
# https://www.figma.com/developers/docs#files-endpoint
curl -X GET -H 'X-FIGMA-TOKEN: <personal access token>' 'https://api.figma.com/v1/files/:file_key' \
| python -m json.tool \
> {file_key}.json
```
The second commit contain changes to the file and via the diff and the screenshots it's easy to understand what has been changed.

The screenshots can be found at the top of the [diff](https://github.com/Homely/Homely.Hackday.DesignChanges/commit/5caa92ea9a1096e76c6a683e35da1b05d9bcb459):
```diff
-    "lastModified": "2018-05-01T07:35:40.894Z",
-    "thumbnailUrl": "https://s3-alpha.figma.com/img/02b8/f956/418ca178b6043c1ad69768dc53e07524",
+    "lastModified": "2018-05-01T07:42:47.844Z",
+    "thumbnailUrl": "https://s3-alpha.figma.com/img/fb2d/cea9/30af5e7b3196d28eb44ee3f58d689008",
```

Version 1 | Version 2
------------ | -------------
![](https://s3-alpha.figma.com/img/02b8/f956/418ca178b6043c1ad69768dc53e07524) | ![](https://s3-alpha.figma.com/img/fb2d/cea9/30af5e7b3196d28eb44ee3f58d689008)
