# ghw - smart contract vulnerability detection tools part one

## check in w/ mlh 
- bit.ly/scvd1

## goal: utilize python libraries to find vulberabilities in smart contracts in the etherscan api 
- follow the slither tutorial + verify its accuracy by first using the the contracts in the ScrawID repo (can find the smart contracts in the etherscan search contract site)
- installed + debugged slither (changed solc-select versions to match the solidity files taken off of the etherscan dev search tool) 

- older + more dependency based apps - led to more low (or sometimes med-high) vulnerabilities 

examples of vulnerabilities we detected: 
- to debug version issues (usually): solc-select install [version that is = to pragma solidity in sol file]
- then run solc-select use [same version you just installed that is in sol file ]

- to run slither: slither [name of solidity file] 

- test.sol -> severe vulnerabiliy = Unchecked transfer -> solution = SafeERC20
- test3.sol -> severe vulnerabilities = Unchecked transfer, Array Length 
        medium vulnerabilities = division before multiplication, dangerous strict equalities can lead to infinite loop (and potentially infinite loss); contracts that lock eth (dont create locked contracts w/o thinking it thru like an engineer - basically asking questions on all of the possible needed functions/methods), re-entrancy on multiple fronts (can lead to infinite money loss glitch)



## reference the code we worked on + other resources 
- bit.ly/scvd-code

- https://github.com/sujeetc/ScrawlD/tree/main
- https://github.com/crytic/slither?tab=readme-ov-file#how-to-install
- https://etherscan.io/searchcontract


