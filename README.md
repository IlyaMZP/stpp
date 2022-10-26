# stpp
A small script to atomate creation of a VPN tunnel based on stunnel (cryptopro fork) and pppd.

# Example usage
On the server side just run:

`stpp --server -p=1234 -v=2 -c=2DF3BD26617D64AA89F850862D11D8B660CF24FE`

Where `1234` is the port to listen on, `2` is the verification level for stunnel and `2DF3BD26617D64AA89F850862D11D8B660CF24FE` is a certificate thumbprint. A certificate path may be specified instead.

On the client side run:

`stpp -p=1234 -a=192.168.235.130 -v=0`

You may specify a certificate with the same argument for two-way TLS.
