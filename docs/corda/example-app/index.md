# Corda Example App

Some notes on running and using the [example app](https://docs.corda.net/tutorial-cordapp.html) 

## Accessing nodes 

* **PartyA**  [home](http://localhost:10009/api/example/me) [peers](http://localhost:10009/api/example/peers) [ious](http://localhost:10009/api/example/ious) [web](http://localhost:10009/web/example)
* **PartyB**  [home](http://localhost:10012/api/example/me) [peers](http://localhost:10012/api/example/peers) [ious](http://localhost:10012/api/example/ious) [web](http://localhost:10012/web/example)
* **PartyC**  [home](http://localhost:10015/api/example/me) [peers](http://localhost:10015/api/example/peers) [ious](http://localhost:10015/api/example/ious) [web](http://localhost:10015/web/example)


## Create an order 

### REST 

To create an IOU between PartyA and PartyB, run the following command from the command line:

```bash
curl -X PUT 'http://localhost:10009/api/example/create-iou?iouValue=1&partyName=O=PartyB,L=New%20York,C=US'
```

port 10012 for PartyB
port 10015 for PartyC


### Console 

```bash
flow start ExampleFlow$Initiator iouValue: 50, otherParty: "O=PartyB,L=New York,C=US"
```

