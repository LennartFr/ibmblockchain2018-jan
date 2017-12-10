# Introduction - concepts and products
## October 2008 It all started with Satoshi Nakamoto and his paper [Bitcoin: A Peer-to-Peer Electronic Cash System](https://bitcoin.org/bitcoin.pdf) 
which addressed a key problem in electronic commerce:
~~~
A purely peer-to-peer version of electronic cash would allow online payments to be sent directly 
from one party to another without going through a financial institution. 

Digital signatures provide part of the solution, but the main benefits are lost if a trusted third party 
is still required to prevent double-spending.

We propose a solution to the double-spending problem using a peer-to-peer network.
~~~

# Blockchain and BitCoin

* Assets over cryptocurrency
* Identity over anonymity
* Selective endorsement (consensus) over proof of work

<img src="https://farm5.staticflickr.com/4503/37148677233_71edc5a37b_o.png" width="1041" height="53" alt="blueband">

# Overview of the Hyperledger architecture

### The flow with one SDK

<img src="https://farm5.staticflickr.com/4479/37162470013_1309212044_b.jpg" width="1024" height="513" alt="Hyperledger Architecture">

### The flow with two and more SDKs

<img src="https://farm5.staticflickr.com/4506/37882671951_5f4f08348a_o.png" width="1142" height="635" alt="Hyper Ivan 2">

### The Blockchain and State database.

<img src="https://github.com/LennartFr/Blockchain-at-Galvanize/blob/master/Hyperledger%20LevelDB.PNG">

### Ordering service

<img src="https://www.ibm.com/developerworks/cloud/library/cl-top-technical-advantages-of-hyperledger-fabric-for-blockchain-networks/fig1.png">

### Blockchain Ledger

<img src="https://farm5.staticflickr.com/4496/37833953496_fa03154139_o.png" width="837" height="421" alt="Ivan Blockchain">

# Hyperledger Fabric and its docker images 

<img src="https://farm5.staticflickr.com/4506/23967210328_2ab9949bdb_o.png" width="701" height="812" alt="hyper docker">

<img src="https://farm5.staticflickr.com/4503/37148677233_71edc5a37b_o.png" width="1041" height="53" alt="blueband">


# Where do we go from here?

<img src="https://farm5.staticflickr.com/4338/36822231841_bc13a7147a_z.jpg" width="640" height="164" alt="IBMBlockchain1">

