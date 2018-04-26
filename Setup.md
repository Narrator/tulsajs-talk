### Environment Setup

This is an easy way to setup the whole environment using nvm. Otherwise, you can install it using the official [Package Manager](https://nodejs.org/en/download/package-manager/) according to your OS.

**Note:** If you're on Windows, you can use [nvm-windows](https://github.com/coreybutler/nvm-windows). After that [Install MongoDB](#install-mongodb) and [LoopBack CLI]().

Loopback has documentation on [installation on windows](https://loopback.io/doc/en/lb3/Installing-on-Windows.html), but it's **outdated**.

Installation steps below are only for UNIX type systems like MacOS, Linux etc.

**If you already have `Node 8.11.1`, `MongoDB 3.6` installed, you can just directly [install the LoopBack CLI](#).**

### Install [NVM](https://github.com/creationix/nvm)
 Using Curl
```
curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.9/install.sh | bash
```

Using Wget
```
wget -qO- https://raw.githubusercontent.com/creationix/nvm/v0.33.9/install.sh | bash
```

### Install [Node LTS](http://node.green/)

Please install version `8.11.1`. The aliases for Node  LTS versions are like so: `4.9.1 => Argon`, `6.14.1 => Boron` and `8.11.1 => Carbon`. LoopBack 3.x (which we're going to use), hasn't [fully caught up](https://loopback.io/doc/en/lb4/Crafting-LoopBack-4.html#objectives) with a lot of ES2015 features, but we can try to use some in our app.

```
nvm ls-remote | grep "Latest LTS" // Lists all the LTS versions
nvm install --lts

nvm install --lts=carbon
```

### Install MongoDB

Follow [these instructions](https://docs.mongodb.com/manual/administration/install-community/) for installation.

##### Manage `mongod`

```
sudo systemctl stop mongod.service # Stop mongod
sudo systemctl start mongod.service # Start mongod
sudo systemctl status mongod.service # Shows the status
```

### Install LoopBack CLI

Install it globally

```
npm install -g loopback-cli
```

That's it!
