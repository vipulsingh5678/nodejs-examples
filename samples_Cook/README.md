# <span id="top">Node.js examples from Cook's book</span> <span style="size:30%;"><a href="../README.md">⬆</a></span>

<table style="font-family:Helvetica,Arial;font-size:14px;line-height:1.6;">
  <tr>
  <td style="border:0;padding:0 10px 0 0;min-width:120px;"><a href="https://nodejs.org/" rel="external" title="Node.js"><img src="../docs/images/nodejs.svg" width="120" alt="Node.js project"/></a></td>
  <td style="border:0;padding:0;vertical-align:text-top;">Directory <strong><code>samples_Cook\</code></strong> contains <a href="https://nodejs.org/" rel="external" title="Node.js">Node.js</a> examples presented in <a href="https://www.amazon.com/Node-js-Essentials-Fabian-Cook/dp/1785284924">Fabian Cook's book</a> "<i>Node.js Essentials</i>" (Packt, 2015).</td>
  </tr>
</table>

> **:mag_right:** The numbering used below &ndash; eg. `03` in example `03_basic_auth` &ndash; refers to the chapter where the example belongs to.

## <span id="03_basic_auth">`03_basic_auth`</span>

Command **`npm start`** starts the server application which listen to our requests on port **`8180`** (defined in file [**`config.json`**](./03_basic_auth/config_TEMPLATE.json)):

<pre style="font-size:80%;">
<b>&gt; <a href="https://docs.microsoft.com/en-us/windows-server/administration/windows-commands/cd">cd</a></b>
N:\samples_Cook\03_basic_auth
&nbsp;
<b>&gt; <a href="https://docs.microsoft.com/en-us/windows-server/administration/windows-commands/start">start</a> "basic_auth" npm start</b>

> basic_auth@1.0.0 start N:\samples_Cook\03_basic_auth
> node app/app.js

[2018-05-10 19:43:17 INFO] (app.js) Listening on port 8180
[2018-05-10 19:43:33 INFO] (app.js) Requested URL: /
[2018-05-10 19:43:33 INFO] (app.js) Requested URL: /
[2018-05-10 19:43:33 INFO] (app.js) Requested URL: /
</pre>

Command **`npm run client`** sends several requests to the server: 

<pre style="font-size:80%;">
<b>&gt; <a href="https://docs.npmjs.com/cli/v6/commands/npm-run-script">npm run</a> client</b>

> basic_auth@1.0.0 client N:\samples_Cook\03_basic_auth
> node npm_scripts/start_client.js

en /
fr /
de /
</pre>

## <span id="03_bear_token">`03_bear_token`</span>

Command [**`npm start`**](https://docs.npmjs.com/cli/v6/commands/npm-start) starts the server application which listen to our requests on port **`8180`** (defined in file [**`config.json`**](./03_bear_token/config_TEMPLATE.json)):

<pre style="font-size:80%;">
<b>&gt; <a href="https://docs.microsoft.com/en-us/windows-server/administration/windows-commands/start">start</a> "bear_token" <a href="https://docs.npmjs.com/cli/v6/commands/npm-start">npm start</a></b>

> bearer_token@1.0.0 start N:\samples_Cook\03_bearer_token
> node .

[2020-07-14 19:06:21 INFO] (app.js) Listening on port 8180
</pre>

Command **`npm run client`** sends a `POST` request to the server (endpoint `/login`): 

<pre style="font-size:80%;">
<b>&gt; <a href="https://docs.npmjs.com/cli/v6/commands/npm-run-script">npm run</a> client</b>

> bearer_token@1.0.0 client N:\samples_Cook\03_bearer_token
> node npm_scripts/start_client.js

[2020-07-14 19:08:02 INFO] (start_client.js) login: username=foo
[2020-07-14 19:08:02 INFO] (start_client.js) curl -H "User-Agent: Mozilla/5.0" -H "Content-Type: application/json" -X POST -d "{\"username\": \"foo\", \"password\":\"bar\"}" http://127.0.0.1:8180/login
token=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6MSwidXNlcm5hbWUiOiJmb28iLCJpYXQiOjE1OTQ3NDY0ODJ9.xCpqkBxRTZ-JfC_HpB15GKur4tjJNuHEWFqhkXkCqtM
</pre>

## <span id="03_bear_token2">`03_bear_token2`</span>

Command [**`npm start`**](https://docs.npmjs.com/cli/v6/commands/npm-start) starts the server application which listen to our requests on port **`8180`** (defined in file [**`config.json`**](./03_bear_token2/config_TEMPLATE.json)):

<pre style="font-size:80%;">
<b>&gt; <a href="https://docs.microsoft.com/en-us/windows-server/administration/windows-commands/start">start</a> "bear_token2" <a href="https://docs.npmjs.com/cli/v6/commands/npm-start">npm start</a></b>

> bearer_token2@1.0.0 start N:\samples_Cook\03_bearer_token2
> node .

[2021-06-02 12:34:21 INFO] (app.js) Listening on port 8180
</pre>


Command **`npm run client`** sends a `POST` request to the server (endpoint `/login`): 

<pre style="font-size:80%;">
<b>&gt; <a href="https://docs.npmjs.com/cli/v6/commands/npm-run-script">npm run</a> client</b>

> bearer_token@1.0.0 client N:\samples_Cook\03_bearer_token2
> node npm_scripts/start_client.js

[2021-06-02 12:36:18 INFO] (start_client.js) login: username=foo
[2021-06-02 12:36:18 INFO] (start_client.js) curl -H "User-Agent: Mozilla/5.0" -H "Content-Type: application/json" -X POST -d "{\"username\": \"foo\", \"password\":\"bar\"}" http://127.0.0.1:8180/login
token=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6MSwidXNlcm5hbWUiOiJmb28iLCJpYXQiOjE2MjI2MzAxNzl9.-vkWn3KQVZdvZh4Eboe1AA7g3vINa7g71c-_uZcQ1j0
[2021-06-02 12:36:19 INFO] (start_client.js) curl -H "Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6MSwidXNlcm5hbWUiOiJmb28iLCJpYXQiOjE2MjI2MzAxNzl9.-vkWn3KQVZdvZh4Eboe1AA7g3vINa7g71c-_uZcQ1j0" -X GET http://127.0.0.1:8180/userinfo
[2021-06-02 12:36:19 INFO] (start_client.js) json={"id":1,"username":"foo"}
</pre>

<!--
## <span id="03_oauth">`03_oauth`</span>


## <span id="04_logging_bunyan">`04_logging_bunyan`</span>
-->

## <span id="04_logging_morgan">`04_logging_morgan`</span>

*WIP*

***

*[mics](https://lampwww.epfl.ch/~michelou/)/April 2022* [**&#9650;**](#top)
<span id="bottom">&nbsp;</span>

<!-- link refs -->
