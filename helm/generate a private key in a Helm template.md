START
Basic
Front: How to generate a private key in a Helm template?
Back: 
The template function `genPrivateKey` allows to generate a private key encoded into a PEM block. The first param is one of the following:  

- `ecdsa` — elliptic curve DSA key (P256)
- `dsa` — DSA key (L2048N256)
- `rsa` — RSA 4096 key

Source: [https://helm.sh/docs/chart_template_guide/function_list/#genprivatekey](https://helm.sh/docs/chart_template_guide/function_list/#genprivatekey)
<!--ID: 1745135900091-->
END
