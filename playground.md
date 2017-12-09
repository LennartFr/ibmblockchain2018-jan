[Hyperledger Composer Playground](https://composer-playground.mybluemix.net/login)

# Perishable Goods Network

## Participants: Growe, Importer, Shipper
## Assets: Contract
{
  "$class": "org.acme.shipping.perishable.Contract",
  
  "contractId": "CON_001",
  
  "grower": "resource:org.acme.shipping.perishable.Grower#farmer@email.com",
  
  "shipper": "resource:org.acme.shipping.perishable.Shipper#shipper@email.com",
  
  "importer": "resource:org.acme.shipping.perishable.Importer#supermarket@email.com",
  
  "arrivalDateTime": "2017-12-10T07:07:14.370Z",
  
  "unitPrice": 0.5,
  
  "minTemperature": 2,
  
  "maxTemperature": 10,
  
  "minPenaltyFactor": 0.2,
  
  "maxPenaltyFactor": 0.1
}

## Assets: Shipment

{
  "$class": "org.acme.shipping.perishable.Shipment",
  
  "shipmentId": "SHIP_001",
  
  "type": "BANANAS",
  
  "status": "IN_TRANSIT",
  
  "unitCount": 5000,
  
  "contract": "resource:org.acme.shipping.perishable.Contract#CON_001"
}



## Transactions: TemperatureReading, ShipmentReceived, SetupDemo
