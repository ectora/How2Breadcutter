## Hosting: How to host in Pterodactyl
1. [Follow the steps except number 3 and 5 in "Starting the Server" section.](https://github.com/Grasscutters/Grasscutter/wiki/Running)
2. Open the `config.json` that the JAR file generated after running.
3. Find the area of the file.
```
  "GameServer": {
      "Name": "My Server Name",
      "Ip": "0.0.0.0",
      "PublicIp": "<pterodactylIP>",
      "Port": <pterodactylPort>,
      "DispatchServerDatabaseUrl": "<mongoConnectionURL>",
      "DispatchServerDatabaseCollection": "<mongoDatabase>",
  ```
4. Replace `serverName` with your server name.
5. Replace `pterodactylIP` with your Pterodactyl IP. \
   If the IP you have is a website domain (Example: wjd12uq.some-host.com:72392) \
   then follow the steps to get the raw IP address.
   * For Windows, you need to open Command Prompt and type `nslookup <Host>` and you will get a result.
   ```
   Server:  one.one.one.one
   Address:  1.1.1.1

   Non-authoritative answer:
   Name:    wjd12uq.some-host.com
   Address:  N07.4N.IP.4DDR355
   ```
   * Get the IP address in the Non-authoritative answer area.
6. And the config should look like this:
```
  "GameServer": {
      "Name": "My Server Name",
      "Ip": "0.0.0.0",
      "PublicIp": "N07.4N.IP.4DDR355",
      "Port": 72392,
      "DispatchServerDatabaseUrl": "mongo+srv://SERVER:PASSWORD@literally-not-a-mon.go",
      "DispatchServerDatabaseCollection": "databaseName",
  ```
