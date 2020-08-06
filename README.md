<p align="center">
<a href="https://bayudwiyansatria.github.io/nginx-external-lb-k8s-ha/">
<img src="https://cdn.bayudwiyansatria.com/assets/logo-full.png" width="100%" />
</a>
<br>
</p>
<p align="center">
<a href="#">
<img src="https://img.shields.io/badge/%20Platforms-Windows%20/%20Linux-blue.svg?style=flat-square" alt="Platforms" />
</a>
<a href="https://bayudwiyansatria.github.io/nginx-external-lb-k8s-ha/blob/master/LICENSE">
<img src="https://img.shields.io/badge/%20Licence-MIT-green.svg?style=flat-square" alt="license" />
</a>
</p>
<p align="center">
<a href="https://github.com/bayudwiyansatria/nginx-external-lb-k8s-ha/blob/master/CODE_OF_CONDUCT.md">
<img src="https://img.shields.io/badge/Community-Code%20of%20Conduct-orange.svg?style=flat-squre" alt="Code of Conduct" />
</a>
<a href="https://github.com/bayudwiyansatria/nginx-external-lb-k8s-ha/blob/master/SUPPORT.md">
<img src="https://img.shields.io/badge/Community-Support-red.svg?style=flat-square" alt="Support" />
</a>
<a href="https://github.com/bayudwiyansatria/nginx-external-lb-k8s-ha/blob/master/CONTRIBUTING.md">
<img src="https://img.shields.io/badge/%20Community-Contribution-yellow.svg?style=flat-square" alt="Contribution" />
</a>
</p>
<hr>

# NGINX External Load Balancing For Kubernetes HA

[![Contributor Covenant](https://img.shields.io/badge/Contributor%20Covenant-v1.4%20adopted-ff69b4.svg)](CODE_OF_CONDUCT.md)

![Github Actions](https://github.com/bayudwiyansatria/nginx-external-lb-k8s-ha/workflows/Development/badge.svg)

Load balancing refers to efficiently distributing network traffic across multiple backend servers.

NGINX can proxy and load balance Transmission Control Protocol) (TCP) traffic. TCP is the protocol for many popular applications and services, such as LDAP, MySQL, and RTMP. NGINX also proxy and load balance UDP traffic. UDP (User Datagram Protocol) is the protocol for many popular non-transactional applications, such as DNS, syslog, and RADIUS.


## Table of Contents

* [Dependencies](#dependencies)
* [Prerequisites](#prerequisites)
* [Installation](#installation)
* [Development](#development)
* [Usage](#usage)
* [Contributing](#contributing)
* [License](#license)

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

### Prerequisites

- latest NGINX Open Source built with the `--with-stream` configuration flag. latest nginx from packages manager such `apt` or `yum` already have `--with-stream`.
- An application, database, or service that communicates over TCP or UDP
- Upstream servers, each running the same instance of the application, database, or service


### Installation

1. Install with package manager

Ubuntu & Debian

```shell
$ apt-get -y install nginx;
```

RHEL & Centos

```shell
$ yum -y install nginx;
```

2. Clone repository put it to installation path of nginx.

```shell
$ rm -rf /etc/nginx && cd /etc/
```

```shell
$ git clone https://github.com/bayudwiyansatria/nginx-external-lb-k8s-ha nginx
```

3. Put your `ip_public` located at `conf.d/loadbalancing/apiserver.conf`

```shell
$ vi /etc/nginx/conf.d/loadbalancing/apiserver.conf
```

4. Test configration

```shell
$ nginx -t
```

5. Start and enable nginx

```
$ systemctl restart nginx && systemctl enable nginx;
```

## Development

-*Release 1.0* : **2020, August**.

## Usage

Nginx Load balancing for High Avability Kubernetes (k8s) Services.

## Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

Looking to contribute to our code but need some help? There's a few ways to get information:

* Connect with us on [Twitter](https://twitter.com/bayudsatria)
* Like us on [Facebook](https://facebook.com/PBayuDSatria)
* Follow us on [LinkedIn](https://linkedin.com/in/bayudwiyansatria)
* Subscribe us on [Youtube](https://youtube.com/channel/UCihxWj1rtheK73mGdrf0OiA)
* Pay a visit at [Website](https://www.bayudwiyansatria.com)
* Log an issue here on github

## Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/bayudwiyansatria/nginx-external-lb-k8s-ha/tags).

## Authors

* **[Bayu Dwiyan Satria](https://github.com/bayudwiyansatria)** 

## Reference

- [NGINX TCP and UDP Load Balancing](https://docs.nginx.com/nginx/admin-guide/load-balancer/tcp-udp-load-balancer/)

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details

<p> Copyright &copy; 2020 Public Use. All Rights Reserved.

## Acknowledgments

* Hat tip to anyone whose code was used
* Inspiration
* etc