[Blockchain for Dummies](https://public.dhe.ibm.com/common/ssi/ecm/xi/en/xim12354usen/XIM12354USEN.PDF)


## IBM has a series of Developer Journeys covering various aspects of Blockchain, with more being added regularly. 

* https://developer.ibm.com/code/journey/build-your-first-blockchain-application/
* https://developer.ibm.com/code/journey/create-and-execute-blockchain-smart-contracts/
* https://developer.ibm.com/code/journey/implement-fda-food-supplier-verification-program-on-hyperledger-composer/
* https://developer.ibm.com/code/journey/build-a-blockchain-network/
* https://developer.ibm.com/code/journey/decentralized-energy-hyperledger-composer/
* https://developer.ibm.com/code/journey/run-blockchain-technology-on-a-linux-mainframe/
* https://developer.ibm.com/code/journey/create-a-to-do-list-app-using-blockchain/
* https://developer.ibm.com/code/journey/deploy-an-asset-transfer-app-using-blockchain/

# https://www.hyperledger.org/community

## Blockchain in the IBM Cloud: https://console.bluemix.net/catalog/services/blockchain/ 

<img src="http://34b70.http.dal05.cdn.softlayer.net/broker-static/v1-ga1/img4.png">

** Initiate a new blockchain network including setting democratic network policies and inviting new members to join.
** Join a network, as a new member, based on an invite from the network initiator.

* Use Issues to log suggestions to this workshop.
https://github.com/LennartFr/Blockchain-at-Galvanize/issues/1


# Appendix

## Bonus Lab : Let's bring up the Hyperledger Fabric!
Instructions below from thess URLs: 
* http://hyperledger-fabric.readthedocs.io/en/latest/build_network.html 
* http://hyperledger-fabric.readthedocs.io/en/latest/samples.html
* http://hyperledger-fabric.readthedocs.io/en/latest/getting_started.html

### Step 1
Only if necessary, execute the following three commands to remove existing Docker instances.
   * docker kill $(docker ps -q)
   * docker rm $(docker ps -aq)
   * docker rmi $(docker images dev-* -q) 
### Step 2   
    Instructions below come from the following URL: http://hyperledger-fabric.readthedocs.io/en/latest/samples.html  
    From a terminal window on your laptop, execute the following commands:
   * git clone https://github.com/hyperledger/fabric-samples.git into a directory on your laptop
   From that directory on your laptop (see above) invoke:
   * curl -sSL https://goo.gl/Q3YRTi | bash   
   * export PATH=<path to download location>/bin:$PATH  
  
### Step 3 
   * Instructions below come from the following URL:  
      http://hyperledger-fabric.readthedocs.io/en/latest/build_network.html
      
   Bring up the Hyperledger Fabric: 
   * cd first-network
   * ./byfn.sh -m generate
   * ./byfn.sh -m up. //See full output from command on this link http://bit.ly/2yyTeIj
   * After checking the output, remember to run ./byfn.sh -m down.
   
 ### Step 4 (optional) Configurate your Hyperledger Fabric instance.  
 http://hyperledger-fabric.readthedocs.io/en/latest/build_network.html



## Deploy bna file on hyperledger fabric
https://hyperledger.github.io/composer/business-network/bnd-deploy.html
``~
Arnes-MBP:bnafile arnelennartfrantzell$ composer network deploy -p hlfv1 -a my-basic-sample.bna -i PeerAdmin -s randomString -A admin -S
Deploying business network from archive: my-basic-sample.bna
Business network definition:
	Identifier: my-basic-sample@0.1.10
	Description: The Composer basic sample network

✔ Deploying business network definition. This may take a minute...

Command succeeded
~~~

## ping application on hyperledger composer

Arnes-MBP:bnafile arnelennartfrantzell$ composer network ping -n my-basic-sample -p hlfv1 -i admin -s adminpw
The connection to the network was successfully tested: my-basic-sample
	version: 0.14.1
	participant: org.hyperledger.composer.system.NetworkAdmin#admin

Command succeeded

~~~



# Hyperledger and IBM Blockchain

[Hyperledger](http://hyperledger.org/) is an umbrella project of open source blockchains and related tools, started in December 2015 by the Linux Foundation, to support the collaborative development of blockchain-based distributed ledgers.

[Hyperledger Documentation](https://hyperledger-fabric.readthedocs.io/en/release/)


[IBM Blockchain](https://developer.ibm.com/code/technologies/blockchain/)

# Blockchain Usecases from IBM
[Blockchain usecases](https://www.ibm.com/blockchain/use-cases/)

# Agenda

# First lab
[Hyperledger Composer Playground](https://composer-playground.mybluemix.net/login)


[Build a Blockchain Network](https://developer.ibm.com/code/patterns/build-a-blockchain-network/)

[Hyperledger Composer Playground in the Cloud](https://composer-playground.mybluemix.net/login)

[Install Hyperledger Composer locally](https://hyperledger.github.io/composer/installing/using-playground-locally.html)

[Installing a Development environment](https://hyperledger.github.io/composer/installing/development-tools.html)

# Second lab
Follow these instructions to launch a basic IBM Blockchain network on the IBM Container Service's free plan. 

[Develop in a cloud sandbox](IBM Blockchain Platform(https://ibm-blockchain.github.io/)

[Prepare and Setup](https://ibm-blockchain.github.io/setup/

# Third lab

# Where do we go from here?
