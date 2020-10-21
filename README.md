# Coder Cloud - Private Alpha

Access [code-server](https://github.com/cdr/code-server) (VSCode in the browser) from anywhere *without* complex configuration. 
Coder Cloud eliminates the need for configuring SSL, network firewall rules, authentication, etc.


Use your code-server instance from any device, even an iPad, without the setup nightmare. 

Request access to the private alpha [here](https://codercom.typeform.com/to/U4IKyv0W).

## Steps
**1. Start code-server with the new `--link` flag**
```
$ code-server --link
```

**2. Authenticate with Github**

**3. Navigate to the URL shown in the log output**
```
[2020-10-08T21:30:44.847Z] info  Proxying code-server to Coder Cloud, 
you can access your IDE at https://charlie_macbook-cmoog.cdr.co
```

## Usage

## --link
Tell code-server to serve VSCode on a public URL protected by your
Github OAuth authentication. Add an optional string value to specify a custom instance name.
The instance name defaults to your hostname as a fallback.

```
$ code-server --link

<other log output>
[2020-10-08T21:30:44.847Z] info  Proxying code-server to Coder Cloud, you can access your IDE at https://charlie_macbook-cmoog.cdr.co
```

#### Custom instance name

```
$ code-server --link home_dev

<other log output>
[2020-10-08T21:30:44.847Z] info  Proxying code-server to Coder Cloud, you can access your IDE at https://home_dev-cmoog.cdr.co
```

To access web services with your cloud URL, browse to `/proxy/<port>/` (see [code-server FAQ](https://github.com/cdr/code-server/blob/v3.6.0/doc/FAQ.md#how-do-i-securely-access-web-services)).

## Feedback and Support

Please send feedback to [jon@coder.com](mailto:jon@coder.com) or open an [issue](https://github.com/cdr/cloud/issues/new).
