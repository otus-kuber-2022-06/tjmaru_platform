NAME: vault
LAST DEPLOYED: Sun Aug 21 12:22:14 2022
NAMESPACE: microservices-demo
STATUS: deployed
REVISION: 1
NOTES:
Thank you for installing HashiCorp Vault!

Now that you have deployed Vault, you should look over the docs on using
Vault with Kubernetes available here:

https://www.vaultproject.io/docs/


Your release is named vault. To learn more about the release, try:

$ helm status vault
$ helm get manifest vault




Unseal Key 1: AzimNwfCh+MxZKbIoESj1eCngRPiW6mWlYT9dn/HGGk=

Initial Root Token: hvs.fOdJryBL2XL30088y7YKVq2C
k



Key                Value
---                -----
Seal Type          shamir
Initialized        true
Sealed             false
Total Shares       1
Threshold          1
Unseal Progress    0/1
Unseal Nonce       n/a
Version            1.11.2
Build Date         2022-07-29T09:48:47Z
Storage Type       consul
HA Enabled         true


Key                  Value
---                  -----
token                hvs.wa2hnRjOEEpDt39YEw4PyBUz
token_accessor       PKQxSAkIAuTA3sMvMgiXO7ze
token_duration       ∞
token_renewable      false
token_policies       ["root"]
identity_policies    []
policies             ["root"]


Path      Type     Accessor               Description
----      ----     --------               -----------
token/    token    auth_token_ea2f4c10    token based credentials




Key                 Value
---                 -----
refresh_interval    768h
username            otus



====== Data ======
Key         Value
---         -----
password    asajkjkahs
username    otus



Path           Type          Accessor                    Description
----           ----          --------                    -----------
kubernetes/    kubernetes    auth_kubernetes_31baface    n/a
token/         token         auth_token_ea2f4c10         token based credentials



Почему мы смогли записать otus-rw/conﬁg1 но не смогли otus-rw/conﬁg 
потому что политика разрешает создание секретов под otus-rw/* но не разрешает обновлять существующие секреты
