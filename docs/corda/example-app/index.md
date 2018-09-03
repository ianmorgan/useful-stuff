# Corda Example App

Some notes on running and using the [example app](https://docs.corda.net/tutorial-cordapp.html) 

## Accessing nodes 

* [PartyA](localhost:10009)
* [PartyB](localhost:10012)
* [PartyC](localhost:10015)

For Party A
* [home](http://localhost:10009/api/example/me)
* [peers](http://localhost:10009/api/example/peers)
* [ious](http://localhost:10009/api/example/ious)
* [web](http://localhost:10009/web/example)

http://localhost:10009/api/example/create-iou with parameters iouValue and partyName which is CN name of a node
There is also a web front-end served from /web/example.

## Create an order 

### REST 

To create an IOU between PartyA and PartyB, run the following command from the command line:

```bash
curl -X PUT 'http://localhost:10009/api/example/create-iou?iouValue=1&partyName=O=PartyB,L=New%20York,C=US'
```

### Console 

```bash
flow start ExampleFlow$Initiator iouValue: 50, otherParty: "O=PartyB,L=New York,C=US"
```

