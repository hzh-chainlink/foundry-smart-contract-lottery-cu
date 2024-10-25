## Deploy（你需要在 HelperConfig 中设置自己的订阅 ID 和对应的钱包地址）
```shell
(base) alex@DESKTOP-UKE5TJQ:~/share/foundry-smart-contract-lottery-cu$ make deploy ARGS="--network sepolia"
[⠊] Compiling...
No files changed, compilation skipped
Traces:
  [12122214] DeployRaffle::run()
    ├─ [4977223] → new HelperConfig@0xC7f2Cf4845C6db0e1a1e91ED41Bcd0FcC1b0E141
    │   └─ ← [Return] 22963 bytes of code
    ├─ [6064979] → new AddConsumer@0xdaE97900D4B184c5D2012dcdB658c008966466DD
    │   └─ ← [Return] 30177 bytes of code
    ├─ [2305] HelperConfig::getConfig()
    │   └─ ← [Return] NetworkConfig({ subscriptionId: 78115397582864920796890914656003262667807066576170740381173807521345994681430 [7.811e76], gasLane: 0x787d74caea10b2b357790d5b5247c2f63d1d91572a9846f780606e4d953677ae, automationUpdateInterval: 30, raffleEntranceFee: 10000000000000000 [1e16], callbackGasLimit: 500000 [5e5], vrfCoordinatorV2_5: 0x9DdfaCa8183c41ad55329BdeeD9F6A8d53168B1B, link: 0x779877A7B0D9E8603169DdbD7836e478b4624789, account: 0xDBbf53236940312438517a348e8D1a3C43cB38A2 })
    ├─ [0] VM::startBroadcast(0xDBbf53236940312438517a348e8D1a3C43cB38A2)
    │   └─ ← [Return] 
    ├─ [884145] → new Raffle@0x67fE96137d03Cc3F8d1aE62a41F91EF717C627Bd
    │   └─ ← [Return] 4070 bytes of code
    ├─ [0] VM::stopBroadcast()
    │   └─ ← [Return] 
    ├─ [82033] AddConsumer::addConsumer(Raffle: [0x67fE96137d03Cc3F8d1aE62a41F91EF717C627Bd], VRFCoordinatorV2_5: [0x9DdfaCa8183c41ad55329BdeeD9F6A8d53168B1B], 78115397582864920796890914656003262667807066576170740381173807521345994681430 [7.811e76], 0xDBbf53236940312438517a348e8D1a3C43cB38A2)
    │   ├─ [0] console::log("Adding consumer contract: ", Raffle: [0x67fE96137d03Cc3F8d1aE62a41F91EF717C627Bd]) [staticcall]
    │   │   └─ ← [Stop] 
    │   ├─ [0] console::log("Using vrfCoordinator: ", VRFCoordinatorV2_5: [0x9DdfaCa8183c41ad55329BdeeD9F6A8d53168B1B]) [staticcall]
    │   │   └─ ← [Stop] 
    │   ├─ [0] console::log("On ChainID: ", 11155111 [1.115e7]) [staticcall]
    │   │   └─ ← [Stop] 
    │   ├─ [0] VM::startBroadcast(0xDBbf53236940312438517a348e8D1a3C43cB38A2)
    │   │   └─ ← [Return] 
    │   ├─ [73242] VRFCoordinatorV2_5::addConsumer(78115397582864920796890914656003262667807066576170740381173807521345994681430 [7.811e76], Raffle: [0x67fE96137d03Cc3F8d1aE62a41F91EF717C627Bd])
    │   │   ├─ emit SubscriptionConsumerAdded(subId: 78115397582864920796890914656003262667807066576170740381173807521345994681430 [7.811e76], consumer: Raffle: [0x67fE96137d03Cc3F8d1aE62a41F91EF717C627Bd])
    │   │   └─ ← [Stop] 
    │   ├─ [0] VM::stopBroadcast()
    │   │   └─ ← [Return] 
    │   └─ ← [Stop] 
    └─ ← [Return] Raffle: [0x67fE96137d03Cc3F8d1aE62a41F91EF717C627Bd], HelperConfig: [0xC7f2Cf4845C6db0e1a1e91ED41Bcd0FcC1b0E141]


Script ran successfully.

== Return ==
0: contract Raffle 0x67fE96137d03Cc3F8d1aE62a41F91EF717C627Bd
1: contract HelperConfig 0xC7f2Cf4845C6db0e1a1e91ED41Bcd0FcC1b0E141

== Logs ==
  Adding consumer contract:  0x67fE96137d03Cc3F8d1aE62a41F91EF717C627Bd
  Using vrfCoordinator:  0x9DdfaCa8183c41ad55329BdeeD9F6A8d53168B1B
  On ChainID:  11155111

## Setting up 1 EVM.
==========================
Simulated On-chain Traces:

  [884145] → new Raffle@0x67fE96137d03Cc3F8d1aE62a41F91EF717C627Bd
    └─ ← [Return] 4070 bytes of code

  [73242] VRFCoordinatorV2_5::addConsumer(78115397582864920796890914656003262667807066576170740381173807521345994681430 [7.811e76], Raffle: [0x67fE96137d03Cc3F8d1aE62a41F91EF717C627Bd])
    ├─ emit SubscriptionConsumerAdded(subId: 78115397582864920796890914656003262667807066576170740381173807521345994681430 [7.811e76], consumer: Raffle: [0x67fE96137d03Cc3F8d1aE62a41F91EF717C627Bd])
    └─ ← [Stop] 


==========================

Chain 11155111

Estimated gas price: 0.328411235 gwei

Estimated total gas used for script: 1452745

Estimated amount required: 0.000477097779590075 ETH

==========================

##### sepolia
✅  [Success]Hash: 0xceba4ee373978eb7ade2999a0bff191a4c17d6e44a90a161b50102a49427e1e6
Contract Address: 0x67fE96137d03Cc3F8d1aE62a41F91EF717C627Bd
Block: 6940841
Paid: 0.000210785246669648 ETH (1010723 gas * 0.208548976 gwei)


##### sepolia
✅  [Success]Hash: 0xd8bb1048fb630c90da0083702ac2fad2a83a3bd110cd764aa7670181cc27dac9
Block: 6940841
Paid: 0.000019850942829536 ETH (95186 gas * 0.208548976 gwei)

✅ Sequence #1 on sepolia | Total Paid: 0.000230636189499184 ETH (1105909 gas * avg 0.208548976 gwei)
                                                                                                                       

==========================

ONCHAIN EXECUTION COMPLETE & SUCCESSFUL.
##
Start verification for (1) contracts
Start verifying contract `0x67fE96137d03Cc3F8d1aE62a41F91EF717C627Bd` deployed on sepolia

Submitting verification for [src/Raffle.sol:Raffle] 0x67fE96137d03Cc3F8d1aE62a41F91EF717C627Bd.

Submitting verification for [src/Raffle.sol:Raffle] 0x67fE96137d03Cc3F8d1aE62a41F91EF717C627Bd.
Submitted contract for verification:
        Response: `OK`
        GUID: `ubuhy5i4kjd6mhsspeedtzyseyf4xyghudxe2fnz9hviqjxigm`
        URL: https://sepolia.etherscan.io/address/0x67fe96137d03cc3f8d1ae62a41f91ef717c627bd
Contract verification status:
Response: `NOTOK`
Details: `Pending in queue`
Contract verification status:
Response: `OK`
Details: `Pass - Verified`
Contract successfully verified
All (1) contracts were verified!

Transactions saved to: /home/alex/share/foundry-smart-contract-lottery-cu/broadcast/DeployRaffle.s.sol/11155111/run-latest.json

Sensitive values saved to: /home/alex/share/foundry-smart-contract-lottery-cu/cache/DeployRaffle.s.sol/11155111/run-latest.json
```

