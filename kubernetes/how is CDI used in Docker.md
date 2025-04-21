START
Basic
Front: 
How is CDI used in Docker?
Back: 
CDI is an experimental feature in Docker. To enable it:
1. Add `"features": {"cdi": true}` to `daemon.json`.
2. Specify CDI directories using `cdi-spec-dirs` in `daemon.json` or `--cdi-spec-dir` flag.
3. Run containers with CDI devices using:
```bash
docker run --rm --device vendor.com/class=device_name my-container
```
An example of `daemon.json`:
```json
{
	"features":  {
		"cdi": true
	},
	"cdi-spec-dirs": ["/etc/cdi/", "/var/run/cdi"]
}
```
<!--ID: 1745221428150-->
END