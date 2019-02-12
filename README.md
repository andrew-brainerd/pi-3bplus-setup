# Raspberry Pi 3 B+ Setup

My process to set up the Raspberry Pi 3 B+

## Install Raspian

## Create project directory

Create directory at root

```none
> sudo mkdir /projects
```

Assign directory owner

```none
> sudo chown -R pi /projects
```

## Install Node

Get processor architecture (should be `armv7l`)

```none
> uname -m
```

Download NodeJS

```none
> wget https://nodejs.org/dist/v10.15.1/node-v10.15.1-linux-armv7l.tar.xz
```

Unzip that shit and move to install location

```none
> tar -xf node-v10.15.1-linux-armv7l.tar.xz
> cd node-v10.15.1-linux-armv7l
> sudo cp -R * /usr/local/
```

Check versions

```none
> node -v
v10.15.1
```

```none
> npm -v
6.4.1
```

## Install Yarn

```none
> sudo npm i -g yarn
```

## Install Phantom JS

```none
> sudo apt -y install phantomjs
```

## Install Project Dependencies

```none
> yarn install --network-timeout 1000000
```

## General Commands

Get IP Address

```node
> sudo ifconfig
```