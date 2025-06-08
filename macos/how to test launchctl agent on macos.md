START
Basic
Front: 
How do you manually run a launchd agent on macOS to test it immediately?
Back: 
User launch agents are located in `~/Library/LaunchAgents`. 
1. **Unload (optional, for a clean reload):**
 ```shell
launchctl unload ~/Library/LaunchAgents/com.example.myagent.plist
```
2. **Load the agent:**
```shell
launchctl load ~/Library/LaunchAgents/com.example.myagent.plist
```
2. **Start it immediately:** (use the `Label` field from the plist file as the agent id)
```
launchctl start com.example.myagent
```
END
