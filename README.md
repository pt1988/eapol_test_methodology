# EAPoL TEST method

## 1. Create configuration file

vi client1.conf

```
network={
        ssid="eduroam"
        key_mgmt=WPA-EAP
        eap=TTLS
        identity="guest"
        anonymous_identity="guest"
        password="guest"
        phase2="auth=MSCHAP"
        #eapol_flags=3
        #
        #  Uncomment the following to perform server certificate validation.
#       ca_cert="/etc/raddb/certs/ca.der"
}
```

## 2. Run eapol_test

```
eapol_test -c client1.conf -a 10.1.1.1 -s testing123 -M xx:xx:xx:xx:xx:xx
```
