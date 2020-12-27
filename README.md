# Xray-install

Bash script for installing Xray in operating systems such as CentOS / Debian / OpenSUSE that support systemd.

[Filesystem Hierarchy Standard (FHS)](https://en.wikipedia.org/wiki/Filesystem_Hierarchy_Standard)

```
installed: /usr/local/bin/xray
installed: /usr/local/etc/xray/*.json

installed: /usr/local/share/xray/geoip.dat
installed: /usr/local/share/xray/geosite.dat

installed: /var/log/xray/access.log
installed: /var/log/xray/error.log

installed: /etc/systemd/system/xray.service
installed: /etc/systemd/system/xray@.service
```

## Basic Usage

**Install & Upgrade Xray-core and geodata with User nobody, but will NOT overwrite User in service files**

```
# bash <(curl -L https://github.com/XTLS/Xray-install/raw/main/install-release.sh) install
```

**Update geoip.dat and geosite.dat only**

```
# bash <(curl -L https://github.com/XTLS/Xray-install/raw/main/install-release.sh) install-geodata
```

**Remove Xray, except json and logs**

```
# bash <(curl -L https://github.com/XTLS/Xray-install/raw/main/install-release.sh) remove
```

## Advance

**Install & Upgrade Xray-core and geodata with User root, which will overwrite User in service files**

```
# bash <(curl -L https://github.com/XTLS/Xray-install/raw/main/install-release.sh) install -u root
```

**Install & Upgrade Xray-core without geodata**

```
# bash <(curl -L https://github.com/XTLS/Xray-install/raw/main/install-release.sh) install --without-geodata
```

**Remove Xray, include json and logs**

```
# bash <(curl -L https://github.com/XTLS/Xray-install/raw/main/install-release.sh) remove --purge
```

## More Usage

```
# bash <(curl -L https://github.com/XTLS/Xray-install/raw/main/install-release.sh) help
```