## 在执行这一步之前，你应该已经完成了 Upkeep 的注册，使用自定义逻辑，注册的合约应该是 Raffle
## Run（如果成功，你会发现钱包余额先减少 0.1，过一会儿这 0.1 会被抽奖合约自动返还，因为只有你一个人参与抽奖）
```shell
(base) alex@DESKTOP-UKE5TJQ:~/share/foundry-smart-contract-lottery-cu$ cast send 0x67fE96137d03Cc3F8d1aE62a41F91EF717C627Bd "enterRaffle()" --value 0.1et
her --private-key $PRIVATE_KEY --rpc-url $SEPOLIA_RPC_URL

blockHash               0x4662ec6fcb40deab5a10d2edc8a251f9be1325a9bd99779340bd246a8679447b
blockNumber             6940924
contractAddress         
cumulativeGasUsed       7440450
effectiveGasPrice       607928137
from                    0xDBbf53236940312438517a348e8D1a3C43cB38A2
gasUsed                 68874
logs                    [{"address":"0x67fe96137d03cc3f8d1ae62a41f91ef717c627bd","topics":["0x0805e1d667bddb8a95f0f09880cf94f403fb596ce79928d9f29b74203ba284d4","0x000000000000000000000000dbbf53236940312438517a348e8d1a3c43cb38a2"],"data":"0x","blockHash":"0x4662ec6fcb40deab5a10d2edc8a251f9be1325a9bd99779340bd246a8679447b","blockNumber":"0x69e8fc","transactionHash":"0x48234bb862de36a6160cbd10acba808d490f98f5d85cf6394cdb4d48edbc6d7e","transactionIndex":"0x37","logIndex":"0x51","removed":false}]
logsBloom               0x00000000000000000000000000000000000000000000000000000000000000000000000000100000000000000005000000000000000000000000000000000000000000000000000000000004000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000080000000008000000000000000004000000000000000000000000000000000000000000000000000000
root                    
status                  1 (success)
transactionHash         0x48234bb862de36a6160cbd10acba808d490f98f5d85cf6394cdb4d48edbc6d7e
transactionIndex        55
type                    2
blobGasPrice            
blobGasUsed             
authorizationList       
to                      0x67fE96137d03Cc3F8d1aE62a41F91EF717C627Bd
```


