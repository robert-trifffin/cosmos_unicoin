# cosmos_unicoin


### Install

```
dep ensure --v

go install ./cmd/uniswapd
go install ./cmd/uniswapcli
```

### Geneate Genesis file

```
uniswapd init --chain-id uniswap-v1 --moniker dsrv
vi ~/.uniswapd/config/genesis.json

//add more accounts to genesis.json
//generate new key
uniswapcli keys list
uniswapcli keys add account1
```

NAME:   TYPE:   ADDRESS:                                                PUBKEY:
account1        local   uniswap1gd5tnlxtlckx0tm4384xmqzvkh0k7mpy2mvnwh  uniswappub1addwnpepqfvx74c2609wkhy2py3cj7wa0z4glv6e50deyeheyktswevtvwvjc3nevc2

**Important** write this seed phrase in a safe place.
It is the only way to recover your account if you ever forget your password.

slender detect suffer silver panic nature country balance entry unfold holiday legal noble car month remain lonely source mango hammer ankle ordinary law immune

```
uniswapcli keys add account2
```

NAME:   TYPE:   ADDRESS:                                                PUBKEY:
account2        local   uniswap1lwqfqnz7svnp0qs56qheckdqkfa2kqvxc7l2wp  uniswappub1addwnpepqv96psp37y9l6gjg53mrwa2xxzvml3q5wrmf4ujamn70lchly5t57fzjaql

**Important** write this seed phrase in a safe place.
It is the only way to recover your account if you ever forget your password.

risk fancy gun carbon shrimp air boy away elegant dawn wool cloth portion leave auto correct rocket scout depart fire organ squirrel spike unfold


### Start Blockchain

```
uniswapd start
```

### Query accounts

```
uniswapcli query account uniswap1gd5tnlxtlckx0tm4384xmqzvkh0k7mpy2mvnwh --trust-node
uniswapcli query account uniswap1lwqfqnz7svnp0qs56qheckdqkfa2kqvxc7l2wp --trust-node
```

### Send Coin

```
uniswapcli tx send --from uniswap1gd5tnlxtlckx0tm4384xmqzvkh0k7mpy2mvnwh --to uniswap1lwqfqnz7svnp0qs56qheckdqkfa2kqvxc7l2wp --chain-id uniswap-v1 --amount 500uniA

uniswapcli tx send --from uniswap1gd5tnlxtlckx0tm4384xmqzvkh0k7mpy2mvnwh --to uniswap1lwqfqnz7svnp0qs56qheckdqkfa2kqvxc7l2wp --chain-id uniswap-v1 --amount 500uniB
```


