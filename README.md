## Dappnode Package SSV Göerli Testnet V2 "Shifu"

This package allows Dappnode Users to help test the SSV Network.

_Note: This package is separate from the SSV Prater Package, and they are incompatible with each other. If you participated in the first V1 SSV testnet "Primus" please keep your operator running until the SSV team announces the official end of the V1 test._
**DO NOT** Reuse keys from V1. You need to create new keys and register them [here](https://app.ssv.network/join/operator/register)

You'll need a keypair in order to run an operator on SSV. To generate a new keypair, you will need access to a terminal on a machine connected to the Internet with Docker installed, such as your Dappnode.  You need to run the following command :
      
      docker run -d --name=ssv_node_op_key -it 'bloxstaking/ssv-node:latest' \
      /go/bin/ssvnode generate-operator-keys && docker logs ssv_node_op_key --follow \
      && docker stop ssv_node_op_key && docker rm ssv_node_op_key
      
This command will generate a PK (Public Key) and a SK (Secret Key). Make sure to back up the output of this command in a safe place and only enter the SK (Secret Key) in this field.  The SK (Secret Key) is all the characters (including special characters i.e. =) between the quotation marks (" ") directly following "{"app": "SSV-Node", "sk":"  in the output of the command.
      
Please check the official documentation from the SSV Team [here](https://docs.ssv.network/run-a-node/operator-node/installation#generate-operator-keys) for more information. 

Note - You will need SSH or direct console access to your Dappnode in order to use it to generate your operator keys.