> ! Updates from Video
> 1. V2.5 of Chainlink VRF uses a `uint256` as a subId instead of a `uint64` this repo has a comment to reflect that. We added a mock in case you'd like to work with version 2.5.
> 2. We use `0.1.0` of the `foundry-devops` package which doesn't need to have `ffi=true`

# Foundry Smart Contract Lottery

This is a section of the Cyfrin Foundry Solidity Course.

*[⭐️ (3:04:09) | Lesson 9: Foundry Smart Contract Lottery](https://www.youtube.com/watch?v=sas02qSFZ74&t=11049s)*

- [Foundry Smart Contract Lottery](#foundry-smart-contract-lottery)
- [Getting Started](#getting-started)
  - [Requirements](#requirements)
  - [Quickstart](#quickstart)
    - [Optional Gitpod](#optional-gitpod)
- [Usage](#usage)
  - [Start a local node](#start-a-local-node)
  - [Library](#library)
  - [Deploy](#deploy)
  - [Deploy - Other Network](#deploy---other-network)
  - [Testing](#testing)
    - [Test Coverage](#test-coverage)
- [Deployment to a testnet or mainnet](#deployment-to-a-testnet-or-mainnet)
  - [Scripts](#scripts)
  - [Estimate gas](#estimate-gas)
- [Formatting](#formatting)
- [Additional Info:](#additional-info)
  - [Let's talk about what "Official" means](#lets-talk-about-what-official-means)
  - [Summary](#summary)
- [Thank you!](#thank-you)

# Getting Started

## Requirements

- [git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
  - You'll know you did it right if you can run `git --version` and you see a response like `git version x.x.x`
- [foundry](https://getfoundry.sh/)
  - You'll know you did it right if you can run `forge --version` and you see a response like `forge 0.2.0 (816e00b 2023-03-16T00:05:26.396218Z)`

## Quickstart

```
git clone https://github.com/Cyfrin/foundry-smart-contract-lottery-cu
cd foundry-smart-contract-lottery-cu
forge build
```

### Optional Gitpod

If you can't or don't want to run and install locally, you can work with this repo in Gitpod. If you do this, you can skip the `clone this repo` part.

[![Open in Gitpod](https://gitpod.io/button/open-in-gitpod.svg)](https://gitpod.io/#github.com/Cyfrin/foundry-smart-contract-lottery-cu)

# Usage

## Start a local node

```
make anvil
```

## Library

If you're having a hard time installing the chainlink library, you can optionally run this command. 

```
forge install smartcontractkit/chainlink-brownie-contracts@0.6.1 --no-commit
```

## Deploy

This will default to your local node. You need to have it running in another terminal in order for it to deploy.

```
make deploy
```

## Deploy - Other Network

[See below](#deployment-to-a-testnet-or-mainnet)

## Testing

We talk about 4 test tiers in the video.

1. Unit
2. Integration
3. Forked
4. Staging

This repo we cover #1 and #3.

```
forge test
```

or

```
forge test --fork-url $SEPOLIA_RPC_URL
```

### Test Coverage

```
forge coverage
```

# Deployment to a testnet or mainnet

1. Setup environment variables

You'll want to set your `SEPOLIA_RPC_URL` and `PRIVATE_KEY` as environment variables. You can add them to a `.env` file, similar to what you see in `.env.example`.

- `PRIVATE_KEY`: The private key of your account (like from [metamask](https://metamask.io/)). **NOTE:** FOR DEVELOPMENT, PLEASE USE A KEY THAT DOESN'T HAVE ANY REAL FUNDS ASSOCIATED WITH IT.
  - You can [learn how to export it here](https://metamask.zendesk.com/hc/en-us/articles/360015289632-How-to-Export-an-Account-Private-Key).
- `SEPOLIA_RPC_URL`: This is url of the sepolia testnet node you're working with. You can get setup with one for free from [Alchemy](https://alchemy.com/?a=673c802981)

Optionally, add your `ETHERSCAN_API_KEY` if you want to verify your contract on [Etherscan](https://etherscan.io/).

1. Get testnet ETH

Head over to [faucets.chain.link](https://faucets.chain.link/) and get some testnet ETH. You should see the ETH show up in your metamask.

2. Deploy

```
make deploy ARGS="--network sepolia"
```

This will setup a ChainlinkVRF Subscription for you. If you already have one, update it in the `scripts/HelperConfig.s.sol` file. It will also automatically add your contract as a consumer.

3. Register a Chainlink Automation Upkeep

[You can follow the documentation if you get lost.](https://docs.chain.link/chainlink-automation/compatible-contracts)

Go to [automation.chain.link](https://automation.chain.link/new) and register a new upkeep. Choose `Custom logic` as your trigger mechanism for automation. Your UI will look something like this once completed:

![Automation](./img/automation.png)

## Scripts

After deploying to a testnet or local net, you can run the scripts.

Using cast deployed locally example:

```
cast send <RAFFLE_CONTRACT_ADDRESS> "enterRaffle()" --value 0.1ether --private-key <PRIVATE_KEY> --rpc-url $SEPOLIA_RPC_URL
```

or, to create a ChainlinkVRF Subscription:

```
make createSubscription ARGS="--network sepolia"
```

## Estimate gas

You can estimate how much gas things cost by running:

```
forge snapshot
```

And you'll see an output file called `.gas-snapshot`

# Formatting

To run code formatting:

```
forge fmt
```

# Additional Info:
Some users were having a confusion that whether Chainlink-brownie-contracts is an official Chainlink repository or not. Here is the info.
Chainlink-brownie-contracts is an official repo. The repository is owned and maintained by the chainlink team for this very purpose, and gets releases from the proper chainlink release process. You can see it's still the `smartcontractkit` org as well.

https://github.com/smartcontractkit/chainlink-brownie-contracts

## Let's talk about what "Official" means
The "official" release process is that chainlink deploys it's packages to [npm](https://www.npmjs.com/package/@chainlink/contracts). So technically, even downloading directly from `smartcontractkit/chainlink` is wrong, because it could be using unreleased code.

So, then you have two options:

1. Download from NPM and have your codebase have dependencies foreign to foundry
2. Download from the chainlink-brownie-contracts repo which already downloads from npm and then packages it nicely for you to use in foundry.
## Summary
1. That is an official repo maintained by the same org
2. It downloads from the official release cycle `chainlink/contracts` use (npm) and packages it nicely for digestion from foundry.


# Thank you!

If you appreciated this, feel free to follow me or donate!

ETH/Arbitrum/Optimism/Polygon/etc Address: 0x9680201d9c93d65a3603d2088d125e955c73BD65

[![Patrick Collins Twitter](https://img.shields.io/badge/Twitter-1DA1F2?style=for-the-badge&logo=twitter&logoColor=white)](https://twitter.com/PatrickAlphaC)
[![Patrick Collins YouTube](https://img.shields.io/badge/YouTube-FF0000?style=for-the-badge&logo=youtube&logoColor=white)](https://www.youtube.com/channel/UCn-3f8tw_E1jZvhuHatROwA)
[![Patrick Collins Linkedin](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/patrickalphac/)
[![Patrick Collins Medium](https://img.shields.io/badge/Medium-000000?style=for-the-badge&logo=medium&logoColor=white)](https://medium.com/@patrick.collins_58673/)
