# How2Breadcutter
<details>
  <summary>Client Errors</summary>
 
  - 4206: Your device isn't connecting to the server properly. Check your proxy settings (Fiddler, mitm, etc) and try again.
    - Potential places for error:
      - The client cannot properly establish an encrypted connection to the local server.
      - The server is not properly handling the query_cur_region request.
      - Your proxy isn't setup properly and isn't redirecting the `query_cur_region` request.
    - Solutions to the problem:
      - Add the keystore.p12 certificate to your system's trusted certificate root authority list.
      - Double-check if you can access [this web URL](https://127.0.0.1/query_cur_region) in your respective browser.
      - Check the settings for the proxy you are using (ex. Fiddler with its Fiddlerscript, MiTMProxy with its Python script, etc.)
</details>
<details>
  <summary>Hosting</summary>
 
  1. [How to host in Pterodactyl](../../blob/main/hosting/pterodactyl.md)
</details>
