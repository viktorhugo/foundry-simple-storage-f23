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

forge script script/DeploySimpleStorage.s.sol:DeploySimpleStorage --rpc-url $RPC_URL --broadcast --sender $ADDRESS_SENDER  

forge script script/DeploySimpleStorage.s.sol:DeploySimpleStorage --rpc-url $RPC_URL --account defaultKey --sender $ADDRESS_SENDER --broadcast

## SEND

cast send 0xD61cE1d0D3a431756067504706b693279A2751F5 "store(uint256)" 123 --rpc-url $RPC_URL --account defaultKey

## Call

cast call 0xD61cE1d0D3a431756067504706b693279A2751F5 "retrieve()" --rpc-url $RPC_URL --account defaultKey

## convert

cast --to-base 0x000000000000000000000000000000000000000000000000000000000000007b dec

## exec transaction on sepolia

forge script script/DeploySimpleStorage.s.sol:DeploySimpleStorage --rpc-url $SEPOLIA_RPC_URL --private-key $PRIVATE_KEY_METAMASK --broadcast
