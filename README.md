# GoPlane

[![Build Status](https://travis-ci.org/osrg/goplane.svg?branch=master)](https://travis-ci.org/osrg/goplane/builds)

GoPlane is an agent for configuring linux network stack via [GoBGP](https://github.com/osrg/gobgp)

```
    +=========================+
    |          GoBGP          |
    +=========================+
                 | <- gRPC API
    +=========================+
    |         GoPlane         |
    +=========================+
                 | <- netfilter
    +=========================+
    |   linux network stack   |
    +=========================+
```

## Install

You need [glide](https://github.com/Masterminds/glide) to resolve goplane's dependencies.

```
$ go get github.com/homoluctus/goplane
$ cd $GOPATH/src/github.com/homoluctus/goplane; glide install
```

## Features
- Flowspec/iptables remote firewall configuration
    - configure firewall using [BGP/FLOWSPEC](https://tools.ietf.org/html/rfc5575) and iptables
    - see [test/iptables](https://github.com/homoluctus/goplane/tree/master/test/iptables) for more details
