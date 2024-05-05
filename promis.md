 I promise to never use my private key associated with real money in plain text

COMMANDS

source .env # add enviroment variables a nuestro shell
echo $PRIVATE_KEY # show
forge script script/DeploySimpleStorage.s.sol --rpc-url $RPC_URL --broadcast --private-key $PRIVATE_KEY

## encrypt private key with password

cast wallet import defaultKey --interactive
cast wallet list

## defaultKey Address (sender)

0xd08c5a6f2ff12fb257978adce5589d48b1e2ac40

## delete history

history -c
rm .bash_history
