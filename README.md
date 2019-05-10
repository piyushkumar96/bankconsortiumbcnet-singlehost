# bankconsortiumbcnet-singlehost

**In This (BANKCONSORTIUMBCNET) Blockchain Network UseCase :-** 

1. Initially there were **3** orgs (banks) **sbi**,**hdfc**,**icici** having **2**, **3**, and **4** peers respectively. There were **2** channels first **chsbihdfc** (in which initially sbi and hdfc are present) and **chhdfcicici** (in which initially hdfc and icici are present).

2. Then I had **UP** the initial blockchain network which consists of **3 ORGs, 9 PEERS, 3 CAs, 2 CHANNELS**.

3. After this I used the scripts to join peers.

4. Added new peer to exsisting org.

5. Created the new org **pnb** (bank) to exsisting blockchain network with 2 peers.

6. Created new channel.

7. Adding org to channel in which it is not present.  


## Technology STACK
1. Hyperledger Fabric(v1.4)
2. Golang and Nodejs (Chaincode)
3. Docker & Container
4. Shell Scripting
5. Python

## System and Software Requirments
1. Ubuntu, Docker, Golang, Python.
2. Download hypeledger fabric binaries like cryptogen, configtxgen etc. basic bin folder of fabric-samples outside the this repo (after clonning).
3. Download Chaincode folder just outside this repo (after clonning).

-----------------------------------------------------------------------------------------------------------------------------
                                                Command to see the containers of blockchain network
-----------------------------------------------------------------------------------------------------------------------------
**ubuntu@ubuntu:~$ docker ps**

CONTAINER ID        IMAGE                               COMMAND                  CREATED              STATUS              PORTS                                            NAMES

20c347122944        hyperledger/fabric-tools:latest     "/bin/bash"              18 minutes ago      Up 18 minutes                                                        pnbcli

86ae07f6d32c        hyperledger/fabric-peer:latest      "peer node start"        18 minutes ago      Up 18 minutes       0.0.0.0:7121-7122->7121-7122/tcp                 peer0.pnb.bankconsortiumbcnet.com

dd127b153cbd        hyperledger/fabric-peer:latest      "peer node start"        18 minutes ago      Up 18 minutes       0.0.0.0:7123->7121/tcp, 0.0.0.0:7124->7122/tcp   peer1.pnb.bankconsortiumbcnet.com

89fb8b16cabe        hyperledger/fabric-ca:latest        "sh -c 'fabric-ca-se…"   18 minutes ago      Up 18 minutes       7054/tcp, 0.0.0.0:8004->8001/tcp                 ca_peerpnb

d752b7a1c937        hyperledger/fabric-peer:latest      "peer node start"        5 minutes ago       Up 5 minutes        0.0.0.0:7119->7101/tcp, 0.0.0.0:7120->7102/tcp   peer2.sbi.bankconsortiumbcnet.com

44a7a912fac6        hyperledger/fabric-tools:latest     "/bin/bash"              43 seconds ago       Up 33 seconds                                                        bankconsortiumbcnetcli

b7c3f2dd9610        hyperledger/fabric-peer:latest      "peer node start"        About a minute ago   Up 48 seconds       0.0.0.0:7107->7105/tcp, 0.0.0.0:7108->7106/tcp   peer1.hdfc.bankconsortiumbcnet.com

ae0e7b1c2644        hyperledger/fabric-ca:latest        "sh -c 'fabric-ca-se…"   About a minute ago   Up 47 seconds       7054/tcp, 0.0.0.0:8002->8001/tcp                 ca_peerhdfc

b99d206f7a53        hyperledger/fabric-peer:latest      "peer node start"        About a minute ago   Up 48 seconds       0.0.0.0:7117->7111/tcp, 0.0.0.0:7118->7112/tcp   peer3.icici.bankconsortiumbcnet.com

e06be2deeed0        hyperledger/fabric-peer:latest      "peer node start"        About a minute ago   Up 48 seconds       0.0.0.0:7115->7111/tcp, 0.0.0.0:7116->7112/tcp   peer2.icici.bankconsortiumbcnet.com

5dabdc93e81d        hyperledger/fabric-peer:latest      "peer node start"        About a minute ago   Up 48 seconds       0.0.0.0:7105-7106->7105-7106/tcp                 peer0.hdfc.bankconsortiumbcnet.com

861a7e5c91b0        hyperledger/fabric-peer:latest      "peer node start"        About a minute ago   Up 43 seconds       0.0.0.0:7101-7102->7101-7102/tcp                 peer0.sbi.bankconsortiumbcnet.com

1f900f99b709        hyperledger/fabric-peer:latest      "peer node start"        About a minute ago   Up 45 seconds       0.0.0.0:7113->7111/tcp, 0.0.0.0:7114->7112/tcp   peer1.icici.bankconsortiumbcnet.com

f50fc4a50e69        hyperledger/fabric-orderer:latest   "orderer"                About a minute ago   Up 48 seconds       0.0.0.0:7050->7050/tcp                           orderer.bankconsortiumbcnet.com

9a3629328fb9        hyperledger/fabric-ca:latest        "sh -c 'fabric-ca-se…"   About a minute ago   Up 44 seconds       7054/tcp, 0.0.0.0:8001->8001/tcp                 ca_peersbi

4c03e8c6bfd0        hyperledger/fabric-peer:latest      "peer node start"        About a minute ago   Up 44 seconds       0.0.0.0:7111-7112->7111-7112/tcp                 peer0.icici.bankconsortiumbcnet.com

d5e9d154a06a        hyperledger/fabric-ca:latest        "sh -c 'fabric-ca-se…"   About a minute ago   Up 47 seconds       7054/tcp, 0.0.0.0:8003->8002/tcp                 ca_peericici

efc3cfa2a3fc        hyperledger/fabric-peer:latest      "peer node start"        About a minute ago   Up 43 seconds       0.0.0.0:7109->7105/tcp, 0.0.0.0:7110->7106/tcp   peer2.hdfc.bankconsortiumbcnet.com

4240dda1c60b        hyperledger/fabric-peer:latest      "peer node start"        About a minute ago   Up 46 seconds       0.0.0.0:7103->7101/tcp, 0.0.0.0:7104->7102/tcp   peer1.sbi.bankconsortiumbcnet.com

-----------------------------------------------------------------------------------------------------------------------------
                                                              END
-----------------------------------------------------------------------------------------------------------------------------
